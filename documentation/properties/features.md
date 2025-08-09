`features`
==========

**Description**  
A collection of distinct characteristics or attributes belonging to the offer. Enables detailed presentation of key aspects to inform and guide user decisions.

**Required**  
No

**Expected Type**  
`Array<Object>`

# name

features > name

**Description**  
Name of the specific characteristic or attribute of the offer. Helps users quickly identify key aspects.

**Guideline**  
Official name or attribute the feature is about.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"name": "battery life"
```

### Incorrect Example

```json
"name": "18 hour battery life"
```

# description

features > description

**Description**  
Provides contextual details that explain or clarify the feature name and value. Enhances user understanding by adding relevant background or usage information.

**Guideline**  
Clear and not verbose context for the name and value.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"description": "average usage time on a single charge"
```

### Incorrect Example

```json
"description": "18 hours average usage time"
```

# value

features > value

**Description**  
Exact measure, type or quantity associated with the feature. Supports clear understanding of the offers capabilities.

**Guideline**  
Only the metric or value associated with the feature.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"value": "18 hours"
```

### Incorrect Example

```json
"value": "battery Life with up to 18 hours of charge available"
```