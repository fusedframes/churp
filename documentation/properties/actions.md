`actions`
=======

**Description**  
Defines interactive elements associated with the offer. Enables users to initiate tasks, navigate to destinations or perform key operations relating to the offer.

**Required**  
No

**Expected Type**  
`Array<Object>`

# label

actions > label

**Description**  
Descriptive text displayed to users for the action. Enables quick recognition and encourages engagement through clear action orientated language.

**Guideline**  
Use a clear call to action.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"label": "Buy now"
```

### Incorrect Example

```json
"label": "Click this button to make a purchase"
```

# target

actions > target

**Description**  
URL that initiates or directs the user to perform the action. Enables the user to easily complete the intended task.

**Guideline**  
Use a publicly accessible URL linking directly to the action target. Avoid query strings, tracking parameters or redirects. Ensure the URL performs the intended action.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"target": "https://example.com/cart/product/103582406"
```

### Incorrect Example

```json
"target": "https://example.com/cart/product/103582406?sessionId=9834ahD7&tracking=true&click=%20%2B%2F%23fail%3Fimg.jpg&token=abc123!@#&utm_source=%%broken%%"
```

# intent

actions > intent

**Description**  
Summary describing the intended user action or outcome. Provides clear, concise insight into what the action accomplishes or offers.

**Guideline**  
Clear description of what the action provides for the user.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"intent": "User wants to go straight to checkout"
```

### Incorrect Example

```json
"intent": "Purchase"
```