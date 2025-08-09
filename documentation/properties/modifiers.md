`modifiers`
==========

**Description**  
Defines selectable options that adjust or create details outside of offer and value fields. Supports representation of options like volume pricing, product variants, add-ons and service customisations.

You can find out more information by viewing the using modifiers section.

**Required**  
No

**Expected Type**  
`Array<Object>`

# label

modifiers > label

**Description**  
Provides a concise name for the option. Enables users to quickly understand the purpose of the modifier.

**Guideline**  
Keep short and simple.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"label": "SSD Storage"
```

### Incorrect Example

```json
"label": "SSD Storage Options"
```

# explainer

modifiers > explainer

**Description**  
Gives a short explanation of how the modifier label changes the offer. Supports better understanding and clarity through added context.

**Guideline**  
Keep short and simple.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"explainer": "Increases the SSD storage available"
```

### Incorrect Example

```json
"explainer": "These options change the available SSD storage on the Acme Ultra Computer"
```

# options

modifiers > options

**Description**  
Lists multiple selectable values for the modifier. Provides clear multi-option availability.

**Required**  
No

**Expected Type**  
`Array<Object>`

## value

modifiers > options > value

**Description**  
Identifies the specific selectable variant. Used to differentiate options offered under a modifier.

**Guideline**  
Keep short and simple. Don't include offer name.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"value": "500GB"
```

### Incorrect Example

```json
"value": "500GB - Acme Ultra Computer"
```

## countries

modifiers > options > countries

**Description**  
Specifies the countries where the nested adjustments apply. Allows for region-specific availability, features and pricing.

**Guideline**  
Use the ISO 3166 short name.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"countries": ["United Kingdom"]
```

### Incorrect Example

```json
"countries": ["UK"]
```

## base_price_delta

modifiers > options > base_price_delta

**Description**  
Adjusts the base price when this option is selected. Enables dynamic pricing based on selected options.

**Guideline**  
Use plus or minus with currency symbol followed by the amount, or currency symbol followed by 0 if free. Should be the price of the units combined not per unit.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"base_price_delta": "+£10"
```

### Incorrect Example

```json
"base_price_delta": "10"
```

## original_price_delta

modifiers > options > original_price_delta

**Description**  
Modifies the original listed price based on the selected option. Reflects original pricing changes due to variant selection.

**Guideline**  
Currency symbol followed by the amount.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"original_price_delta": "£5"
```

### Incorrect Example

```json
"original_price_delta": "GBP 5"
```

## tax_amount_delta

modifiers > options > tax_amount_delta

**Description**  
Specifies how tax changes with the selected option. Enables tax transparency for different selected options.

**Guideline**  
Currency symbol followed by the amount.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"tax_amount_delta": "£2"
```

### Incorrect Example

```json
"tax_amount_delta": "Two Great British Pounds"
```

## quantity_delta

modifiers > options > quantity_delta

**Description**  
Specifies how the offer quantity is adjusted when a modifier is selected. Enables clarity for bundles, reductions or additions.

**Guideline**  
Can be positive or negative.

**Required**  
No

**Expected Type**  
`Integer`

### Correct Example

```json
"quantity_delta": 2
```

### Incorrect Example

```json
"quantity_delta": "Includes Two"
```

## add

modifiers > options > add

**Description**  
Allows adding new properties or content that doesn't exist elsewhere in the schema when this modifier option is selected.

**Guideline**  
Nest under add to include something new alongside content defined outside of modifiers. Use this only when the item does not already exist outside of modifiers.

You can find out more information by viewing the using modifiers section.

**Required**  
No

**Expected Type**  
`Array<Object>`