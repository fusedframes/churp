`identifier`
=======

**Description**  
Specifies a unique reference used to identify the offer. Helps provide accurate search results.

**Required**  
No

**Expected Type**  
`Object`

# type

identifier > type

**Description**  
Specifies the kind of identifier being used. Provides the correct context for the value.

**Guideline**  
Use a standard identifier name in uppercase format.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"type": "GTIN"
```

### Incorrect Example

```json
"type": "GLOBALTRADENUMBER"
```

# value

identifier > value

**Description**  
The actual code used to identify the offer. Enables precise lookup of the offer.

**Guideline**  
Must match the format for the corresponding identifier type.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"value": "1234567890123"
```

### Incorrect Example

```json
"value": "GTIN 1234567890123"
```