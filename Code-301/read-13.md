# Notes for Read 13 - Update/Delete

[Sending form data](https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data)

`<form method="GET">'

This uses the *REST* verbs *Get, Post, Update, Delete*

GET URL `www.foo.com/?say=Hi&to=Mom`

POST Example

```<form action="http://www.foo.com" method="POST">
  <div>
    <label for="say">What greeting do you want to say?</label>
    <input name="say" id="say" value="Hi">
  </div>
  <div>
    <label for="to">Who do you want to say it to?</label>
    <input name="to" id="to" value="Mom">
  </div>
  <div>
    <button>Send my greetings</button>
  </div>
</form>
```

POST URL = `http://www.foo.com?say=Hi&to=Mom`

STEPS TO VIEW HTTP requests:

+ Select "Network"
+ Select "All"
+ Select "foo.com" in the "Name" tab
+ Select "Headers"

Sending Files

```<form method="post" action="https://www.foo.com" enctype="multipart/form-data">
  <div>
    <label for="file">Choose a file</label>
    <input type="file" id="file" name="myFile">
  </div>
  <div>
    <button>Send the file</button>
  </div>
</form>
```

The method attribute **POST** Can't put into URL params.
**enctype** = *multipart/form-data*: Data will be split into multiple parts, one for each file and one for the text data included in the form body (if text is also entered into the form).

One or more `<input type="file">` controls to allow your users to select the file(s) that will be uploaded.

## SECURITY

*** NEVER TRUST USERS ***

Escape potentially dangerous characters

+ Specific characters you should be cautious with vary depending on the context in which the data is used and the server platform you employ, but all server-side languages have functions for this. 
+ Things to watch out for are character sequences that look like executable code (such as JavaScript or SQL commands).
+ Limit the incoming amount of data to allow only what's necessary.
+ Sandbox uploaded files. Store them on a different server and allow access to the file only through a different subdomain or even better through a completely different domain.



[&lt;--&#91;BACK&#93;](/README.md)