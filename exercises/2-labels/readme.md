# Exercise 2: Labels

With the HTML tags we have seen so far, we can build a fully  functioning form. We now need to make it user-friendly.

For this, we will add a **label** for each field:

`<label for="target-id">Some text here</label>`

Labels are used to tell the user what data they are expected to enter in that field. The value of the `for` attribute is the `id` of the field to which the label makes reference. For example:

```
<form method="POST" action="/comment">
	<label for="comment">Make a comment:</label>
	<textarea name="comment" id="comment" rows="5" columns="20"></textarea>
	<input type="submit">Submit</button>
</form>
```

The `label` in the example above is linked to the `textarea` field with id `comment`.

To the user it will look like this:

![Form example](../../img/form-example-1.png)
