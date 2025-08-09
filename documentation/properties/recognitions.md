`recognitions`
==========

**Description**  
Official acknowledgments or certifications related to the offer. Enables users to verify legitimacy and compliance with standards.

**Required**  
No

**Expected Type**  
`Array<Object>`

# title

recognitions > title

**Description**  
Name of the recognition or certification. Helps users identify the specific credential awarded.

**Guideline**  
Official name of the recognition or certification.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"title": "FDA Approval"
```

### Incorrect Example

```json
"title": "Approved"
```

# title

recognitions > title

**Description**  
Name of the recognition or certification. Helps users identify the specific credential awarded.

**Guideline**  
Official name of the recognition or certification.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"title": "FDA Approval"
```

### Incorrect Example

```json
"title": "Approved"
```

# type

recognitions > type

**Description**  
Category or classification of the recognition. Supports clear understanding of the recognition's purpose or domain.

**Guideline**  
Specific classification of recognition.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"type": "certification"
```

### Incorrect Example

```json
"type": "FDA Certification"
```

# issuing_body

recognitions > issuing_body

**Description**  
Name of the authoritative organization granting the recognition. Provides credibility and context for trust.

**Guideline**  
Full formal name of the organization granting the recognition.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"issuing_body": "U.S. Food and Drug Administration"
```

### Incorrect Example

```json
"issuing_body": "health agency"
```

# summary

recognitions > summary

**Description**  
Brief non-binding explanation of the recognition's scope and significance. Helps users grasp its relevance without legal complexity.

**Guideline**  
Clear summary of what the recognition covers.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"summary": "FDA approved for safe use as a medical device"
```

### Incorrect Example

```json
"summary": "approved"
```

# proof

recognitions > proof

**Description**  
URL linking directly to official documentation or evidence supporting the recognition. Ensures users can verify details and authenticity.

**Guideline**  
Publicly accessible URL linking directly to official recognition documents. Avoid indirect links, redirects, query strings, or non-official sources.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"proof": "https://www.fda.gov/downloads/acme-ultra.pdf"
```

### Incorrect Example

```json
"proof": "https://www.fda.gov/downloads/acme-ultra.pdf?sessionId=9834ahD7&tracking=true&click=%20%2B%2F%23fail%3&token=abc123!@#&utm_source=%%broken%%"
```