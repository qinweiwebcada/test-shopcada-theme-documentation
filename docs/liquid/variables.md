# Liquid Variables

Liquid is an open-source template language created by Shopify and written in Ruby. It is the backbone of Shopcada themes and is used to load dynamic content on storefronts.

Liquid uses a combination of **tags**, **objects**, and **filters** to load dynamic content. They are used inside Liquid template files, which are a group of files that make up a theme.

## Object

**Objects** contain the content that Liquid displays on a page. Objects and variables are displayed when enclosed in double curly braces: `{{` and `}}`.

```
{{ page.title }} // About Us
```

## Tags

**Tags** create the logic and control flow for templates. The curly brace percentage delimiters `{%` and `%}` and the text that they surround do not produce any visible output when the template is rendered. This is used to assign variables and create conditions or loops without showing any of the Liquid logic on the page.

```
{% if customer %}
  Hello {{ customer.name }}!
{% endif %}

// Hello Admin!
```

## Filters

**Filters** change the output of a Liquid object or variable. They are used within double curly braces `{{ }}` and variable assignment, and are separated by a pipe character `|`.

```
{{ "Hello" | append: " Admin!" }} // Hello Admin!
```



Multiple filters can be used on one output, and are applied from left to right.

```
{{ "Hello" | append: " Admin!" | upcase }} // HELLO ADMIN!
```

