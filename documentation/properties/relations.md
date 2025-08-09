`relations`
=======

**Description**  
Defines how this offer relates to other offers. Enables intelligent recommendations and validation of required or optional items.

**Required**  
No

**Expected Type**  
`Object`

# often_bought_with

relations > often_bought_with

**Description**  
Specifies offers frequently purchased alongside this offer. Helps drive relevant cross-selling suggestions.

**Required**  
No

**Expected Type**  
`Array<Object>`

## offer_name

relations > often_bought_with > offer_name

**Description**  
Name of an offer frequently purchased alongside this one. Helps surface commonly paired items.

**Guideline**  
Use the offer name.

**Required**  
No

**Expected Type**  
`String`

## offer_url

relations > often_bought_with > offer_url

**Description**  
Direct link to the related offer. Supports quick access to complementary items.

**Guideline**  
Use a publicly accessible URL linking directly to the offer. Avoid query strings, tracking parameters or redirects.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"offer_url": "https://store.acme.com/products/x-battery-pack"
```

### Incorrect Example

```json
"offer_url": "https://store.acme.com/products/x-battery-pack?sessionId=9834ahD7&tracking=true&click=%20%2B%2F%23fail%3&token=abc123!@#&utm_source=%%broken%%"
```

## stock_state

relations > often_bought_with > stock_state

**Description**  
Indicates the current availability of the suggested product. Enables dynamic display based on stock status.

**Guideline**  
Use the enumerated values.

**Enumerated Values**  
in_stock — Item or service is readily available  
low_stock — Limited quantity remaining  
out_of_stock — Currently unavailable  
backorder — Can be ordered for later fulfilment  
by_request — Availability confirmed upon inquiry  
preorder — Available to order before first fulfillment  
notify_when_in_stock — Currently unavailable and can be alerted when available  
discontinued — No longer supplied  

**Required**  
No

**Expected Type**  
`String`

# requires

relations > requires

**Description**  
Lists other offers that must be obtained to use this offer as intended. Enables transparency of dependencies before purchase.

**Required**  
No

**Expected Type**  
`Array<Object>`

## offer_name

relations > requires > offer_name

**Description**  
Name of an offer that is needed for this offer to function properly. Makes dependencies clear to users.

**Guideline**  
Use the offer name.

**Required**  
No

**Expected Type**  
`String`

## offer_url

relations > requires > offer_url

**Description**  
Public link to the required offer. Enables users to quickly view or purchase the necessary offer.

**Guideline**  
Use a publicly accessible URL linking directly to the offer. Avoid query strings, tracking parameters or redirects.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"offer_url": "https://store.acme.com/products/x-battery-pack"
```

### Incorrect Example

```json
"offer_url": "https://store.acme.com/products/x-battery-pack?sessionId=9834ahD7&tracking=true&click=%20%2B%2F%23fail%3&token=abc123!@#&utm_source=%%broken%%"
```

## stock_state

relations > requires > stock_state

**Description**  
Shows whether the required product is currently in stock. Enables validation of dependencies before purchase.

**Guideline**  
Use the enumerated values.

**Enumerated Values**  
in_stock — Item or service is readily available  
low_stock — Limited quantity remaining  
out_of_stock — Currently unavailable  
backorder — Can be ordered for later fulfilment  
by_request — Availability confirmed upon inquiry  
preorder — Available to order before first fulfillment  
notify_when_in_stock — Currently unavailable and can be alerted when available  
discontinued — No longer supplied  

**Required**  
No

**Expected Type**  
`String`

# compatible_with

relations > compatible_with

**Description**  
Specifies other offers known to work well with this offer. Enables relevant add-on discovery.

**Required**  
No

**Expected Type**  
`Array<Object>`

## offer_name

relations > compatible_with > offer_name

**Description**  
Name of an offer known to work with this one. Helps users identify compatible accessories or extensions.

**Guideline**  
Use the offer name.

**Required**  
No

**Expected Type**  
`String`

## offer_url

relations > compatible_with > offer_url

**Description**  
Direct URL to the compatible offer. Aids in exploring options that integrate well with the current offer.

