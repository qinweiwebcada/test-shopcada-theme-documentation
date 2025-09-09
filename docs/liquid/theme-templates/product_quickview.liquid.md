# product\_quickview.liquid

---

product_quickview.liquid renders a popup of product details without going to product.liquid. The content included product variables and add to cart form.

---


## Layout

![Product Quickview](<../../assets/images/documents/image (64).png>)

## Available Liquid Variables

#### 1. Product

[products](liquid/variables/products.md)

```
{{ product }}
```

#### 2. Add To Cart Form

```
{{ 'add_to_cart' | shopcada_form: product.id }}

// Output

<table><thead><tr><th>Output</th></tr></thead><tbody><tr><td><pre><code><form action="/callback/form" accept-charset="UTF-8" method="post" id="uc-product-add-to-cart-form-23" class="ajax-cart-submit-form uc-aac-cart"><div class="attributes">
 <div class="form-item element-type-select" id="edit-attributes-Size-wrapper">
  <label for="edit-attributes-Size">Size: <span class="form-required" title="This field is required.">*</span></label>
  <span class="select"><select name="attributes[Size]" class="form-select required chosen-widget aac-processed" data-name="Size" id="edit-attributes-Size"><option value="" selected="selected">Select Size</option><option value="S">S</option><option value="M">M</option></select></span>
 </div>
 </div><input type="hidden" name="nid" id="edit-nid" value="23">
 <div class="form-item element-type-select" id="edit-qty-wrapper">
  <label for="edit-qty">Quantity: </label>
  <span class="select"><select name="qty" class="form-select chosen-widget" id="edit-qty"><option value="1" selected="selected">1</option><option value="2">2</option><option value="3">3</option><option value="4">4</option><option value="5">5</option><option value="6">6</option><option value="7">7</option><option value="8">8</option></select></span>
 </div>
<input type="submit" name="op" id="edit-submit-23" value="Add to cart" class="notranslate form-submit node-add-to-cart primary ajax-cart-submit-form-button ajax-cart-processed">
</form>
```

![Add To Cart Form](<../../assets/images/documents/quickviewaddtocartform (1).png>)

