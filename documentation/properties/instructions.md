`instructions`
==========

**Description**  
Provides guidance on how to use, assemble, or care for the product. Enables users to understand proper handling and operation procedures.

**Required**  
No

**Expected Type**  
`Array<Object>`

# care

instructions > care

**Description**  
Routine upkeep instructions for the offer. Helps preserve the offer over time.

**Guideline**  
Use present-tense instructions. Avoid vague or generic phrases.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"care": ["do not tumble dry"]
```

### Incorrect Example

```json
"care": ["don't break it"]
```

# setup

instructions > setup

**Description**  
Initial preparation steps to make the offer ready for use. Ensures proper configuration, assembly or activation.

**Guideline**  
Use present-tense instructions in a logical order. Avoid vague or generic phrases.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"setup": ["charge for 2 hours before use"]
```

### Incorrect Example

```json
"setup": ["configure it"]
```

# disposal

instructions > disposal

**Description**  
Guidelines for safely discarding or recycling the offer after use. Supports environmental responsibility and compliance.

**Guideline**  
Use specific disposal or recycling methods. Avoid generic throwaway phrasing.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"disposal": ["recycle at electronics center"]
```

### Incorrect Example

```json
"disposal": ["throw away"]
```

# warnings

instructions > warnings

**Description**  
Safety alerts and cautionary statements. Helps prevent harm, misuse or regulatory violations.

**Guideline**  
Use present tense. Avoid vague or non-informative alerts.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"warnings": ["do not use indoors"]
```

### Incorrect Example

```json
"warnings": ["indoor use maybe not best"]
```

# usage

instructions > usage

**Description**  
Instructions describing how the offer should be used. Ensures correct and safe operation in line with its intended function.

**Guideline**  
Use clear present-tense instructions. Avoid vague, passive or uncertain phrasing.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"usage": ["apply a thin layer to clean facial skin every morning and evening"]
```

### Incorrect Example

```json
"usage": ["this product is great for your face"]
```