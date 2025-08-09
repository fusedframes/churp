Implementation
==============

This file outlines how to implement Churp correctly on your website. It covers where the data should be placed, how it should be delivered and the technical requirements to ensure it's reliably detected and interpreted by AI systems.

## Placement

Your Churp schema must always be included at the start of the <body> section of each individual product or service webpage. This ensures that AI systems can reliably discover, parse and use the Churp schema.

## Occurrence

Each product or service page should contain exactly one <script type="application/ld+json"> block in the <body>. Including multiple Churp blocks per page may cause confusion or unexpected AI behaviour.

## Type

The Churp data block must use type="application/ld+json". This helps AI systems and tools correctly identify and extract Churp content from the page.

```HTML
<script type="application/ld+json">
{
  "@context": "https://www.churp.dev/context/v1.0.json",
  "offer": {
    "name": "Eco Water Bottle",
    "quantity": 1
  },
  "value": {
    "base_price": "$20.00"
  },
  "seller": {
    "entity_name": "Green Goods Ltd"
  }
}
</script>
```

## Visibility

Churp must be included in the initial HTML payload. It should not be injected dynamically after page load, or hidden behind consent banners, lazy loaders or user interactions. AI systems may not detect Churp content that isn't included in the initial page load.

## Consistency

The Churp data must clearly and accurately represent the primary product or service featured on the webpage. The values should align with how the product or service is presented, while following Churp's guidelines.

## Rendering

Churp data must be rendered server-side to ensure it is included in the initial HTML response. This allows AI systems to detect and process the data immediately, without relying on client-side JavaScript. Many AI crawlers and language models do not execute scripts or wait for dynamic content to load, meaning any Churp data rendered client-side may be completely missed.

## Multi-Language Handling

If your website supports multiple languages, Churp data should be embedded individually per language-specific page. Each localised page should contain a Churp block matching the visible language.

**Example:**

/us/product: Churp block entirely in American English.
/pt/product: Churp block with values in Portuguese, but schema properties and enumerated values in American English.