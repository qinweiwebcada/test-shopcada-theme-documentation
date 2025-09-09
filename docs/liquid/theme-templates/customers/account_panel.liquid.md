# account\_panel.liquid

---

account_panel.liquid is used for having account drawer as quick way to show
the list of account links or authorization form.

---

## Layout

![Account Links Drawer](<../../../assets/images/documents/image (40).png>)

![Register & Login Drawer](<../../../assets/images/documents/image (21).png>)

## Available Liquid Variables

#### 1. Customer

[account](liquid/variables/account.md)

```
{{ customer }}
```

#### 2. Social Login

```
{{ social_login }}
```

![Social Media Login](../../../assets/images/documents/socialmedialogin.png)

#### 3. Login Form

```
{% form "login_form", id: "user-login" %} {% endform %}
```

![Login Form](<../../../assets/images/documents/login form.png>)

#### 4. Register Form

```
{% form "register_form", id: "user-register" %} {% endform %}
```

![Register Form](<../../../assets/images/documents/register form.png>)

