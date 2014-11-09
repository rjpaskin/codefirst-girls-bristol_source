---
title: Creating your own form
---

In order to have a working form on a website there needs to be somewhere for the information to go when the user clicks submit. So far we have only looked at *static* webpages: we have a dumb server that just hands out our hand-created HTML and CSS files. We have no way of accepting information from the user.

Later in the course we will build *dynamic* sites, using Ruby on Rails. In a dynamic site the server builds the pages depending on information stored in a database and details provided by the user. When we have a dynamic site we will just submit the form information back to the server.

### Serving pages using http://

We're going to use [a free service](http://forms.brace.io) from [Brace.io](http://brace.io) to forward the contents of the form submission to your email address. However, for this to work properly, you'll need to access the form page using `http://` (as opposed to `file://`). Fortunately Ruby has a little webserver we can use for this purpose.

{% exercise %}
1. Copy and paste the following into *Terminal* or *Command Prompt with Ruby on Rails* (where *path/to/html_forms* is the location of the `html_forms` repo you cloned):

       ruby -run -e http path/to/html_forms -p 5000

2. Open [http://localhost:5000/basic_form.html](http://localhost:5000/basic_form.html) - you should see the same page as before.
{% endexercise %}

### Brace.io

Brace allows us to design our own form HTML, with their server just handling the form submission -  we just add our email address to the URL that the form submits to, and Brace does the rest. Since we're **sending** data to the server, we need to use `POST`.

Here's an example:

{% highlight html %}
<form method="post" action="http://forms.brace.io/you@email.com">
    <input type="text" name="name">
    <input type="email" name="_replyto">
    <input type="submit" value="Send">
</form>
{% endhighlight %}

{% exercise %}
1. Set the `action` property of the `form` in `basic_form.html` to submit to Brace.io with your email address.
2. Fill out and submit the form
3. Check your inbox (of the email address you used) for a confirmation email - click on the link in the email to confirm that you own that address.
4. Fill and submit the form again - you should now get an email containing the text you entered in the form!
{% endexercise %}

### Redirecting the submission

It isn't ideal that after the submission the user is sent to a Brace 'form submitted' page. Fortunately, it is possible to change this, using a special `_next` input:

{% highlight html %}
<input type="hidden" name="_next" value="http://localhost:5000/thanks.html">
{% endhighlight %}

By using `type="hidden"`, we ensure that the input is not shown to the user, but is still included in the form submission.

{% exercise %}
1. Add an hidden input to the form in `basic_form.html` to redirect to `http://localhost:5000/thanks.html`.
2. Test that the form redirects to this page by filling out the form again.
{% endexercise %}
