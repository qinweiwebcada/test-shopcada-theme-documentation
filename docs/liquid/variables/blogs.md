# Blogs

### blogs

Return a list of [blog](liquid/variables/blogs/blog.md)

```
{% for blog in blogs %}
    {{ blog.title }}
    ...
{% endfor %}
```



### category

Return current category page [term](liquid/variables/blogs/term.md), only valid for blog category page.

