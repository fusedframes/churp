`ux_preference`
==========

**Description**  
Specifies stylistic preferences that guide how the offer is visually and tonally presented. Enables consistent alignment with brand and offer style.

**Required**  
No

**Expected Type**  
`Object`

# tone

ux_preference > tone

**Description**  
Specifies the intended stylistic or emotional character to guide presentation. Supports consistent alignment with brand positioning.

**Guideline**  
Avoid evaluative or subjective terms. Must express style, not value.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"tone": "premium"
```

### Incorrect Example

```json
"tone": "expensive"
```

# layout

ux_preference > layout

**Description**  
Suggests a specific visual structure for presenting options when default behaviour may not suffice. Used to guide display of complex or layered choices.

**Guideline**  
Use the enumerated values.

**Enumerated Values**  
modifiers_table — Shows selectable options in a structured table  
modifiers_multi_step — Guides user through each modifier  

**Required**  
No

**Expected Type**  
`String`

# brand_color

ux_preference > brand_color

**Description**  
Defines the highlight visual colour for aligning the UI with brand identity. Allows for visual consistency across experiences.

**Guideline**  
Exposed colour value in either hex or RGB format.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"brand_color": "#FF5733"
```

### Incorrect Example

```json
"brand_color": "Orange"
```