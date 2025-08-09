`value`
=======

**Description**  
Specifies pricing-related figures associated with the offer. Enables a clear understanding of pricing, taxes and discounts.

**Required**  
No

**Expected Type**  
`Array<Object>`

# countries

value > countries

**Description**  
Defines the set of countries where specific pricing-related values apply. Enables regional differentiation and accurate presentation.

**Guideline**  
Use the ISO 3166 short name for each country.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"countries": ["United States of America"]
```

### Incorrect Example

```json
"countries": ["USA"]
```

# base_price

value > base_price

**Description**  
Specifies the current selling price of the offer before shipping, modifiers, promotions or taxes if price_including_tax is false. Enables clear communication of current selling price.

**Guideline**  
Currency symbol followed by the amount. If the delivery cost is free, represent it simply as the currency symbol followed by 0.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"base_price": "$150"
```

### Incorrect Example

```json
"base_price": "150 USD"
```

# original_price

value > original_price

**Description**  
Represents the previously listed or recommended price of the offer before shipping, modifiers, promotions or taxes if price_including_tax is false. Allows highlighting price changes.

**Guideline**  
Currency symbol followed by the amount.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"original_price": "$170"
```

### Incorrect Example

```json
"original_price": "Was $170"
```

# import_duties_paid

value > import_duties_paid

**Description**  
Specifies whether charges for transporting the offer to the customer's country are included in the base price. Enables clear understanding of total cost to receive the offer.

**Required**  
No

**Expected Type**  
`Boolean`

# price_including_tax

value > price_including_tax

**Description**  
Indicates whether applicable government charges are included in the base price. Provides transparency on charges the customer will have to pay.

**Required**  
No

**Expected Type**  
`Boolean`

# tax_amount

value > tax_amount

**Description**  
Details the amount added to the offer due to government charges on the sale. Breaks down government charges for transparency.

**Guideline**  
Currency symbol followed by the amount.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"tax_amount": "$6.50"
```

### Incorrect Example

```json
"tax_amount": "6.50 USD"
```