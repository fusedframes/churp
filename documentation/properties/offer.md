`offer`
=======

**Description**  
Key information describing the product or service. Provides essential details for identification and classification.

**Required**  
Yes

**Expected Type**  
`Object`

# name

offer > name

**Description**  
The title of the product or service. Used for clear identification and reference.

**Guideline**  
Don't include modifiers in the string.

**Required**  
Yes

**Expected Type**  
`String`

### Correct Example

```json
"name": "Acme Monogram Cricket Bat"
```

### Incorrect Example

```json
"name": "Red Acme Monogram Cricket Bat"
```

# producer

offer > producer

**Description**  
The creator of the product or service, distinct from the seller. Indicates who makes the product or service.

**Guideline**  
Use the commercially recognised name.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"producer": "Acme"
```

### Incorrect Example

```json
"producer": "Acme Global Trading Limited"
```

# version

offer > version

**Description**  
Specifies the generation of the product or service being offered. Helps distinguish between different iterations or releases.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"version": "2025"
```

# category

offer > category

**Description**  
Specifies the type or class the product or service belongs to. Helps summarise the product or service for improved understanding.

**Guideline**  
Avoid generic or overly broad terms.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"category": "Cricket Bat"
```

### Incorrect Example

```json
"category": "Sports Equipment"
```

# manufactured_in

offer > manufactured_in

**Description**  
Indicates the country where the producer states the product or service is created. Helps support regulatory transparency.

**Guideline**  
Use the ISO 3166 short name.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"manufactured_in": "Japan"
```

### Incorrect Example

```json
"manufactured_in": "JP"
```

# quantity

offer > quantity

**Description**  
Indicates the number of units included in the product or service. Provides clarity on what is included and supports quantity-based pricing and bundling.

**Guideline**  
Must be positive.

**Required**  
Yes

**Expected Type**  
`Integer`

### Correct Example

```json
"quantity": 5
```

### Incorrect Example

```json
"quantity": "pack of five"
```

# build_time

offer > build_time

**Description**  
Estimated duration required to prepare or assemble the product before it is ready for fulfillment. Enables setting customer expectations for timing.

**Guideline**  
Numeric value or threshold followed by a time unit.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"build_time": "3-4 working days"
```

### Incorrect Example

```json
"build_time": "3-4"
```

# included_items

offer > included_items

**Description**  
Lists individual components included in the offer. Enables clear understanding of what the customer will receive.

**Guideline**  
Use specific and clear item names.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"included_items": ["USB-C Charger"]
```

### Incorrect Example

```json
"included_items": ["Charger"]
```