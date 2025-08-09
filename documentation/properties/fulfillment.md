`fulfillment`
=======

**Description**  
Defines how the offer is provided to the customer. Enables accurate representation of service expectations and logistics.

**Required**  
No

**Expected Type**  
`Array<Object>`

# method

fulfillment > method

**Description**  
Specifies the type of delivery or collection option. Supports clear communication of the nature of the fullfillment type.

**Guideline**  
Short and recognisable name.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"method": "Local Pickup"
```

### Incorrect Example

```json
"method": "You can come and get it from our warehouse"
```

# timeframe

fulfillment > timeframe

**Description**  
Specifies the expected duration for completing the fulfillment process. Enables accurate delivery estimates and helps manage customer expectations.

**Guideline**  
Numeric value or threshold followed by a time unit.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"timeframe": "1-2 working days"
```

### Incorrect Example

```json
"timeframe": "1-2"
```

# price

fulfillment > price

**Description**  
Specifies the cost associated with the fulfillment method. Enables transparent pricing by clearly breaking down charges.

**Guideline**  
Currency symbol followed by the amount. If the delivery cost is free, represent it simply as the currency symbol followed by 0.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"price": "£7.00"
```

### Incorrect Example

```json
"price": "seven pounds"
```

# tax_amount

fulfillment > tax_amount

**Description**  
Amount of tax applied to the fulfillment cost. Enables clear breakdown of charges and accurate pricing calculations.

**Guideline**  
Currency symbol followed by the amount. Tax is added on top of the fulfilment price if the offer has price_including_tax set to true; if false, tax is assumed already included in the price.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"tax_amount": "£1.00"
```

### Incorrect Example

```json
"tax_amount": "1.00 GBP"
```

# countries

fulfillment > countries

**Description**  
Specifies the countries where the fulfillment option can be used. Used to define the geographic scope of availability.

**Guideline**  
Use the ISO 3166 short name.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"countries": ["Netherlands"]
```

### Incorrect Example

```json
"countries": ["NL"]
```

# excluded_regions

fulfillment > excluded_regions

**Description**  
Lists areas within included countries where the fulfillment option is not available. Enables exceptions within broader availability zones.

**Guideline**  
Use commonly recognised names. Avoid codes or abbreviations.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"excluded_regions": ["North Brabant"]
```

### Incorrect Example

```json
"excluded_regions": ["NL-NB"]
```

# excluded_postal_codes

fulfillment > excluded_postal_codes

**Description**  
Specifies regional patterns to exclude from fulfillment options within a country. Enables exceptions within broader availability zones.

**Guideline**  
Prefix of a postal code followed by an asterisk (*) to exclude all matching areas.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"excluded_postal_codes": ["4*"]
```

### Incorrect Example

```json
"excluded_postal_codes": ["40*", "41*", "42*", "43*", "44*", "45*", "46*", "47*", "48*", "49*"]
```

# note

fulfillment > note

**Description**  
Provides additional important information or instructions related to the fulfillment process. Enables clearer communication and helps set proper expectations.

**Guideline**  
Concise text with clear instructions or details.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"note": "Order by 2pm on a working day for next working day delivery. Working days are Monday to Friday, excluding bank holidays."
```

### Incorrect Example

```json
"note": "Next working day"
```

# included_items_override

fulfillment > included_items_override

**Description**  
Overrides the list of individual components included in the offer. Enables updating the contents of what is included in the offer based off the selected fulfillment option.

**Guideline**  
Use specific and clear item names. Provide an empty array if all items should be removed.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"included_items_override": ["USB-C Charger"]
```

### Incorrect Example

```json
"included_items_override": [""]
```

# carbon_footprint

fulfillment > carbon_footprint

**Description**  
Estimated carbon impact of the delivery, expressed in CO₂e equivalent. Supports transparency and informed consumer decisions.

**Guideline**  
Grams or kilograms of CO₂e.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"carbon_footprint": "300g CO₂e"
```

### Incorrect Example

```json
"carbon_footprint": "low impact"
```

# build_time_override

fulfillment > build_time_override

**Description**  
Overrides the duration required to prepare or assemble the offer before it is ready for fulfillment. Enables updating build times based on fulfillment method selected.

**Guideline**  
Numeric value or threshold followed by a time unit.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"build_time_override": "6-7 business days"
```

### Incorrect Example

```json
"build_time_override": "6-7"
```