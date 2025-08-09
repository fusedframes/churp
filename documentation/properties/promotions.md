`promotions`
=======

**Description**  
Specifies one or more promotional offers applicable to the offer. Enables detailed representation of discounts, special deals or incentives to improve sales and engagement.

**Required**  
No

**Expected Type**  
`Array<Object>`

# benefit

promotions > benefit

**Description**  
Specifies the advantage or reward granted by the promotion. Enables clear communication of what the customer gains.

**Guideline**  
Clear description of the reward.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"benefit": "10% discount on your total order"
```

### Incorrect Example

```json
"benefit": "huge discount on your total order"
```

# countries

promotions > countries

**Description**  
List of country codes where the promotion is valid. Enables geo-targeting for accurate promotion eligibility.

**Guideline**  
Use the ISO 3166 short name.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"countries": ["Italy"]
```

### Incorrect Example

```json
"countries": ["IT"]
```

# minimum_age

promotions > minimum_age

**Description**  
Minimum age required to be eligible for the promotion. Helps enforce age-appropriate targeting.

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

# subscribed_email_required

promotions > subscribed_email_required

**Description**  
Indicates whether users must be subscribed to email marketing to qualify. Enables promotions tied to communication opt-in.

**Required**  
No

**Expected Type**  
`Boolean`

# user_type

promotions > user_type

**Description**  
Specifies the customer type the promotion applies to. Enables segmentation by user journey stage.

**Guideline**  
Use the enumerated values.

**Enumerated Values**  
new_customer — First-time buyer or newly registered user  
existing_customer — User with past purchases or activity  
all — Promotion available to all users  

**Required**  
No

**Expected Type**  
`String`

# minimum_purchase_amount

promotions > minimum_purchase_amount

**Description**  
Minimum spend required to activate the promotion. Supports conditional promotions based on order value.

**Guideline**  
Currency symbol followed by the amount.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"minimum_purchase_amount": "€5"
```

### Incorrect Example

```json
"minimum_purchase_amount": "EUR 5"
```

# note

promotions > note

**Description**  
Optional disclaimer or notice related to eligibility. Helps communicate important conditions or limitations that users should be aware of.

**Guideline**  
Concise text with clear message.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"note": "Offer not valid during public holidays"
```

### Incorrect Example

```json
"note": "Public holidays excluded"
```

# custom_rules

promotions > custom_rules

**Description**  
Additional eligibility notes or clarifications. Enables inclusion of custom rules that don't fit structured fields.

**Guideline**  
Each rule must be a clear, actionable condition, not vague.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"custom_rules": ["Must complete onboarding tutorial"]
```

### Incorrect Example

```json
"custom_rules": ["Onboarding tutorial"]
```

# linked_offer

promotions > custom_rules

**Description**  
Provides a direct URL to the related offer. Enables easy access and reference to the specific offer from the promotion.

**Guideline**  
Use a direct, public URL to the offer. Avoid redirects, query strings, or tracking codes.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"linked_offer": "https://acmecorp.com/products/vinyl-turntable"
```

### Incorrect Example

```json
"linked_offer": "/products/vinyl-turntable"
```