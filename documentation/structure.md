Structure
=========

This file explains how to organise Churp data. It covers the required properties, shows every property in its hierarchy and explains how to use modifiers, so your product or service data stays clear for AI systems to understand.

## Property Hierarchy

@context
offer
    name
    producer
    version
    category
    manufactured_in
    quantity
    build_time
    included_items
value
    countries
    base_price
    original_price
    import_duties_paid
    price_including_tax
    tax_amount
identifier
    type
    value
transaction
    type
    methods
availability
    countries
    excluded_regions
    excluded_postal_codes
    stock_state
    stock_quantity
    languages
relations
    often_bought_with
        offer_name
        offer_url
        stock_state
    requires
        offer_name
        offer_url
        stock_state
    compatible_with
        offer_name
        offer_url
        stock_state
    fallbacks
        offer_name
        offer_url
        stock_state
    upsells
        offer_name
        offer_url
        stock_state
restrictions
    minimum_age
    regulated_category
fulfillment
    method
    timeframe
    price
    tax_amount
    countries
    excluded_regions
    excluded_postal_codes
    note
    included_items_override
    carbon_footprint
    build_time_override
actions
    label
    target
    intent
promotions
    benefit
    countries
    minimum_age
    subscribed_email_required
    user_type
    minimum_purchase_amount
    note
    custom_rules
    linked_offer
media
    source
    position_preference
    description
features
    name
    description
    value
seller
    commercial_name
    entity_name
    locations
        branch_name
        address_line
        postal_code
        city
        country
        intent
terms
    commitment_period
    deposit_amount
    renewal_frequency
    policies
        title
        overview
        reference_url
    warranties
        overview
        reference_url
    liability_limit
    insurance_notice
contact
    method
    handle
    hours
    timezone
    days
    intent
legal
    title
    summary
    reference_url
    jurisdictions
customer_context
    recommend_if
    not_recommended_if
    ideal_conditions
    problem_it_solves
    learning_curve
    frequently_asked
        question
        answer
    gender
    age_range
lifecycle
    stage
    estimated_lifespan
    estimated_maintenance
    estimated_ownership_cost
    discontinued_on
    repairability
    carbon_footprint
ux_preference
    tone
    layout
    brand_color
documents
    title
    overview
    intent
    file_url
    language
ratings
    label
    average_value
    total_count
    score_range
    best_score
    reviews
        reviewer
        date
        score
        content
        media
    collected_by
recognitions
    title
    type
    issuing_body
    summary
    proof
instructions
    care
    setup
    disposal
    warnings
    usage
modifiers
    label
    explainer
    options
        value
        countries
        base_price_delta
        original_price_delta
        tax_amount_delta
        quantity_delta
        add

## Using Modifiers
Modifiers allow you to create flexible options for users. This is achieved by overriding, adding or removing specific properties. You can use modifiers to change nearly all properties within the schema. This makes your offer adjustable and clear for both people and systems.

If something only applies to certain options, include it only inside those modifiers. Do not place it outside the modifiers section unless it applies to every option. Modifiers inherit values from outside, so if a value should not apply to an option, simply leave it out. This makes each option self-contained, consistent and unambiguous.

### Hierarchy

This shows where different types of properties can be nested inside a modifier. For each option, you can include any content property from the Churp schema, excluding unmodifiable properties.

The properties should follow the same structure as the schema hierarchy. For example, to change source within media, nest source under media.

modifiers
    label
    explainer
    options
        value
        countries
        base_price_delta
        original_price_delta
        tax_amount_delta
        quantity_delta
        **overriding properties**
        add
            **added properties**

### Overriding

Nest under value to override values defined outside of modifiers. Place these below standard items like countries, base_price_delta and quantity_delta, following the structure in the diagram. Use this when you need to change or extend something that already exists.

```json
{
  "@context": "https://www.churp.dev/context/v1.0.json",
  "offer": {
    "name": "64GB USB 2.0 Flash Drive",
    "quantity": 1
  },
  "value": [
    {
      "base_price": "$15.00",
      "price_including_tax": true
    }
  ],
  "availability": [
    {
      "stock_state": "in_stock",
      "stock_quantity": 10
    }
  ],
  "modifiers": [
    {
      "label": "Quantity Bundle Discounts",
      "explainer": "Unit price is cheaper when you buy in bulk",
      "options": [
        {
          "value": "Pack of Two",
          "base_price_delta": "+$10.00",
          "quantity_delta": 2
        },
        {
          "value": "Pack of Five",
          "base_price_delta": "+$35.00",
          "quantity_delta": 5
        }
      ]
    }
  ],
  "seller": {
    "entity_name": "Acme & Co Ltd"
  }
}
```

### Adding

Nest under add to include something new alongside content defined outside of modifiers. Use this only when the item does not already exist outside of modifiers.

```json
{
  "@context": "https://www.churp.dev/context/v1.0.json",
  "offer": {
    "name": "Quick Drying Sports T-Shirt",
    "quantity": 1
  },
  "value": [
    {
      "base_price": "$45.00",
      "price_including_tax": true
    }
  ],
  "modifiers": [
    {
      "label": "Colour",
      "explainer": "Changes the colour of the T-Shirt",
      "options": [
        {
          "value": "Sea Blue",
          "add": [
            {
              "identifier": {
                "type": "gtin",
                "value": "5012345678900"
              }
            }
          ]
        },
        {
          "value": "Pine Green",
          "add": [
            {
              "identifier": {
                "type": "gtin",
                "value": "8901234567897"
              }
            }
          ]
        }
      ]
    }
  ],
  "seller": {
    "entity_name": "Cool Clo Ltd"
  }
}
```

### Unmodifiable Properties

Some properties cannot be changed within modifiers. These include any properties under @context, offer or value, as they define the original offer and must remain unchanged. To adjust things like price or quantity, use the provided modifier properties such as base_price_delta or quantity_delta. Use the diagram below to see all the unmodifiable properties.

@context
offer
    name
    producer
    version
    category
    manufactured_in
    quantity
    build_time
    included_items
value
    countries
    base_price
    original_price
    import_duties_paid
    price_including_tax
    tax_amount

## Required Properties

The following properties must always be included: @context as a top-level property, name and quantity must be nested under offer and entity_name must be nested under seller. These are essential for identifying and validating the content. Use the diagram below to see all the required properties.

@context
offer
    name
    quantity
seller
    entity_name

## Required Order

The top-level properties must follow this order: first @context, then offer, then value. This order is required and must be followed exactly. After value, you can use any order for the remaining content. Inside any property, the items it contains can also be in any order. Use the diagram below to see the required order.

@context
offer
value