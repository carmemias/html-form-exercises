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

For the rest of the lesson, we will learn about many other form controls and how to use them with hands-on exercises.

## HTML5 Form exercises - Getting started

We will use the exercises to start building a checkout page for the CodeYourFuture merchandise shop.

Ready? Let's get started!

### Fork and clone this repository

First, you need to create your own copy of these exercises. We call this a "fork". Follow these steps to create your fork.

...screenshot(s)...

Next, you need to download your fork so that you have the files on your computer. Follow these steps to clone your fork.

...screenshot(s)...

Open the Terminal on your computer, browse to your projects directory, and run the following command to create a copy of your fork:

```
cd <your-project-directory>
git clone <your-fork-url>
cd html-form-exercises
code .
```

When you're done, you should see your code editor with the files open on the left, like the following screenshot.

...screenshot...

### Set up the project

Before you can start the exercises, we must set up the project. To do this, we will install all of the code necessary to run the exercises. In your editor, open the Terminal and run the following commands:

```
npm install
```

Carefully read the messages that appear. Are there any errors? If so, please ask a mentor for help.

### Begin working on the exercises

To begin working on the first exercise, run the following command in the Terminal in your code editor:

```
npm run 1
```

This will lauch the sample website for the first exercise in your browser.

Now go back to your code editor. Open the first exercise in the `week-1` directory and find the [readme.md](week-1/1-getting-started/readme.md) file.

...screenshot...

Read the instructions in this file and follow the steps to complete the exercise.

### Completing more exercises

When you have finished the first exercise, move to the next one. First, go to the Terminal in your code editor, and type `CTRL`+`C` (`CMD`+`C` on a Mac) to stop running the first exercise.

To run another exercise, run the following code with the correct number of that exercise:

```
npm run 2
```

### When you have completed all exercises

When you reach the final exercise, you'll be asked to submit a pull request. When you've finished that task, post in your Slack channel to let the mentors know that you have finished.

## Resources

 * [The HTML `<form>` element - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)
 * [HTML forms - MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms)
 * [Creating Accessible Forms - WebAIM](https://webaim.org/techniques/forms/)
 * [Basic Form hints - MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/forms/Basic_form_hints)

## Go deeper

> As well as **check boxes**, other very common form fields are **radio buttons**. We haven't told you how to build them but you can do so with the fields we have covered in this lesson.
Do some research of your own and add a new section to the final form from the exercises. This new section is for the customer to let us know whether the t-shirt needs to be delivered to their home or somewhere else.

> We can do the same as `<input type="submit">` and `<input type="reset">` by using `<button type="submit"></button>` and `<button type="reset"></button>`.
Do some research to find out the advantages and disadvantages of both.
