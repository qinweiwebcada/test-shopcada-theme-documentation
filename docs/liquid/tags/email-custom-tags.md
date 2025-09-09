# Email Custom Tags

---

Email Custom Tags are used for specific case to return certain variables in email templates.

---

## cart upsell

Return a list of related products (You May Also Like) based on cart ID.

```
{% cart_upsell cart.cart_id, limit:6 %}
    {{ upsell_products }}
{% endcart_upsell %}
```

## wishlist items on sale

Return a list of sale items that customer added to wish list.

```
{% wishlist_items_on_sale account.customer_id, limit: 10, page: 1 %}
    {{ products }}
{% endwishlist_items_on_sale %}
```

## store credit

Return store credit current balance and upcoming expiry store credit.

```
{% store_credit account.customer_id, currency: sgd %}
    {{ store_credit }}
{% endstore_credit %}
```

## order points earned

To use in Order Payment Received Email. Return a list of transaction details such as description, points, date ...

```
{% order_points_earned [order-id] %}
    {% for transaction in points_earned.point_txns %}
        {{ transaction }}
    {% endfor %}
{% endorder_points_earned %}
```
