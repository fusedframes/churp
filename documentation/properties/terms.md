`terms`
==========

**Description**  
Defines the contractual conditions and agreements governing the offer. Enables clear communication of user obligations and provider commitments.

**Required**  
No

**Expected Type**  
`Object`

# commitment_period

terms > commitment_period

**Description**  
Duration the user agrees to commit to the offer. Helps set clear expectations around minimum usage periods.

**Guideline**  
Numeric value or threshold followed by a time unit.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"commitment_period": "12 months"
```

### Incorrect Example

```json
"commitment_period": "12"
```

# deposit_amount

terms > deposit_amount

**Description**  
Upfront refundable or non-refundable amount required to secure the offer. Enables transparent financial expectations.

**Guideline**  
Currency symbol followed by the amount.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"deposit_amount": "$20"
```

### Incorrect Example

```json
"deposit_amount": "20 USD"
```

# renewal_frequency

terms > renewal_frequency

**Description**  
How often the product or service automatically renews. Supports clear communication of ongoing commitments.

**Guideline**  
Use clear time intervals. Avoid vague, unclear or verbose phrases.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"renewal_frequency": "monthly"
```

### Incorrect Example

```json
"renewal_frequency": "every 1 month"
```

# policies

terms > policies

**Description**  
Outlines key policies that apply to the offer. Enables users to understand important terms before purchase or use.

**Required**  
No

**Expected Type**  
`Array<Object>`

## title

terms > policies > title

**Description**  
Lists the title of the policy. Enables users to understand what the policy refers to.

**Required**  
No

**Expected Type**  
`String`

## overview

terms > policies > overview

**Description**  
Brief non-binding summary of relevant policies related to the offer. Provides quick understanding without legal jargon.

**Guideline**  
Use plain text. Avoid legal jargon, vague phrases or full policy text.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"overview": ["returns accepted within 30 days of delivery"]
```

### Incorrect Example

```json
"overview": ["We accept returns within 30 days of delivery. Please refer to \"https://acmecorp.com/legal/returns-policy\" for more info"]
```

## reference_url

terms > policies > reference_url

**Description**  
URL linking to the full official policy document or page. Ensures users can access detailed policy info.

**Guideline**  
Use a publicly accessible URL linking directly to the document or page. Avoid query strings, tracking parameters or redirects.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"reference_url": "https://acmecorp.com/legal/returns-policy.pdf"
```

### Incorrect Example

```json
"reference_url": "https://acmecorp.com/legal/returns-policy?sessionId=9834ahD7&tracking=true&click=%20%2B%2F%23fail%3Fimg.pdf&token=abc123!@#&utm_source=%%broken%%"
```

# warranties

terms > warranties

**Description**  
Summarises available warranties, including their scope and duration. Helps users assess protection and coverage.

**Required**  
No

**Expected Type**  
`Array<Object>`

### Correct Example

```json
"reference_url": "https://acmecorp.com/legal/returns-policy.pdf"
```

### Incorrect Example

```json
"reference_url": "https://acmecorp.com/legal/returns-policy?sessionId=9834ahD7&tracking=true&click=%20%2B%2F%23fail%3Fimg.pdf&token=abc123!@#&utm_source=%%broken%%"
```

## overview

terms > warranties > overview

**Description**  
Short, non-binding summary of warranty coverage and terms. Helps users understand protections offered.

**Guideline**  
Use plain text. Avoid legal jargon, vague phrases or full policy text.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"overview": ["2-year coverage for accidental damage"]
```

### Incorrect Example

```json
"overview": ["2-year coverage for accidental damage please see the following documentation for further information https://acmecorp.com/legal/tech-care?sessionId=9834ahD7&tracking=true&click=%20%2B%2F%23fail%3Fimg.pdf&token=abc123!@#&utm_source=%%broken%%"]
```

## reference_url

terms > warranties > reference_url

**Description**  
Link to full warranty documentation or pages. Enables users to review comprehensive warranty terms.

**Guideline**  
Use a publicly accessible URL linking directly to the document or page. Avoid query strings, tracking parameters or redirects.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"reference_url": "https://acmecorp.com/legal/tech-care.pdf"
```

### Incorrect Example

```json
"reference_url": "https://acmecorp.com/legal/tech-care?sessionId=9834ahD7&tracking=true&click=%20%2B%2F%23fail%3Fimg.png&token=abc123!@#&utm_source=%%broken%%"
```

# liability_limit

terms > liability_limit

**Description**  
Maximum amount the seller is liable for under the terms. Ensures clear risk boundaries for the user.

**Guideline**  
Use plain text. Avoid legal jargon, vague phrases or full policy text.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"liability_limit": "£100,000 for property damage or personal injury"
```

### Incorrect Example

```json
"liability_limit": "£100,000 liability limit for property damage please see the following documentation for further information https://acmecorp.com/legal/tech-care?sessionId=9834ahD7&tracking=true&click=%20%2B%2F%23fail%3Fimg.pdf&token=abc123!@#&utm_source=%%broken%%"
```

# insurance_notice

terms > insurance_notice

**Description**  
Information about any required or recommended insurance related to the offer. Helps users understand additional protection needs.

**Guideline**  
Use plain text. Avoid legal jargon, vague phrases or full policy text.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"insurance_notice": "insurance doesn't cover accidental damage"
```

### Incorrect Example

```json
"insurance_notice": "Coverage shall be afforded pursuant to Policy No. 12345 under Sections 4.1-4.7 of the General Terms and Conditions, subject to all exclusions and endorsements therein."
```