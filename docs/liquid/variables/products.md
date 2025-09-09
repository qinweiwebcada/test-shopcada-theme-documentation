# Products

### id

Return product ID



### title

Return product title



### teaser

Return product teaser



### content

Return product description



### images

Return an array on product images

```
{% for image in product.images %}
    {{ image | img_url | img_tag }}
{% endfor %}
```

### url

Return product url



### tags

Return an array of product terms

```
{% for tag in product.tags %}
    <a class="tag" href="{{ tag.url }}">{{ tag.name }}</a>
{% endfor %}
```



### category

Return an array of product category

```
{% for category in product.category %}
    <div class="category" href="{{ category.url }}">{{ category.name }}</div>
{% endfor %}
```



### collection

Return an array of product collection

```
{% for collection in product.collection %}
    <div class="collection" href="{{ collection.url }}">{{ collection.name }}</div>
{% endfor %}
```



### brand

Return `product.brand.name`



### color

Return an array of product color



### available

Return true if product is available, else false



### pos\_available

Return true if product is available in POS, else false



### pos\_available\_on

Return available date of product in POS

{{ date-output-example pos_available_on }}



### images\_info

Return an array of [product images info](liquid/variables/products/product-image-info.md)

```
{% for image in product.images_info %}
    {{ image.file_path | img_url: settings.product_detail_image_thumbnail_size | img_tag : image.alt, 'img-fluid' }}   
{% endfor %}
```



### extra\_fields

Return an array of [product extra fields](liquid/variables/products/product-extra-field.md)

```
{% for extra_field in product.extra_fields %}
    {% if extra_field.label and extra_field.content %}
        <div class="extra-field-label">{{ extra_field.label }}</div>
        <div class="extra-field-content">{{ extra_field.content }}</div>
    {% endif %}
{% endfor %}
```



### options

Return an array of [product options](liquid/variables/products/product-option.md)&#x20;



### options\_by\_name

Return an array of [product options](liquid/variables/products/product-option.md) by name



### options\_with\_values

Return an array of [product option](liquid/variables/products/product-option.md) with values



### list\_price

Return product list price



### compare\_at\_price

Return product compare price



### price

Return product price



### price\_min

Return product price minimum



### price\_max

Return product price maximum



### price\_varies

Return boolean of product price varies



### variants

Return an array of [product variants](liquid/variables/products/product-variant.md)



### wishlist

Return string on product wishlist

```
{% if shop.features.wishlist %}
    {{ product.wishlist }}
{% endif %}
```



### related\_products

Return an array of [related products](liquid/variables/products/related-product.md), it comes from "Group Products By Colour"



### backorder\_status

Return product backorder status content



### backorder\_status\_date

Return product backorder status date

{{ date-output-example backorder_status_date }}

