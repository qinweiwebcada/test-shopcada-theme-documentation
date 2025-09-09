# Debug Filter

### debug

Vardump the content of the variables into DB log

```
{{ order | debug: 'Order' }}
{{ package | debug: 'Package' }}
```

### dsm

dsm the object, need to "Enable devel modules" in order to see result.

```
{{ order | dsm: 'Order' }}
{{ package | dsm: 'Package' }}
```

### variable\_get

Call variable\_get to get variable value

```
{{ 'description_text' | variable_get: 'default_value' }}
```

###
