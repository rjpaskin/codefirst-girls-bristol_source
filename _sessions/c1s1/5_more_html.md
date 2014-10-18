---
title: More HTML
---
Now we will look at some slightly more interesting things you can do with HTML.

### HTML file layout

{% highlight html %}
<!DOCTYPE html>
<html>
    <head>
        <title>Page title</title>
    </head>
    <body>
        ...
    </body>
</html>
{% endhighlight %}

* The doctype tells you what sort of HTML you're using (HTML5, HTML4 ...). With HTML5 it's simple - you just write `html`.
* Everything is wrapped in an `<html> ... </html>` tag
* Things within the `<head> .. </head>` are used to provide information about the page
* Only things within the `<body> ... </body>` tags are displayed on the page - for example, the text within `<title> ... </title>` will be displayed in the browser bar

### Headings

{% highlight html %}
<h1>Top level heading</h1>

<h3>Lower level heading</h3>
{% endhighlight %}

* There are six levels of heading `h1` ... `h6`
* The higher numbers are more important
* It's usual to only have one `h1` on a page
* You rarely see anything below `h4` in real pages

### Paragraphs and text

{% highlight html %}
<p>This is a paragraph.</p>

<p>This is another paragraph. It has some <em>italic text</em> and some <strong>bold text</strong>.</p>
{% endhighlight %}

* Paragraphs are created using the `<p>` tag
* The `<em>` tag is used to provide emphasis. In reality that means italics - in fact the tag `<i>` also works. Using em is better though as it fits with the idea of *semantic markup* - marking your information with its meaning, instead of how you want it to look.
* The `<strong>` tag is used to make text stand out. It basically means bold - `<b>` also works, but `<strong>` is better - see above.

### Comments

{% highlight html %}
<!-- comments look like this -->
{% endhighlight %}

* Comments will not display in the page ...
* ... but they will display in the page source. Don't be rude!

### Lists

{% highlight html %}
<ul>
    <li>Apples</li>
    <li>Oranges</li>
</ul>
{% endhighlight %}

* Lists have a nested structure
* `<ul>` is for an *unordered* list. This means bullet points.
* `<ol>` is for an *ordered* list. That means automatic numbering.
* In both types of list you add items using a `<li>` tag. This stands for *list item*.

### Links

{% highlight html %}
<a href="http://www.facebook.com">this is a link to facebook</a>
{% endhighlight %}

* The `href` property tells you where the link will point
* You can specify this link it different ways:
    * absolute external link e.g. "http://www.facebook.com"
    * absolute local link e.g. "/about". This links to a file relative to the root of your webserver. For example if your site is at `www.example.com` the link will point to `www.example.com/about`
    * relative local link e.g. "about". This links to a file relative to the current HTML document. In this case it will link to the file called `about` in the same folder as your current html file.
* You can also link to places in the same document using `href="#my_tag"`. More on this later.
* You can get the link to open in a new tab like this: `<a href="http://www.facebook.com" target="_blank">`

### Images

{% highlight html %}
<img alt='my cat' src="my_cat.png">
{% endhighlight %}

* The `alt` tag is for providing a description of your image. This is useful for partially sighted people using screen readers, or in case the image doesn't load.
* The file can be linked to in the same way as `href`. In the example above we use a relative local link to a file called `my_cat.png` in the same folder as the HTML file.

### Tables

{% highlight html %}
<table>
    <thead>
        <tr>
            <th>Column1 Heading</th>
            <th>Column2 Heading</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Row1, Column1</td>
            <td>Row1, Column2</td>
        </tr>
        <tr>
            <td>Row2, Column1</td>
            <td>Row2, Column2</td>
        </tr>
        <tr>
            <td>Row3, Column1</td>
            <td>Row3, Column2</td>
        </tr>
    </tbody>
</table>

{% endhighlight %}

Now you will use these ideas to create a richer web page.

{% exercise %}
1. Go to the github repository for this session: [https://github.com/code61/learning_html](https://github.com/code61/learning_html)
2. [Download](https://github.com/code61/learning_html/archive/master.zip) the repository and unzip it.
3. Open the whole folder in Sublime Text
4. Open the file `example.html` in Chrome and look around with the Developer Tools
5. Open the file `notes.html` in Sublime Text
6. Change `notes.html` into valid HTML so that it looks like `notes_solution.jpg` - use `example.html` as guidance
{% endexercise %}
