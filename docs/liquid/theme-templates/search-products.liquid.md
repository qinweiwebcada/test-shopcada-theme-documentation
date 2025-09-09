# search-products.liquid

---

search-products.liquid is used when customers search for certain product keywords, the layout is similar to products.liquid.

---

## Layout

![Search Products](<../../assets/images/documents/image (42).png>)

## Available Liquid Variables

#### 1. Products

[products](liquid/variables/products.md)

```
{{ products }}
```

#### 2. Tag

[term](liquid/variables/pages/term.md)

```
{{ tag }}
{{ tag.description_top }}
{{ tag.description_bottom }}
```

#### 3. Categories

```
{% categories %}
    {{ current_category }}
    {{ categories }}
    {{ is_deepest }}
{% endcategories %}
```

#### 4. Pagination

```
{% pagination %}
    {{ paginate }}
    {{ paginate | default_pagination, 'Previous', 'Next', 5, 'First', 'Last' }}
    
    {% if paginate.page_size < 100 and paginate.pages > 1 %}
        <a href='{{ paginate.view_all_url }}' class="view-all-page">View All</a>
    {% endif %}
{% endpagination %}
```

