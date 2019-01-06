# Exercise 3: textarea

The `<textarea>` is used for bigger chunks of text that normally take up more than only line.

An example of this would be the Comments box:

```
<form action="/comments" method="POST">
	<textarea name="comment" id="comment" cols="45" rows="8" maxlength="65525"></textarea>
	<input type="submit" name="submit" value="Post Comment">
	<input type="hidden" name="comment_post_ID" value="2741">
</form>
```

> Have a look at the example above. What do you think the **cols** and **rows** attributes are for?
And what do you think the **hidden** input filed does?
