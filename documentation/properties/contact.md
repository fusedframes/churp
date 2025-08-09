`contact`
==========

**Description**  
A list of ways users can reach the provider or support team. Enables appropriate routing and visibility of available channels.

**Required**  
No

**Expected Type**  
`Array<Object>`

# method

contact > method

**Description**  
Specifies one or more contact methods available to users. Enables intent linked options for communication.

**Guideline**  
Use a clear and recognisable action.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"method": "phone"
```

### Incorrect Example

```json
"method": "on-demand phone line"
```

# handle

contact > handle

**Description**  
The detail needed to reach the specified method, such as a phone number or email address. Enables straightforward access through the selected communication channel.

**Guideline**  
Plain text without protocols or HTML. Can be a URL if applicable. Include necessary prefixes for phone numbers.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"handle": "support@acmecorp.com"
```

### Incorrect Example

```json
"handle": "mailto:support@acmecorp.com"
```

# hours

contact > hours

**Description**  
Defines the time of day when the contact method is available or monitored. Enables clear visibility into when communication is actively provided.

**Guideline**  
HH:MM-HH:MM in 24-hour format.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"hours": "09:00-18:00"
```

### Incorrect Example

```json
"hours": "9 to 6"
```

# timezone

contact > timezone

**Description**  
Indicates the time zone used to interpret the specified contact hours. Enables accurate alignment of user expectations based on local operating times.

**Guideline**  
Standard time zone abbreviation or IANA name.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"timezone": "GMT"
```

### Incorrect Example

```json
"timezone": "UK time"
```

# days

contact > days

**Description**  
Lists the specific days of the week when the contact method is operational. Enables accurate display of availability windows.

**Guideline**  
Use full day names with no abbreviations.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"days": ["monday"]
```

### Incorrect Example

```json
"days": ["monday-friday"]
```

# intent

contact > intent

**Description**  
Specifies the reasons or service categories the contact method supports. Enables intelligent routing and more relevant responses to user queries.

**Guideline**  
Use clear labels that aren't too verbose.

**Required**  
No

**Expected Type**  
`Array<String>`

### Correct Example

```json
"intent": ["returns"]
```

### Incorrect Example

```json
"intent": ["to ask about returns"]
```