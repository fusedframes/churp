`documents`
==========

**Description**  
Supporting materials related to the offer. Enables users to access important information for decision-making, compliance or correct usage.

**Required**  
No

**Expected Type**  
`Array<Object>`

# title

documents > title

**Description**  
Lists the title of the document. Enables users to understand what the document refers to.

**Required**  
No

**Expected Type**  
`String`

# overview

documents > overview

**Description**  
Brief non-binding summary of the document's contents. Helps users decide whether to open the document.

**Guideline**  
Concise summary of what it provides.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"overview": "Explains how to get started and use the product safely."
```

### Incorrect Example

```json
"overview": "This comprehensive document thoroughly outlines every feature, technical detail, warranty clause, regulatory note, troubleshooting step, and historical background necessary for complete mastery of the product in any conceivable scenario."
```

# intent

documents > intent

**Description**  
Defines the primary purpose or role of the document within the offer. Enables targeted retrieval of relevant documents.

**Guideline**  
Use clear action phrases. Clearly list the intended purpose.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"intent": ["how to setup"]
```

### Incorrect Example

```json
"intent": ["user manual"]
```

# file_url

documents > file_url

**Description**  
Direct link to the hosted document file. Enables users to easily access official documentation.

**Guideline**  
Use a publicly accessible URL linking directly to the document. Avoid query strings, tracking parameters or redirects.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"file_url": "https://acmecorp.com/guides/user-manual.pdf"
```

### Incorrect Example

```json
"file_url": "https://acmecorp.com/guides/user-manual?sessionId=9834ahD7&tracking=true&click=%20%2B%2F%23fail%3Fimg.png&token=abc123!@#&utm_source=%%broken%%"
```

# language

documents > language

**Description**  
Indicates the language the document is written in. Enables correct localisation and accessibility for users.

**Guideline**  
Use the ISO 639-1 codes, optionally combined with ISO 3166 country codes to indicate regional language use.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"language": ["en-us"]
```

### Incorrect Example

```json
"language": ["english-us"]
```