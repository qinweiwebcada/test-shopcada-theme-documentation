# Custom Tags

---

Custom Tags are used for specific case to return certain variables, for example countries and categories tag.

---

## all\_rewards

Return all tier rewards

```
{% all_rewards %}
    {{ rewards }}
{% endall_rewards %}
```

## buy\_together

Return all the buy together products of the current product

```
{% buy_together product.id %}
    {{ buy_together_products }}
{% endbuy_together %}
```

## countdown\_timer

Return the countdown timer

```
{% countdown_timer %}
    {{ timer }}
{% endcountdown_timer %}
```

## currencies

Return a list of the currency groups and selected currency group.

```
{% currencies %}
  {{ currency_groups }}
  {{ selected_currency_group }}
{% endcurrencies %}
```

## customcss

Add the custom css file from css\_custom\_editor module.

```
{% customcss %}
```

## countries

Return a list of the Countries that allow manipulation within the block.

```
<select name="country" id="edit-country">
    {% countries %}
        {% for country in countries %}
            <option value="{{ country.dial_code }}"{% if country.dial_code == '65' %} selected{% endif %}>
                +{{ country.dial_code }} 
            </option>
        {% endfor %}
    {% endcountries %}
</select>
```

## categories

Return a list of the categories.

* show all the subcategories if current page is a category page
* show all main categories if current page is not a category page
* contains 3 variables in this tag, current\_categor&#x79;_,_ categorie&#x73;_,_ is\_deepest

```
{% categories %}
    {{ current_category }}
    {{ categories }}
    {{ is_deepest }}
{% endcategories %}
```

## form

Return a form.

```
{% form "contact", class: "contact-form" %}
    {{ form.errors | default_errors }}
    <div class="form-group" id="name-wrapper">
        <label for="edit-name">{{ 'contact.form.name' | t }}</label>
        <input type="text" name="name" id="edit-name" value="{{ form.values.name }}" class="form-control" required>
        <div class="valid-feedback">{{ 'contact.form.valid_feedback' | t }}</div>
    </div>
{% endform %}
```

## google\_review

Return all the google reviews

```
{% google_review minimum_star, limit: 10, page: 0 %}
    {{ google_reviews }}
    {{ average_rating }}
    {{ total_reviews }}
{% endgoogle_review %}
```

## taxonomy

### term

Return term.

* show current term
* show current term's child terms

```
{% term 1 %}
    {{ term }}
    {{ child_terms }}
{% endterm %}
```

### terms

Return a list of terms

```
{% terms 1 %}
    {{ terms }}
{% endterms %}
```

### products\_b&#x79;_\__&#x74;erm

Return a list of products by term.

```
{% terms 1 %}
    {% for term in terms %}
        <div class="container">
            <h2>{{ term.name }} </h2>

            {% products_by_term term.id, limit: 20 , page: 0 %}
                {% for product in products %}
                    <div>{{ product.title }}</div>
                {% endfor %}
            {% endproducts_by_term %}    
            
        </div>
    {% endfor %}
{% endterms %}
```

## node

Return a list of nodes by type

```
{% nodes 'blog', limit: 5, page: 0 %}
   {{ nodes }}
{% endnodes %}
```

## outlets

Return a list of the outlets that available for web used.

```
{% outlets %}
    {{ outlets }}
{% endoutlets %}
```

## order\_points\_earned

Return points earned in an order

```
{% order_points_earned [order-id] OR 177 %}
    {% for transaction in points_earned.point_txns %}
        {{ transaction | dsm }}
        {{ transaction.description }}
        {{ transaction.points }}
    {% endfor %}
{% endorder_points_earned %}
```

## membership\_details

Return a list of membership details if Membership module is turned on.

```
{% membership_details customer.customer_id %}
    {{ membership }}
{% endmembership_details %}
```

## pagination

Return page pagination.

```
{% pagination %}
    {{ paginate | default_pagination, 'Previous', 'Next', 5, 'First', 'Last' }}
{% endpagination %}
```

## points\_expiration\_breakdown

Return a list of expiring points in 3 periods if Reward Point module is turned on.

```
{% points_expiration_breakdown customer.customer_id, period1: 30, period2: 60, period3: 180 %}
    {{ point_expiring_soon }}
    {{ expiring_breakdown }}
{% endpoints_expiration_breakdown %}
```

## pwp

Add purchase with purchase to page

```
{% pwp %}
```

## rewards

Return a list of rewards from reward shop

```
{% rewards %}
    {{ rewards }}
{% endrewards %}
```

## shoe\_sizes

Return all extra sizes detail for shoe.

<pre><code>{% shoe_sizes gender_taxonomy_id %}
    {% for size in shoe_sizes %}
        {{size.us}}
<strong>        {{size.uk}}
</strong>        {{size.eu}}
        {{size.length.start}}
        {{size.length.end}}
        {{size.width.narrow}}
        {{size.width.average}}
        {{size.width.narrow}}
    {% endfor %}
{% endshoe_sizes %}
</code></pre>

## section

Return a section html

<pre><code>{% section 'foo' %}
// Will include the template called 'foo'

{% section 'foo' with 'bar' %}
// Will include the template called 'foo', 
// with a variable called foo that will have the value of 'bar'

{% section 'foo' for 'bar' %}
<strong>// Will loop over all the values of bar, 
</strong><strong>// including the template foo, passing a variable called foo with each value of bar
</strong></code></pre>

## Balances

### points\_balance

Return total points balance

```
{% points_balance account.customer_id %}
    {{ points_balance }}
{% endpoints_balance %}
```

### store\_credit\_balance

Return highest total store credit balance between currency

```
{% store_credit_balance account.customer_id %}
    {{ store_credit_balance }}
{% endstore_credit_balance %}
```

### gift\_certificate\_balance

Return highest total gift certificate balance between currency

```
{% gift_certificate_balance account.customer_id %}
    {{ gift_certificate_balance }}
{% endgift_certificate_balance %}
```

### cashback\_balance

Return highest total cashback balance between currency

```
{% cashback_balance account.customer_id %}
    {{ cashback_balance }}
{% endcashback_balance %}
```

