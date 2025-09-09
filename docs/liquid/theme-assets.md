# Theme Assets

---
  The assets directory is rendered as the assets folder in the theme editor. It
  contains all the assets used in the theme, including fonts, images,
  stylesheets, and JavaScript files.
---

## asset\_url

The `asset_url` return the URL of a file in the "assets" folder of a theme.

```
{{ 'styles.scss.css' | asset_url | stylesheet_tag }}

<link rel="stylesheet" type="text/css" media="all" href="https://shopcada.g.shopcadacdn.com/sites/files/shopcada/assets/02f74a2392b447815187efaab3bc5041_styles.scss.css">
```

## global\_asset\_url

The `global_asset_url` returns the URL of a global asset. Global assets are kept in a directory on Shopcada servers. Using global assets can improve the load times of your pages.

The `asset_url` return the URL of a file in the "assets" folder of a theme.

```
{{ 'assets/js/user.js' | global_asset_url | script_tag }}

<script type="text/javascript" src="https://shopcada.g.shopcadacdn.com/assets/js/user.js?67">&#x3C;/script>
```
