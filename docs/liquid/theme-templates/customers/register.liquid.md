# register.liquid

---

register.liquid renders registration form for customers who did not have any account in the store.

---

## Layout

![Register](<../../../assets/images/documents/image (7).png>)

## Available Liquid Variables

#### 1. Customer

[account](liquid/variables/account.md)

```
{{ customer }}
```

#### 2. Register Form

```
{% form "register_form", id: "user-register" %} {% endform %}
```

![Register Form](../../../assets/images/documents/registerform.png)
