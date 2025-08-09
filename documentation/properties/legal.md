`legal`
==========

**Description**  
Collection of legal terms related to the offer. Enables users to understand compliance requirements and relevant legal context.

**Required**  
No

**Expected Type**  
`Array<Object>`

# title

legal > title

**Description**  
Official title of the legal document. Helps users quickly identify and differentiate between multiple legal texts associated with the offer.

**Guideline**  
Use the official or commonly recognized title of the document. Avoid vague or overly broad terms.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"title": "data protection policy"
```

### Incorrect Example

```json
"title": "policy about data"
```

# summary

legal > summary

**Description**  
Non-binding overview of the legal information relevant to the offer. Helps users quickly grasp essential legal conditions.

**Guideline**  
Use plain text. Avoid legal jargon, vague phrases or full policy text.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"summary": ["users must be 18 or older"]
```

### Incorrect Example

```json
"summary": ["this document includes all terms and conditions related to product use"]
```

# reference_url

legal > reference_url

**Description**  
Direct URL to the official legal document or regulation referenced. Ensures users can verify detailed legal information.

**Guideline**  
Use a publicly accessible URL linking directly to the official legal document or regulation. Avoid redirects, query strings or tracking parameters.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"reference_url": "https://www.acmecorp.com/legal/privacy-policy.pdf"
```

### Incorrect Example

```json
"reference_url": "https://acmecorp.com/legal/privacy-policy.pdf?id=123&session=abc&track=true"
```

# jurisdictions

legal > jurisdictions

**Description**  
List of countries or regions where the legal terms apply. Supports accurate enforcement and compliance by location.

**Guideline**  
Use the ISO 3166 short name.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"jurisdictions": ["Netherlands"]
```

### Incorrect Example

```json
"jurisdictions": ["NL"]
```