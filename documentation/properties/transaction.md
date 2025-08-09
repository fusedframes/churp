`transaction`
=======

**Description**  
Defines how the offer is acquired. Supports system understanding of commitments and payment types.

**Required**  
No

**Expected Type**  
`Object`

# type

transaction > type

**Description**   
Specifies the kind of transaction being offered. Provides context for the purchase process.

**Guideline**  
Use the enumerated values.

**Enumerated Values**  
one-time — Single acquisition without recurring charges  
subscription — Ongoing access or delivery with recurring charges  
rental — Temporary use for a specified period  
lease — Long-term rental with contract terms  
pre-order — Acquisition before availability  
gift — Acquisition without cost  
book — Schedule access to a service for a specific time slot  
reserve — Hold an item without completing acquisition  

**Required**  
No

**Expected Type**  
`String`

# methods

transaction > methods

**Description**  
Indicates the accepted means for completing the transaction. Supports transparency around available options for fulfilling the purchase process.

**Guideline**  
Avoid abbreviations or informal phrasing.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"methods": ["American Express"]
```

### Incorrect Example

```json
"methods": ["amex"]
```