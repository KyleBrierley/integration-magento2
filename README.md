# Tealium Magento 2 Integration

Historical Magento 2 module for deploying Tealium tags and page-level universal data objects across an ecommerce storefront.

This repository is the stronger public Tealium/Magento artifact and should be treated as the canonical legacy Magento 2 integration. It shows a real module structure, admin configuration, layout integration, data-layer templates, and Tealium tag rendering for common ecommerce page types.

## What This Demonstrates

- Magento 2 module architecture.
- Admin configuration for Tealium account, profile, and environment settings.
- Page-level data-layer deployment through universal data objects.
- Frontend layout XML coverage for catalog, product, checkout, customer, CMS, search, and sales pages.
- Enterprise partner/ecommerce integration work for a customer-data platform.

## Module Coverage

The extension includes layout hooks and templates for flows such as:

- Global storefront pages.
- Catalog category and product detail pages.
- Search result pages.
- Cart, checkout, and order success pages.
- Customer account pages.
- Guest sales, invoice, shipment, and credit memo pages.

## Installation

### Magento Marketplace

The original extension was distributed through Magento Marketplace:

https://marketplace.magento.com/tealium-tags.html

### Manual Install

Copy the `Tealium` folder into `app/code` within a Magento installation. If `app/code` does not exist, create it.

Then run:

```bash
sudo php bin/magento setup:upgrade
sudo php -d set_time_limit=3600 -d memory_limit=1024M bin/magento setup:di:compile
```

## Configuration

In the Magento admin panel, go to `Stores -> Configuration -> Tealium -> Tags`.

Configure:

- Extension enabled/disabled state.
- Tealium iQ account.
- Tealium iQ profile.
- Tealium environment.

## Data-Layer Context

The extension uses Tealium universal data objects as the page-level contract between Magento and Tealium iQ. Tealium's data-layer concepts are documented here:

https://community.tealiumiq.com/t5/Getting-Started/Getting-Started-with-The-Data-Layer/ta-p/9503

## Repository Status

This is a legacy Magento 2 integration and should not be evaluated as a current Magento/PHP package without dependency and compatibility review. Its portfolio value is the enterprise integration pattern: packaging a customer-data platform into a commerce ecosystem with admin configuration, data-layer scaffolding, and page-specific implementation points.

## Change Log

- `1.0.1` release
  - Default UDO (`utag_data` JSON object in page source) deployed via Magento extension to match the Tealium iQ TMS Data Layer bundle.
  - Account/profile/environment configuration in Magento admin.
  - Extensible UDO support for customization.

## License

Use of this software is subject to the terms and conditions of the license agreement contained in `LICENSE.txt`.

Copyright (C) 2012-2018, Tealium Inc.
