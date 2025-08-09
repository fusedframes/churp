`ratings`
==========

**Description**  
Structured user-generated evaluations of the offer. Enables analysis of sentiment, satisfaction and real-world usage insights.

**Required**  
No

**Expected Type**  
`Object`

# label

ratings > label

**Description**  
Descriptive title for the specific rating. Helps distinguish different types of scores.

**Guideline**  
Avoid verbose descriptions.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"label": "customer service"
```

### Incorrect Example

```json
"label": "we asked our customers how they viewed our service"
```

# average_value

ratings > average_value

**Description**  
The average score for the rating label. Supports quick summarization of sentiment across reviews.

**Required**  
No

**Expected Type**  
`Number`

### Correct Example

```json
"average_value": 4.2
```

### Incorrect Example

```json
"average_value": "★★★★"
```

# total_count

ratings > total_count

**Description**  
Total volume of individual ratings for the category. Indicates strength of data and rating reliability.

**Guideline**  
Use a positive integer.

**Required**  
No

**Expected Type**  
`Integer`

### Correct Example

```json
"average_value": 4.2
```

### Incorrect Example

```json
"average_value": "★★★★"
```

# score_range

ratings > score_range

**Description**  
Defines the minimum and maximum possible rating values. Enables consistent normalization and comparison across diverse scoring systems.

**Guideline**  
Range using a dash.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"score_range": "0–5"
```

### Incorrect Example

```json
"score_range": "from zero to five stars"
```

# best_score

ratings > best_score

**Description**  
Represents the highest achievable rating within the system. Supports calibration of user scores and ranking logic.

**Guideline**  
Must be within the score range.

**Required**  
No

**Expected Type**  
`Number`

### Correct Example

```json
"best_score": 5
```

### Incorrect Example

```json
"best_score": 7
```

# reviews

ratings > reviews

**Description**  
Detailed narratives and opinions shared by users about their experience with the offer. Provide insights that support deeper understanding of user context.

**Required**  
No

**Expected Type**  
`Array<Object>`

## reviewer

ratings > reviews > reviewer

**Description**  
Name or identifier of the individual who authored the review. Helps contextualize feedback with user attribution.

**Guideline**  
Avoid titles, formatting or special characters.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"reviewer": "Jane D"
```

### Incorrect Example

```json
"reviewer": "@Jane D"
```

## date

ratings > reviews > date

**Description**  
The date the review was submitted. Enables chronological sorting and freshness assessment.

**Guideline**  
Use the ISO 8601 date format. Can be in the future or past.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"date": "2024-12-31"
```

### Incorrect Example

```json
"date": "12/31/2024"
```

## score

ratings > reviews > score

**Description**  
Numeric value representing the reviewer's overall rating. Provides a quantifiable measure of satisfaction.

**Guideline**  
Must be a value within the defined scoring range.

**Required**  
No

**Expected Type**  
`Number`

### Correct Example

```json
"score": 5
```

### Incorrect Example

```json
"score": "★★★★★"
```

## content

ratings > reviews > content

**Description**  
Full text of the review describing user experience. Offers detailed qualitative feedback to inform decisions.

**Required**  
No

**Expected Type**  
`String`

## media

ratings > reviews > media

**Description**  
Associated images or videos attached to the review. Enhances credibility and visual engagement through user-generated content.

**Guideline**  
Use a publicly accessible URL linking directly to a media file. Avoid query strings, tracking parameters or redirects.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"media": ["https://acmecorp.com/cdn/ugc-review-2351.jpg"]
```

### Incorrect Example

```json
"media": ["https://acmecorp.com/cdn/ugc-review-2351?sessionId=9834ahD7&tracking=true&click=%20%2B%2F%23fail%3Fimg.jpg&token=abc123!@#&utm_source=%%broken%%"]
```

# collected_by

ratings > collected_by

**Description**  
Identifies the organization responsible for gathering the review. Enables transparency based on source credibility.

**Guideline**  
Clear name of collecting entity.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"collected_by": "Trustpilot"
```

### Incorrect Example

```json
"collected_by": "Jane D"
```