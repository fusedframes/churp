General Authoring Guidelines
============================

This file defines clear, technical guidelines on the language, capitalisation and punctuation conventions to follow when writing Churp schema data. Following these guidelines ensures consistency and accurate parsing by AI systems.

## Language

### Properties and Enumerated Values

All schema property names and enumerated values must be written consistently in American English. These values should not be translated, altered or localised.

**Correct Example:**

```json
{
  "@context": "https://www.churp.dev/context/v1.0.json",
  "offer": {
    "name": "Pen USB 2.0 64GB",
    "quantity": 1
  },
  "value": {
    "base_price": "€15,00",
    "price_including_tax": true
  },
  "seller": {
    "entity_name": "Acme & Co Lda"
  }
}
```

**Incorrect Example:**

```json
{
  "@contexto": "https://www.churp.dev/context/v1.0.json",
  "oferta": {
    "nome": "Pen USB 2.0 64GB",
    "quantidade": 1
  },
  "valor": {
    "preco_base": "€15,00",
    "preco_inclui_imposto": true
  },
  "vendedor": {
    "nome_entidade": "Acme & Co Lda"
  }
}
```

### Free-Text Values

All schema free-text values should be written in the primary language of the webpage's audience. Don't mix multiple languages in a single Churp schema.

If language localisation isn't possible, these fields must be provided clearly in American English.

```json
{
  "@context": "https://www.churp.dev/context/v1.0.json",
  "offer": {
    "name": "Wireless Bluetooth Speaker",
    "quantity": 1
  },
  "value": {
    "base_price": "$49.99",
    "price_including_tax": true
  },
  "features": [
    {
      "name": "Battery Life",
      "description": "Average usage time on a single charge",
      "value": "18 hours"
    },
    {
      "name": "Water Resistance",
      "description": "Protects against splashes and light rain",
      "value": "IPX5"
    }
  ],
  "seller": {
    "entity_name": "Acme Audio Inc"
  }
}
```

```json
{
  "@context": "https://www.churp.dev/context/v1.0.json",
  "offer": {
    "name": "Wireless Bluetooth Speaker",
    "quantity": 1
  },
  "value": {
    "base_price": "$49.99",
    "price_including_tax": true
  },
  "features": [
    {
      "name": "Battery Life",
      "description": "Average usage time on a single charge",
      "value": "18 hours"
    },
    {
      "name": "Resistência à água",
      "description": "Protege contra salpicos e chuva leve",
      "value": "IPX5"
    }
  ],
  "seller": {
    "entity_name": "Acme Audio Inc"
  }
}
```

## Capitalisation & Punctuation

### Sentence Case

Use sentence case, capitalising only the first letter of the first word, for all descriptive text values such as description, insurance_notice and instructions.

### Title Case

Use title case, capitalising the first letter of each major word, exclusively for fields representing titles or labels such as name or title.

### Lower Case

Use lower case exclusively for short labels like intent. Avoid any capitalisation in these cases.

### Full Stops

Use full stops only when the field value is a complete sentence or paragraph like insurance_notice or description. Omit full stops for short phrases or single-word labels.