# String Filter

### append

Adds the specified string to the end of another string.

`append` can also accept a variable as its argument.

```
{{ "/my/fancy/url" | append: ".html" }} // /my/fancy/url.html


{% assign filename = "/index.html" %}
{{ "website.com" | append: filename }} // website.com/index.html
```

### asset\_url

Return complete URL of the theme's asset.

a. If the given file is ended with .css

* If the file name given not found in assets folder, this function first look if .liquid exists, if yes, it will compile the liquid fie.
* After that it check if it is a scss file. If yes, further compile the scss into css file
* It then return the file name with the with the theme path and assets/ concatenated automatically to the file name.

```
{{ "abc.scss.css" | asset_url }}
```

* First check for abc.scss.css exists in the assets folder, if yes, return complete URL.
* If not, check for abc.scss.liquid exists in liquid folder.
  * If yes, then compile abc.scss.liquid into abc.scss, then further compile it into abc.scss.css
  * If not, check for abc.scss, then compile it into abc.scss.css.

b. If the file name given is ended with .js

* If the js file is found, return the complete URL of the js file given.
* If not, this function look if .liquid exists, if exists, it will complete the .liquid into file name given and return the file name.
* It then return the file name with the with the theme path and assets/ concatenated automatically to the file name.

c. All other files All other files should be placed inside assets folder of the theme. This function will output the file name with the theme path and assets/ concatenated automatically to the file name. E.g. `{{ "image.png" | asset_url }}` will return `https://www.yourdomain.com/assets/image.png`

```
{{ file_name | asset_url }}
```

### bank\_transfer\_link

Return the update bank transfer link

```
{{ order.order_id | bank_transfer_link: "Update Payment" }}
```

### bank\_transfer\_details

Return the bank transfer details

```
{{ order.order_id | bank_transfer_details }}
```

### capitalize

Makes the first character of a string capitalized and converts the remaining characters to lowercase.

```
{{ "title" | capitalize }} // Title
{{ "my GREAT title" | capitalize }} // My great title
```

### compact

Removes any `nil` values from an array.

For this example, assume `site.pages` is an array of content pages for a website, and some of these pages have an attribute called `category` that specifies their content category. If we `map` those categories to an array, some of the array items might be `nil` if any pages do not have a `category` attribute.

```
{% assign site_categories = site.pages | map: "category" %}

{% for category in site_categories %}
    {{ category }}
{% endfor %}}

// business
// 
// celebrities
// lifestyle
// sports
// 
// technology
```

By using `compact` when we create our `site_categories` array, we can remove all the `nil` values in the array.

```
{% assign site_categories = site.pages | map: "category" | compact %}

{% for category in site_categories %}
    {{ category }}
{% endfor %}

// business
// celebrities
// lifestyle
// sports
// technology
```

### concat

Concatenates (joins together) multiple arrays. The resulting array contains all the items from the input arrays.

```
{% assign fruits = "apples, oranges, peaches" | split: ", " %}
{% assign vegetables = "carrots, turnips, potatoes" | split: ", " %}

{% assign everything = fruits | concat: vegetables %}

{% for item in everything %}
- {{ item }}
{% endfor %}

// - apples
// - oranges
// - peaches
// - carrots
// - turnips
// - potatoes

```

You can string together multiple `concat` filters to join more than two arrays.

```
{% assign furniture = "chairs, tables, shelves" | split: ", " %}

{% assign everything = fruits | concat: vegetables | concat: furniture %}

{% for item in everything %}
    {{ item }}
{% endfor %}

// - apples
// - oranges
// - peaches
// - carrots
// - turnips
// - potatoes
// - chairs
// - tables
// - shelves
```

### default\_pagination

For use in pagination tag to return standard pagination HTML. Paginate is an array that contains following keys

```
{% pagination %}
   {{ paginate | default_pagination: "Previous", "Next", 5, "First", "Last" }}
{% endpagination %}
```

### downcase

Makes each character in a string lowercase. It has no effect on strings which are already all lowercase.

```
{{ "Parker Moore" | downcase }} // parker moore
```

### download\_url

Return a special download URL that mask of the CDN url base on the file path given

```
{{ file_path | download_url }}
```

### escape

Escapes a string by replacing characters with escape sequences (so that the string can be used in a URL, for example). It doesn’t change strings that don’t have anything to escape.

```
{{ "Have you read 'James & the Giant Peach'?" | escape }}
// Have you read &#39;James &amp; the Giant Peach&#39;?
```

### escape\_once

Escapes a string without changing existing escaped entities. It doesn’t change strings that don’t have anything to escape.

```
{{ "1 < 2 & 3" | escape_once }} // 1 &lt; 2 &amp; 3
```

### first

Returns the first item of an array.

```
{{ "Ground control to Major Tom." | split: " " | first }} // Ground
```

### file\_url

Return CDN URL of a file

### format\_address

Return formatted address

