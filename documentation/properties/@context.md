`@context`
=======

**Description**  
The official Churp context file. Provides machine-readable definitions for all properties used in the data.

**Guideline**  
Must be a valid URL that links directly to the official Churp context file. Make sure this URL references the same version of the schema used in your data.

**Required**  
Yes

**Expected Type**  
`String`

### Correct Example

```json
"@context": "https://www.churp.dev/context/v1.0.json"
```

### Incorrect Example

```json
"@context": "v1.0"
```