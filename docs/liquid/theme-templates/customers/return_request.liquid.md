# return\_request.liquid

---

return_request.liquid provides interface for customers who want to return their products based on certain reasons.

---

## Layout

![Return Request](<../../../assets/images/documents/image (52).png>)

## Available Liquid Variables

#### 1. Customer

[account](liquid/variables/account.md)

```
{{ customer }}
```

#### 2. Orders

[order](liquid/variables/order.md)

```
{{ orders }}
```

#### 3. Return Request Form

```
{% form "order_return_request_form", id: "order-return-request-form" %} {% endform %}
```

![Return Request Form](<../../../assets/images/documents/returnrequestform (1).png>)

