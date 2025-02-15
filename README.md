# Personal GitHub website built with Hugo
This is my GitHub page built with Hugo.

## Modifications made by me
- (15 Feb 2025) I add shortcodes for creating multicolums according to [this theme](https://roneo.org/shortcodes/#responsive-columns).
I use the three files `column.html`, `columns.html` and `endcolumns.html` in the folder `layouts/shortcodes/` from the [above theme](https://github.com/RoneoOrg/hugo-shortcode-roneo-collection/tree/main/layouts/shortcodes).
Here is an example of creating two columns:
```
{{< columns >}}

Some text

{{< column >}}

![A picture of clouds and sky](/illustrations/cloud.jpg)
Some text

{{< endcolumns >}}
```
