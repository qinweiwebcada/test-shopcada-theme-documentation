# Shop

### shop.name

Return shop name



### shop.description

Return short description of the shop that can use in social sharing



### shop.domain

Return domain name of the shop



### shop.email

Return email address of the shop



### shop.phone

Return phone number of the shop



### shop.currency

Return ISO 4217 code of the currency supported



### shop.enabled\_currencies

Return list of currencies accepted in the shop



### shop.enabled.payment\_types

Return use in showing the payment icons

```
{% for type in shop.enabled_payment_types %}
    <li>
        <img src="{{ type | payment_type_image_url }}">
    </li>
{% endfor %}
```



### shop.bank\_transfer

Return true or false indicate if this shop accepted bank transfer payment method



### shop.url

Return URL of the shop



### shop.favicon\_img

Return Favicon File Path of the shop



### shop.logo\_img

Return Logo File Path of the shop



### shop.footer\_message

Return footer message of the shop



### shop.enabled\_social\_medias

Return list of [social medias](liquid/variables/shop/social-media.md) enabled



### shop.languages

Return a list of available [language](liquid/variables/shop/language.md)

```
{% if shop.languages.size > 0 %}
    <select id="setLang">
        {% for language in shop.languages %}
            <option value="{{ language.path }}">{{ language.name }}</option>
        {% endfor %}
    </select>
{% endif %}
```



### shop.settings

Return a list of [shop settings](liquid/variables/shop/settings.md)



### shop.features

Return a list of [shop features](liquid/variables/shop/features.md)
