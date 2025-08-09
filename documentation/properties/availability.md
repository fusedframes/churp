`availability`
=======

**Description**  
Specifies when and where the offer can be accessed or obtained. Enables clarity for distribution and visibility.

**Required**  
No

**Expected Type**  
`Array<Object>`

# countries

availability > countries

**Description**  
Specifies the countries where the offer can be received. Used to define the geographic scope of availability.

**Guideline**  
Use the ISO 3166 short name for each country.

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

# excluded_regions

availability > excluded_regions

**Description**  
Lists areas within included countries where the offer is not available. Enables exceptions within broader availability zones.

**Guideline**  
Use commonly recognised names. Avoid codes or abbreviations.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"excluded_regions": ["Scottish Highlands"]
```

### Incorrect Example

```json
"excluded_regions": ["HLD"]
```

# excluded_postal_codes

availability > excluded_postal_codes

**Description**  
Specifies regional patterns to exclude from availability within a country. Enables exceptions within broader availability zones.

**Guideline**  
Prefix of a postal code followed by an asterisk (*) to exclude all matching areas.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"excluded_postal_codes": ["IV*"]
```

### Incorrect Example

```json
"excluded_postal_codes": ["IV1", "IV2", "IV3", "IV4", "IV5", "IV6", "IV7", "IV8", "IV9", "IV10", "IV11", "IV12", "IV13", "IV14", "IV15", "IV16", "IV17", "IV18", "IV19", "IV20", "IV21", "IV22", "IV23", "IV24", "IV25", "IV26", "IV27", "IV28", "IV30", "IV31", "IV32", "IV36", "IV40", "IV41", "IV42", "IV43", "IV44", "IV45", "IV46", "IV47", "IV48", "IV49", "IV51", "IV52", "IV53", "IV54", "IV55", "IV56"]
```

# stock_state

availability > stock_state

**Description**  
Indicates the current inventory status of the offer. Enables accurate presentation of availability.

**Guideline**  
Use the enumerated values.

**Enumerated Values**  
in_stock — Item or service is readily available  
low_stock — Limited quantity remaining  
out_of_stock — Currently unavailable  
backorder — Can be ordered for later fulfilment  
by_request — Availability confirmed upon inquiry  
preorder — Available to order before first fulfillment  
notify_when_in_stock — Currently unavailable and can be alerted when available  
discontinued — No longer supplied  

**Required**  
No

**Expected Type**  
`String`

# stock_quantity

availability > stock_quantity

**Description**  
Specifies the number of units currently available. Provides clarity in levels of availability.

**Guideline**  
Must be positive.

**Required**  
No

**Expected Type**  
`Integer`

### Correct Example

```json
"stock_quantity": 10
```

### Incorrect Example

```json
"stock_quantity": "ten units"
```

# languages

availability > languages

**Description**  
Lists languages supported by the offer. Enables users to understand available options for usage and localisation.

**Guideline**  
Use the ISO 639-1 codes, optionally combined with ISO 3166 country codes to indicate regional language use.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"languages": ["en-us"]
```

### Incorrect Example

```json
"languages": ["english-us"]
```