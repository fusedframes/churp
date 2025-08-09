`restrictions`
=======

**Description**  
A set of limitations and conditions applicable to the offer. Enables precise control over user eligibility and compliance requirements.

**Required**  
No

**Expected Type**  
`Object`

# minimum_age

restrictions > minimum_age

**Description**  
Specifies the minimum age required to purchase or use the offer. Ensures legal compliance and appropriate user access restrictions.

**Guideline**  
Use a positive integer.

**Required**  
No

**Expected Type**  
`Integer`

### Correct Example

```json
"minimum_age": 18
```

### Incorrect Example

```json
"minimum_age": "adult"
```

# regulated_category

restrictions > regulated_category

**Description**  
Specifies if the product or service falls into a regulated category, such as alcohol or tobacco. Helps with compliance and content filtering.

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