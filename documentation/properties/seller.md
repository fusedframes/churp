`seller`
==========

**Description**  
Contains information about the party providing the offer. Enables identification and location-specific details for support or compliance.

**Required**  
Yes

**Expected Type**  
`Object`

# commercial_name

seller > commercial_name

**Description**  
Recognised trading name of the business entity. Enables brand attribution and customer trust.

**Guideline**  
Commonly recognised brand name or trading name. This may differ from legal name.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"commercial_name": "Ecosound"
```

### Incorrect Example

```json
"commercial_name": "Ecosound & Partners Limited"
```

# entity_name

seller > entity_name

**Description**  
Displays the officially registered name of the business or organisation. Helps for transparency and compliance.

**Guideline**  
Full legal name as registered with official authorities.

**Required**  
Yes

**Expected Type**  
`String`

### Correct Example

```json
"entity_name": "Ecosound & Partners Limited"
```

### Incorrect Example

```json
"entity_name": "Ecosound"
```

# locations

seller > locations

**Description**  
Specifies physical seller sites customers can visit or contact. Enables online seller compliance and customer support.

**Required**  
No

**Expected Type**  
`Array<Object>`

## branch_name

seller > locations > branch_name

**Description**  
Identifying label for the specific seller location. Aids customer clarity for multi-branch operations.

**Guideline**  
Official name of the branch.

**Required**  
No

**Expected Type**  
`String`

## address_line

seller > locations > address_line

**Description**  
Provides the house number and street address of the seller location. Used for customer reference and compliance.

**Guideline**  
Street and number in the country's valid format.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"address_line": "Keizersgracht 456"
```

### Incorrect Example

```json
"address_line": "456 Keizersgracht Street"
```

## postal_code

seller > locations > postal_code

**Description**  
The local postal or ZIP code for the seller location. Enables precise geolocation and compliance.

**Guideline**  
Valid local postal format.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"postal_code": "1017 EG"
```

### Incorrect Example

```json
"postal_code": "1017EG"
```

## city

seller > locations > city

**Description**  
The name of the city or municipality where the branch or facility is located. Enables customers to visit locations and meet digital seller compliance laws.

**Guideline**  
Official city name.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"city": "Amsterdam"
```

### Incorrect Example

```json
"city": "The Dam"
```

## country

seller > locations > country

**Description**  
The full name of the country in which the location resides. Enables location filtering and compliance enforcement.

**Guideline**  
Use the ISO 3166 short name.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"country": "Netherlands"
```

### Incorrect Example

```json
"country": "NL"
```

## intent

seller > locations > intent

**Description**  
Defines the operational purposes the location supports. Enables functional categorization of seller locations for accurate user guidance and operational logic.

**Guideline**  
Use a clear and recognisable singular action for each value.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"intent": ["purchase"]
```

### Incorrect Example

```json
"intent": ["purchase and pickup"]
```