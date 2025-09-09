# login.liquid

---

login.liquid provides login form for customers who have an account to log in.

---

## Layout

![Login](<../../../assets/images/documents/image (35).png>)

## Available Liquid Variables

#### 1. Customer

[account](liquid/variables/account.md)

```
{{ customer }}
```


#### 2. Social Media Login

```
{{ social_login }}
```

#### 3. Login Form

```
{% form "login_form", id: "user-login" %} {% endform %}
```

![Login Form](../../../assets/images/documents/loginform.png)

