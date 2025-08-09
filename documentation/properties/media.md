`media`
=======

**Description**  
Specifies visual assets associated with the offer. Supports better understanding, engagement and representation.

**Required**  
No

**Expected Type**  
`Array<Object>`

# source

media > source

**Description**  
Specifies visual content related to the offer. Provides better representation and user understanding through media.

**Guideline**  
Use a publicly accessible URL linking directly to a media file. Avoid query strings, tracking parameters or redirects.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"source": "https://acmecorp.com/cdn/studio-speakers-front.jpg"
```

### Incorrect Example

```json
"source": "https://acmecorp.com/cdn/studio-speakers-front?sessionId=9834ahD7&tracking=true&click=%20%2B%2F%23fail%3Fimg.png&token=abc123!@#&utm_source=%%broken%%"
```

# position_preference

media > position_preference

**Description**  
Indicates the preferred sequence in which media assets should appear. Enables control over visual displays.

**Guideline**  
Use a positive integer, where 1 represents the first position.

**Required**  
No

**Expected Type**  
`Integer`

### Correct Example

```json
"position_preference": 1
```

### Incorrect Example

```json
"position_preference": "first"
```

# position_preference

media > position_preference

**Description**  
Indicates the preferred sequence in which media assets should appear. Enables control over visual displays.

**Guideline**  
Use a positive integer, where 1 represents the first position.

**Required**  
No

**Expected Type**  
`Integer`

### Correct Example

```json
"position_preference": 1
```

### Incorrect Example

```json
"position_preference": "first"
```

# description

media > description

**Description**  
Describes the content of the media asset. Enables understanding to support presentation of the offer.

**Guideline**  
Concise text conveying the image context. Include only essential details, without unnecessary fillers.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"description": "Acme Monogram Cricket Bat held by batsman striking ball on grass pitch"
```

### Incorrect Example

```json
"description": "A photo of a famous batsman gracefully swinging the red-and-gold cricket bat on a lush pitch during a glorious summer afternoon."
```