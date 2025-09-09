# reset\_password.liquid

---

reset_password.liquid shows the reset password form for customers who forgot their password.

---

## Layout

![Reset Password](<../../../assets/images/documents/image (2).png>)

## Available Liquid Variables

#### 1. Customer

[account](liquid/variables/account.md)

```
{{ customer }}
```

#### 2. Reset Password Form

```
{% form "reset_password_form" %} {% endform %}
```

![Reset Password Form](../../../assets/images/documents/resetpasswordform.png)
