# Seedance 2.5 Pricing Sources

This file records public source checks for the Seedance 2.5 API pricing tracker.

The goal is to separate confirmed public pricing from monitoring status. If a provider has not publicly listed Seedance 2.5 pricing, the pricing status should remain `not_published`.

Last checked: 2026-06-25

---

## Source Check Summary

| Provider              | Monitoring URL            | API status    | Pricing status | Notes                                                                            |
| --------------------- | ------------------------- | ------------- | -------------- | -------------------------------------------------------------------------------- |
| BytePlus / Volcengine | https://www.byteplus.com/ | Not confirmed | Not published  | Official Seedance 2.5 API pricing has not been recorded in this tracker yet.     |
| OpenRouter            | https://openrouter.ai/    | Not confirmed | Not published  | No public Seedance 2.5 listing or pricing has been recorded in this tracker yet. |
| fal.ai                | https://fal.ai/           | Not confirmed | Not published  | No public Seedance 2.5 listing or pricing has been recorded in this tracker yet. |
| PiAPI                 | https://piapi.ai/         | Not confirmed | Not published  | No public Seedance 2.5 listing or pricing has been recorded in this tracker yet. |
| Kie.ai                | https://kie.ai/           | Not confirmed | Not published  | No public Seedance 2.5 listing or pricing has been recorded in this tracker yet. |
| EvoLink               | https://www.evolink.ai/   | Not confirmed | Not published  | No public Seedance 2.5 listing or pricing has been recorded in this tracker yet. |

---

## Source Rules

A provider should only be marked as having published pricing when the pricing appears on one of the following public source types:

* official documentation
* public pricing page
* public model page
* public API provider documentation
* public changelog or announcement page

Private dashboard screenshots, unverified claims, scraped rumors, and unsupported estimates should not be treated as confirmed pricing.

---

## Pricing Status Rules

| Status                     | Meaning                                                                                                                         |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| `not_published`            | No public Seedance 2.5 pricing has been recorded.                                                                               |
| `starting_price_published` | Provider publishes a starting price or provider-dependent price.                                                                |
| `published`                | Provider publishes a fixed or clearly defined public price.                                                                     |
| `estimated`                | Provider publishes an estimated price, but billing may depend on tokens, credits, resolution, duration, or other usage factors. |

---

## API Status Rules

| Status                  | Meaning                                                                             |
| ----------------------- | ----------------------------------------------------------------------------------- |
| `not_confirmed`         | No public API access confirmation has been recorded.                                |
| `listed_but_unverified` | The model appears in public material, but API access should be verified.            |
| `available`             | Public documentation or provider page indicates API access is available.            |
| `restricted`            | API access may require approval, region access, allowlist, or console verification. |

---

## Baseline Policy

Seedance 2.0 pricing may be used as a temporary budget reference while Seedance 2.5 pricing remains unpublished.

Seedance 2.0 pricing should not be treated as a prediction for Seedance 2.5 pricing.

The live tracker maintains the current baseline table:

https://videoapicost.com/seedance-2-5-pricing

---

## Update Policy

When a new public source is found, update:

1. `data/seedance-2-5-providers.json`
2. this source file
3. `CHANGELOG.md`
4. the live tracker page if the change affects public status or pricing

Each update should include:

* provider name
* source URL
* date checked
* pricing status
* API status
* billing unit if available
* notes on whether the price is fixed, estimated, token-based, credit-based, or provider-dependent
