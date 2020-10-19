# PlanBee 'V1.1.x' - based on Empire V5.5.2

A running record of the changes I make. The main purpose of this is to leverage the improvements in this latest version of our base theme, and customise it according to best practice.

To ensure that our theme can be updated whenever Pixel Union bring out an updated version of 'Empire', I've changed the way custom code is implemented.

1. Every single piece of custom code is created as a separate snippet. Their names are all prefixed with 'pb-', e.g. 'pb-register-banner.liquid'.
2. Every single piece of custom code will be inserted into the theme's liquid files using 'render', e.g. '{%- render 'pb-register-banner' -%}'.
3. An additional CSS file has been created in the 'assets' folder, 'pb-theme.css'. This handles new CSS classes, IDs and overrides, instead of appending CSS to the main CSS file, 'theme.scss.liquid'.

When the theme is updated, all we need to do is:

1. Check that settings in the new theme's 'customizer' match those of the old theme.
2. Add the custom CSS file to the 'assets' folder.
3. Add the custom code snippets to the 'snippets' folder.
4. Copy over the 'render' references to the custom snippets in the theme's liquid files. These can be quickly found in the old theme by searching for "render 'pb-'".

## Ongoing tasks

Collection sidebar grid. Art is done; use as a reference for other collections.

## Completed tasks

### Customizer

Most theme settings applied. Home page sections still need customising.

### Templates

- Login page
- Register page
- Contact page
- 404 page
- Blog page
- Article page
- Product page (ongoing; slider, title, trustbox product mini and quantity selector are done so far.)

### Assets

- **This** readme
- PlanBee custom CSS file

### Snippets

- pb-404-banner.liquid
- pb-contact-left_column.liquid
- pb-contact-right_column.liquid
- pb-login-foot.liquid
- pb-register-banner.liquid
- pb-register-foot.liquid
- pb-register-subheading.liquid
- pb-theme-old-product-category-canonical.liquid
- pb-author-bios.liquid
- pb-blog-categories-tag-cloud.liquid
- pb-product-image-slider.liquid
- pb-product-mini.liquid