```
{{ order.shipping_address | format_address }}

// Jenny
// 20 WILKIE ROAD
// #10 Wilkie Road
// Singapore, 228098
// 0123456789
```

### handle/handleize

Format string into a handle

```
{{ 'This is my post' | handle }}
// this-is-my-postode
```

### img\_tag

Return img tag with URL, alt text, and class given

```
{{ 'images/icon-search.png' | asset_url | img_tag: 'test', 'img-responsive' }}

// <img class="img-responsive" alt="test" title="test" src="https://www.bubscollective.co/sites/themes/bubscollective/bootstrap4/assets/images/icon-search.png">
```

### img\_url

Return CDN URL of a image, with optional size

```
{{ image | img_url: '120xAUTO' | img_tag: '', 'img-responsive gift-image' }}
```

### join

Combines the items in an array into a single string using the argument as a separator.

```
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}
{{ beatles | join: " and " }}
// John and Paul and George and Ringo
```

### last

Returns the last item of an array.

```
{{ "Ground control to Major Tom." | split: " " | last }}
// Tom.
```

### link\_to

Return anchor tag.

```
{{ "View" | link_to: "https://www.example.com/", "View Page" }}

// Output
<a href=''https://www.example.com" title="View Page">View</a>
```

### location\_name

Return order product location name

```
{{ product.location_id | location_name }}
```

### lstrip

Removes all whitespace (tabs, spaces, and newlines) from the **left** side of a string. It does not affect spaces between words.

```
{{ "          So much room for activities          " | lstrip }}!
// So much room for activities          !
```

### money

Return formatted amount.

If currency code is not given, default to use store default currency or currently selected currency for multi-currency site at the conversation rate configured.

```
{{ amount | money: 'SGD' }}
// S$5.20
```

### payment\_link

Return the update payment / complete payment link

```
{{ order.order_id | payment_link: "Update Payment", "Complete Payment" }}
```

### payment\_type\_image\_url

Return absolute url of the payment type icon image

```
{% for type in shop.enabled_payment_types %}
    <span>{{ type | payment_type_image_url | img_tag }}</span>
{% endfor %}
```

### prepend

Adds the specified string to the beginning of another string.

```
{{ "apples, oranges, and bananas" | prepend: "Some fruit: " }}
// Some fruit: apples, oranges, and bananas
```

### product\_waiting\_list\_url

Return the join waiting list URL for this product

```
{{ product.id | product_waiting_list_url }}
```

### product\_reviews

Return product reviews and review form

```
{{ product.id | product_reviews }}
// Return product reviews and review form

{{ product.id | product_reviews: "reviews" }}
// Return product reviews only

{{ product.id | product_reviews: "form" }}
// Return product review form only
```

### product\_reviews\_rating

Return product review rating (integer)

```
{{ product.id | product_reviews_rating }}
// Return 5
```

### product\_reviews\_count

Return total count of the product (integer)

```
{{ product.id | product_reviews_count }}
// Return 10
```

### product\_ribbon

Render the ribbon upload for this product

```
{{ product.id | product_ribbon }}
```

### product\_wishlist\_link

Return wish list link

```
{{ product.id | product_wishlist_link }}
```

### product\_load

Return full liquid product object

```
{{ product.id | product_load }} 
```

### region\_widgets

Output the HTML for all the widgets given inside the configurable region

```
{{ 'footer1' | region_widgets }}
```

### remove

Removes every occurrence of the specified substring from a string.

```
{{ "I strained to see the train through the rain" | remove: "rain" }}
// I sted to see the t through the 
```

### remove\_first

Removes only the first occurrence of the specified substring from a string.

```
{{ "I strained to see the train through the rain" | remove_first: "rain" }}
// I sted to see the train through the rain
```

### replace

Replaces every occurrence of the first argument in a string with the second argument.

```
{{ "Take my protein pills and put my helmet on" | replace: "my", "your" }}
// Take your protein pills and put your helmet on
```

### replace\_first

Replaces only the first occurrence of the first argument in a string with the second argument.

```
{{ "Take my protein pills and put my helmet on" | replace_first: "my", "your" }}
// Take your protein pills and put my helmet on
```

### reverse

Reverses the order of the items in an array. `reverse` cannot reverse a string.

```
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}
{{ my_array | reverse | join: ", " }}
// plums, peaches, oranges, apples
```

### rstrip

Removes all whitespace (tabs, spaces, and newlines) from the **right** side of a string. It does not affect spaces between words.

```
{{ "          So much room for activities          " | rstrip }}!
//           So much room for activities!
```

### size

Returns the number of characters in a string or the number of items in an array.

```
{{ "Ground control to Major Tom." | size }} // 28
```

### slice

Returns a substring of one character or series of array items beginning at the index specified by the first argument. An optional second argument specifies the length of the substring or number of array items to be returned.

String or array indices are numbered starting from 0.

