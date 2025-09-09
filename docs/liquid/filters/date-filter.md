# Date Filter

### date

Converts a timestamp into another date format. The format for this syntax is the same as [`strftime`](http://strftime.net/). The input uses the same format as Ruby’s [`Time.parse`](https://ruby-doc.org/stdlib/libdoc/time/rdoc/Time.html#method-c-parse).

To get the current time, pass the special word `"now"` (or `"today"`) to `date`.

Note that the value will be the current time of when the page was last generated from the template, not when the page is presented to a user if caching or static site generation is involved.

```
{{ article.published_at | date: "%a, %b %d, %y" }} // Fri, Jul 17, 15
```

| Directive | Meaning                   | Example |
|-----------|--------------------------|---------|
| `%Y`      | 4-digit year              | `2025`  |
| `%m`      | Month (01–12)             | `06`    |
| `%d`      | Day of the month (01–31)  | `23`    |
| `%A`      | Full weekday name         | `Monday`|
| `%a`      | Abbreviated weekday name  | `Mon`   |
| `%B`      | Full month name           | `June`  |
| `%b`      | Abbreviated month name    | `Jun`   |
| `%H`      | Hour (24-hour clock)      | `14`    |
| `%I`      | Hour (12-hour clock)      | `02`    |
| `%M`      | Minute                    | `05`    |
| `%p`      | AM/PM                     | `PM`    |
| `%S`      | Second                    | `07`    |
| `%y`      | 2-digit year              | `25`    |