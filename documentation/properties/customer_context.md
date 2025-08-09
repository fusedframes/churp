`customer_context`
==========

**Description**  
Collection of customer context information related to the offer. Enables users to understand customer requirements and relevant context.

**Required**  
No

**Expected Type**  
`Object`

# recommend_if

customer_context > recommend_if

**Description**  
Provides context to help users assess whether the offer fits their needs. Supports clearer expectations and better decision-making.

**Guideline**  
Clear condition where the offer is well-suited.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"recommend_if": ["Infant aged 6+ months and ready to be introduced to solids"]
```

### Incorrect Example

```json
"recommend_if": ["For babies"]
```

# not_recommended_if

customer_context > not_recommended_if

**Description**  
Specifies when the offer may be unsuitable. Enables transparency and reduces likelihood of poor fit.

**Guideline**  
Clear condition that highlights incompatibility.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"not_recommended_if": ["Has a soy or dairy intolerance"]
```

### Incorrect Example

```json
"not_recommended_if": ["Not suitable for some allergies"]
```

# not_recommended_if

customer_context > not_recommended_if

**Description**  
Specifies when the offer may be unsuitable. Enables transparency and reduces likelihood of poor fit.

**Guideline**  
Clear condition that highlights incompatibility.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"not_recommended_if": ["Has a soy or dairy intolerance"]
```

### Incorrect Example

```json
"not_recommended_if": ["Not suitable for some allergies"]
```

# ideal_conditions

customer_context > ideal_conditions

**Description**  
Specifies the circumstances in which the offer performs best. Helps guide appropriate use and manage user expectations.

**Guideline**  
Avoid generalisations or vague conditions.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"ideal_conditions": ["Refrigerated storage between 2–6°C "]
```

### Incorrect Example

```json
"ideal_conditions": ["Refrigerated storage"]
```

# problem_it_solves

customer_context > problem_it_solves

**Description**  
Clarifies the challenge the offer addresses. Helps align users need with the offer.

**Guideline**  
Focus on the problem the offer addresses, not the solution.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"problem_it_solves": ["Difficulty falling asleep"]
```

### Incorrect Example

```json
"problem_it_solves": ["Allows you to fall asleep fast"]
```

# learning_curve

customer_context > learning_curve

**Description**  
Describes the level of experience required to effectively use the offer. Helps set expectations around user skill requirements.

**Guideline**  
Use the enumerated values.

**Enumerated Values**  
none — No learning needed  
easy — Very simple to learn  
moderate — Takes some practice  
hard — Needs a lot of learning  
expert — For advanced users only  

**Required**  
No

**Expected Type**  
`String`

# frequently_asked

customer_context > frequently_asked

**Description**  
Lists common questions and answers related to the offer. Helps address typical user concerns and improve understanding.

**Required**  
No

**Expected Type**  
`Array<Object>`

## question

customer_context > problem_it_solves > question

**Description**  
Concise text stating a common inquiry about the offer. Supports understanding by anticipating majority of user questions.

**Guideline**  
Use a direct question.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"question": "How does this product help with falling asleep"
```

### Incorrect Example

```json
"question": "Product details"
```

## answer

customer_context > problem_it_solves > answer

**Description**  
Informative response addressing the related question. Provides clear and relevant information to users.

**Guideline**  
Provide concise and factual responses.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"answer": "It uses natural herbs combined with melatonin, which has been scientifically proven to reduce the time needed to fall asleep"
```

### Incorrect Example

```json
"answer": "This product helps improve sleep quality because it contains natural ingredients that work well for most people and makes falling asleep easier"
```

# gender

customer_context > problem_it_solves > gender

**Description**  
Indicates the intended gender relevance of the offer. Supports better personalisation and inclusive representation in recommendations and presentation.

**Guideline**  
Recognisable gender term.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"gender": "female"
```

### Incorrect Example

```json
"gender": "for females"
```

# age-range

customer_context > problem_it_solves > age-range

**Description**  
Defines the age suitability range for the offer. Assists in relevance and appropriateness. To be used for general guidance only. For compliance and age-restrictions use minimum_age_required.

**Guideline**  
Simple range or threshold.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"age-range": "18–65"
```

### Incorrect Example

```json
"age-range": "adults"
```