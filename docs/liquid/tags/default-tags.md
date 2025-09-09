# Default Tags

---

Default tags consists of variables, iteration, control flow and theme.

---

## Variables

### assign

Performs an assignment of one variable to another

```
{% assign var = var %}
{% assign var = "hello" | upcase %}
```



### capture

Captures the output inside a block and assigns it to a variable

```
{% capture foo %}
   bar
{% endcapture %}
```



### increment

Used to increase a counter into a template. Creates a new number variables and increases its value by one every time it is called. The initial value is 0.

```
{% increment variable %}
   {{ variable }}
{% increment variable %}
   {{ variable }}
{% increment variable %}
   {{ variable }}

// 0 1 2
```



### decrement

Used to decrease a counter into a template. Creates a new number variables and decreases its value by one every time it is called. The initial value is -1.

```
{% decrement variable %}
   {{ variable }}
{% decrement variable %}
   {{ variable }}
{% decrement variable %}
   {{ variable }}

// -1 -2 -3
```



## Iteration

### for

Loops over an array, assigning the current value to a given variable.

```
{% for item in array %}
   {{ item }}
{% endfor %}
```



### break

Break iteration of the current loop.

```
{% for i in (1..5) %}
   {% if i == 4 %}
      {% break %}
   {% endif %}
      {{ i }}
{% endfor %}

// 1 2 3
```



### continue

Skips the current iteration of the current loop.

```
{% for i in (1..5) %}
   {% if i == 4 %}
      {% continue %}
   {% endif %}
      {{ i }}
{% endfor %}

// 1 2 3 5
```



### tablerow

Quickly create a table from a collection.

```
<table>
   {% tablerow product in collection.products %}
       {{ product.title }}
   {% endtablerow %}
</table>


// Output
<table>
   <tr class="row1">
      <td class="col1">
         Cool Shirt
      </td>
      <td class="col2">
         Alien Poster
      </td>
      <td class="col3">
         Batman Poster
      </td>
      <td class="col4">
         Bullseye Shirt
      </td>
      <td class="col5">
         Another Classic Vinyl
      </td>
      <td class="col6">
         Awesome Jeans
      </td>
   </tr>
</table>
```



### cycle

Cycles between a list of values, calls to the tag will return each value in turn.

```
{% cycle "one", "two" %}
{% cycle "one", "two" %}
{% cycle "one", "two" %}

// one two one
```

Cycles can also be named, to differentiate between multiple cycle with the same values:

```
{% cycle 1: "one", "two" %}
{% cycle 2: "one", "two" %}
{% cycle 1: "one", "two" %}
{% cycle 2: "one", "two" %}

// one one two two
```


## Control Flow

### if

If statement. Support if and else if. Noted that the else if spelled as elsif.

```
{% if customer.name == 'admin' %}
   Hey Admin!
{% elsif customer.name == 'anonymous' %}
   Hey Anonymous!
{% else %}
   Hi Stranger!
{% endif %}
```


### case

A switch statement.

```
{% assign handle = 'cake' %}
{% case handle %}
   {% when 'cake' %}
      This is a cake
   {% when 'cookie' %}
      This is a cookie
   {% else %}
      This is not a cake nor cookie
{% endcase %}
```


### unless

Negated If statement.

```
{% unless product.title == 'Awesome' %}
   These shoes are not awesome
{% endunless %}
```


### and

Used in `if` and `unless` tag to add `AND` conditions to the tag.

```
{% if product.title == 'Awesome Shoes' and product.price < 20000 %}
   These awesome shoes are affodable.
{% endif %}
```


### or

Used in `if` and `unless` tag to add `OR` conditions to the tag.

```
{% if product.title == 'Awesome Shoes' or product.title == 'Awesome Hat' %}
   You're buying an awesome product!
{% endif %}
```


## Theme

### comment

Creates a comment, everything inside will be ignored.

```
{% comment %}
   This will not be rendered
{% endcomment %}
```


### include

Inserts a snippet from the snippets folder of a theme.

Include the template called 'foo', which is foo.liquid inside snippet folder.

```
{% include 'foo' %}
```


Include the template called 'bar', with a variable called foo that will have the value of 'bar'.

```
{% include 'foo' with 'bar' %}
```


Looping over all the values of bar, including the template foo, passing a variable called foo with each value of bar.

```
{% include 'foo' for 'bar' %}
```


### paginate

The paginate tag works in conjunction with the for tag to split content into numerous pages.

```
{% paginate collection.products by 5 %}
   {% for product in collection.products %}
      <!-- show product details here -->
   {% endfor %}
{% endpaginate %}
```


### raw

Allows output of Liquid code on a page without being parsed.

```
{% raw %}{{ 5 | plus: 6 }}{% endraw %} is equal to 11.

// {{ 5 | plus: 6 }} is equal to 11.
```