```
{{ "Liquid" | slice: 0 }} // L
{{ "Liquid" | slice: 2 }} // q
{{ "Liquid" | slice: 2, 5 }} // quid
{{ "Liquid" | slice: -3, 2 }} // ui

{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}
{{ beatles | slice: 1, 2 }} // PaulGeorge
```

### sort

Sorts items in an array in case-sensitive order.

```
{% assign my_array = "zebra, octopus, giraffe, Sally Snake" | split: ", " %}

{{ my_array | sort | join: ", " }} // Sally Snake, giraffe, octopus, zebra
```

### sort\_natural

Sorts items in an array in case-insensitive order.

```
{% assign my_array = "zebra, octopus, giraffe, Sally Snake" | split: ", " %}

{{ my_array | sort_natural | join: ", " }} // giraffe, octopus, Sally Snake, zebra
```

### split

Divides a string into an array using the argument as a separator. `split` is commonly used to convert comma-separated items from a string to an array.

```
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}

{% for member in beatles %}
  {{ member }}
{% endfor %}

// John
// Paul
// George
// Ringo
```

### strip

Removes all whitespace (tabs, spaces, and newlines) from both the left and right sides of a string. It does not affect spaces between words.

```
{{ "          So much room for activities          " | strip }}!
// So much room for activities!
```

### strip\_html

Removes any HTML tags from a string.

```
{{ "Have <em>you</em> read <strong>Ulysses</strong>?" | strip_html }}
// Have you read Ulysses?
```

### strip\_newlines

Removes any newline characters (line breaks) from a string.

```
{% capture string_with_newlines %}
Hello
there
{% endcapture %}

{{ string_with_newlines | strip_newlines }}

// Hellothere
```

### stylesheet\_tag

Return \<link rel>

```
{{ 'styles.scss.css' | asset_url | stylesheet_tag }}
// <link rel='stylesheet' type='text/css' media='all' href='https://dev.g.shopcadacdn.com/sites/files/example/assets/styles.scss.css'>
```

### script\_tag

Return \<script>

```
{{ 'assets/js/user.js' | asset_url | script_tag }}
// <script type="text/javascript" defer src="/assets/lib/animateit/animateit.min.js?24"></script>
```

### shopcada\_form

Return \<form> of the form id given

```
{{ 'add_to_cart' | shopcada_form: product.id }}
```

### t

Return translation of string

```
{{ 'customer.account.title' | t }}
```

### truncate

Shortens a string down to the number of characters passed as an argument. If the specified number of characters is less than the length of the string, an ellipsis (…) is appended to the string and is included in the character count.

```
{{ "Ground control to Major Tom." | truncate: 20 }}
// Ground control to...

{{ "Ground control to Major Tom." | truncate: 25, ", and so on" }}
// Ground control, and so on

{{ "Ground control to Major Tom." | truncate: 20, "" }}
// Ground control to Ma
```

### truncatewords

Shortens a string down to the number of words passed as an argument. If the specified number of words is less than the number of words in the string, an ellipsis (…) is appended to the string.

```
{{ "Ground control to Major Tom." | truncatewords: 3 }}
// Ground control to...

{{ "Ground control to Major Tom." | truncatewords: 3, "--" }}
// Ground control to--

{{ "Ground control to Major Tom." | truncatewords: 3, "" }}
// Ground control to
```

### uniq

Removes any duplicate items in an array.

```
{% assign my_array = "ants, bugs, bees, bugs, ants" | split: ", " %}
{{ my_array | uniq | join: ", " }}
// ants, bugs, bees
```

### upcase

Makes each character in a string uppercase. It has no effect on strings which are already all uppercase.

```
{{ "Parker Moore" | upcase }}
// PARKER MOORE
```

### upsell\_products

Return the list of the products selected to show in upsell section. This is a liquid object that need to be pass to template to convert into HTML.

```
{{ product.id | upsell_products }}
```

### url\_decode

Decodes a string that has been encoded as a URL or by [`url_encode`](https://shopify.github.io/liquid/filters/url_encode/).

```
{{ "%27Stop%21%27+said+Fred" | url_decode }}
// 'Stop!' said Fred
```

### url\_encode

Converts any URL-unsafe characters in a string into percent-encoded characters.

```
{{ "john@liquid.com" | url_encode }}
// john%40liquid.com

{{ "Tetsuro Takara" | url_encode }}
// Tetsuro+Takara
```

### url

Return the absolute URL of a path given.

```
{{ "page/123" | url }} // https://www.example.com/about-us
{{ "<account>/edit" | url }} // https://www.example.com/user/2/edit
```

### visual\_editor\_content

render the content from visual editor

```
{{ page.id | visual_editor_content }}
```

### xofy\_pagination

For use in pagination tag to return standard pagination HTML. Paginate is an array that contains following keys

```
{% pagination %}
   {{ paginate | xofy_pagination: "Previous", "Next", "First", "Last" }}
{% endpagination %}
```