**Guideline**  
Use a publicly accessible URL linking directly to the offer. Avoid query strings, tracking parameters or redirects.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"offer_url": "https://store.acme.com/products/x-battery-pack"
```

### Incorrect Example

```json
"offer_url": "https://store.acme.com/products/x-battery-pack?sessionId=9834ahD7&tracking=true&click=%20%2B%2F%23fail%3&token=abc123!@#&utm_source=%%broken%%"
```

## stock_state

relations > compatible_with > stock_state

**Description**  
Reflects the availability of the offer. Supports compatibility guidance based on real-time stock levels.

**Guideline**  
Use the enumerated values.

**Enumerated Values**  
in_stock — Item or service is readily available  
low_stock — Limited quantity remaining  
out_of_stock — Currently unavailable  
backorder — Can be ordered for later fulfilment  
by_request — Availability confirmed upon inquiry  
preorder — Available to order before first fulfillment  
notify_when_in_stock — Currently unavailable and can be alerted when available  
discontinued — No longer supplied  

**Required**  
No

**Expected Type**  
`String`

# fallbacks

relations > fallbacks

**Description**  
Defines alternative options if the primary offer is unavailable or not suitable. Supports flexible substitutions and inventory-based recommendations.

**Required**  
No

**Expected Type**  
`Array<Object>`

## offer_name

relations > fallbacks > offer_name

**Description**  
Alternative offer that can be provided if the main item is unavailable. Helps preserve user intent by suggesting substitutes.

**Guideline**  
Use the offer name.

**Required**  
No

**Expected Type**  
`String`

## offer_url

relations > fallbacks > offer_url

**Description**  
URL pointing to the fallback product. Facilitates quick access to suitable replacements.

**Guideline**  
Use a publicly accessible URL linking directly to the offer. Avoid query strings, tracking parameters or redirects.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"offer_url": "https://store.acme.com/products/x-battery-pack"
```

### Incorrect Example

```json
"offer_url": "https://store.acme.com/products/x-battery-pack?sessionId=9834ahD7&tracking=true&click=%20%2B%2F%23fail%3&token=abc123!@#&utm_source=%%broken%%"
```

## stock_state

relations > fallbacks > stock_state

**Description**  
Indicates the current availability status of the fallback item. Helps prioritise fallback options that are immediately in stock or soon available.

**Guideline**  
Use the enumerated values.

**Enumerated Values**  
in_stock — Item or service is readily available  
low_stock — Limited quantity remaining  
out_of_stock — Currently unavailable  
backorder — Can be ordered for later fulfilment  
by_request — Availability confirmed upon inquiry  
preorder — Available to order before first fulfillment  
notify_when_in_stock — Currently unavailable and can be alerted when available  
discontinued — No longer supplied  

**Required**  
No

**Expected Type**  
`String`

# upsells

relations > upsells

**Description**  
Highlights upgraded or premium alternatives to the current item. Enables guided selling to higher-value options and supports inventory-based recommendations.

**Required**  
No

**Expected Type**  
`Array<Object>`

## offer_name

relations > upsells > offer_name

**Description**  
More advanced or premium offer recommended in place of the current one. Supports increase feature alternatives, while enabling the provider to increase sales.

**Guideline**  
Use the offer name.

**Required**  
No

**Expected Type**  
`String`

## offer_url

relations > upsells > offer_url

**Description**  
Link to the higher-tier version of the offer. Helps users explore more advanced options easily.

**Guideline**  
Use a publicly accessible URL linking directly to the offer. Avoid query strings, tracking parameters or redirects.

**Required**  
No

**Expected Type**  
`String`

### Correct Example

```json
"offer_url": "https://store.acme.com/products/x-battery-pack"
```

### Incorrect Example

```json
"offer_url": "https://store.acme.com/products/x-battery-pack?sessionId=9834ahD7&tracking=true&click=%20%2B%2F%23fail%3&token=abc123!@#&utm_source=%%broken%%"
```

## stock_state

relations > upsells > stock_state

**Description**  
Represents the availability status of the suggested upsell item. Ensures upsell recommendations are relevant and purchasable at time of decision.

**Guideline**  
Use the enumerated values.

**Enumerated Values**  
in_stock — Item or service is readily available  
low_stock — Limited quantity remaining  
out_of_stock — Currently unavailable  
backorder — Can be ordered for later fulfilment  
by_request — Availability confirmed upon inquiry  
preorder — Available to order before first fulfillment  
notify_when_in_stock — Currently unavailable and can be alerted when available  
discontinued — No longer supplied  

**Required**  
No

**Expected Type**  
`String`