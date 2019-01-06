# HTML5 forms

## What will we learn today?
 * HTML5 Form Syntax.
 * Accessibility and Validation.
 * Interactivity.

Forms are everywhere, from the cookie and data privacy notices to Google search, the login page of any website or an online shop's check out.

Any process that needs input from a user, has a form at its forefront.

So how do we build a form in HTML5?

## HTML5 Form Syntax

A form always starts with a `<form>` tag and ends with `</form>`.

Useful attributes to add may be:

* `name` - this is useful if there is more than one form in the same page.
* `method` - can be either `GET` or `POST`, depending on whether the user is expecting to receive some data in response or he/she is expecting the server to do something with the data he/she is posting.
* `action` - this is the URL where the data will be sent.

Of course, apart from these, we can also use the `class` and `id` attributes we have been using for other HTML elements.

For example, if you inspect the main Google page you will see it contains a form like this:

```
<form name="f" method="GET" action="/search" id="tsf">
	...
</form>
```

In this example, we have a form called `f` which gets data back from the `https://google.com/search` URL.

The next step in building a form is to add the necessary controls between its opening and closing tags.

The various HTML elements that go inside the form are called **controls**. The main controls can be classified as **fields**, **labels** or **buttons**.

## Fields

These are the HTML elements used by the user to enter the data. The most common are `<input>`, `<textarea>`, `<select>` and `<option>`.

### `<input>` fields

There are many different types of `<input>` fields. For example, the Google Search form uses a **text** input field:

```
<form name="f" method="GET" action="/search" id="tsf">
	<input type="text" name="q" maxlength="2048" value title="Search">
</form>
```

Notice that the `<input>` field does not have a closing tag.

> What do you think the **maxlength** and **value** attributes do? You can find out by opening [Google](https://google.com) on Chrome and inspecting the field.

> Have a look at the [Input form element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#Attributes) documentation on MDN.
Which other attributes do you think could be useful for a text input element?

Other common types of `<input>` fields are: **email**, **password**, **tel**, **date**, **url**, **image**, **hidden**, **checkbox**, **radio**, **submit**, **reset**, etc.

> Go back to the [Input form element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input) documentation on MDN and find out more about all these different input fields.

For example, to complete the Google Search example, we will add two more input fields to the form:

```
<form name="f" method="GET" action="/search" id="tsf">
	<input type="text" name="q" maxlength="2048" value title="Search">
	<input type="submit" name="btnK" value="Google Search">
	<input type="submit" name="btnI" value="I'm Feeling Lucky">
</form>
```

> What do you think the **value** attribute does in the submit input fields?
Is it the same as in the text input field we saw earlier?

## Resources

 * [The HTML `<form>` element - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)
 * [HTML forms - MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms)
 * [Creating Accessible Forms - WebAIM](https://webaim.org/techniques/forms/)
 * [Basic Form hints - MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/forms/Basic_form_hints)

## Go deeper

> As well as **radio buttons**, other very common form fields are **checkboxes**. We haven't told you how to build them but you can do so with the fields we have covered in this lesson.
Do some research of your own and build an example!

> We can do the same as `<input type="submit">` and `<input type="reset">` by using `<button type="submit"></button>` and `<button type="reset"></button>`.
Do some research to find out the advantages and disadvantages of both.
