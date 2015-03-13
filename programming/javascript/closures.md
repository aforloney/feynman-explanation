_The following is an excerpt from a StackOverflow question explaining closures where the author
decided to take a more creative approach. The URL can be found here, http://stackoverflow.com/a/6472397/166712_

Once upon a time:

There was a princess...

```javascript
function princess() {
```

She lived in a wonderful world full of adventures. She met her Prince Charming, rode around her world on a unicorn, battled dragons, encountered talking animals, and many other fantastical things.

```javascript
    var adventures = [];

    function princeCharming() { /* ... */ }

    var unicorn = { /* ... */ },
        dragons = [ /* ... */ ],
        squirrel = "Hello!";
```

But she would always have to return back to her dull world of chores and grown-ups.

```javascript
    return {
```

And she would often tell them of her latest amazing adventure as a princess.

```javascript
        story: function() {
            return adventures[adventures.length - 1];
        }
    };
}
```

But all they would see is a little girl...

```javascript
var littleGirl = princess();
```

...telling stories about magic and fantasy.

```javascript
littleGirl.story();
```

And even though the grown-ups knew of real princesses, they would never believe in the unicorns or dragons because they could never see them. The grown-ups said that they only existed inside the little girl's imagination.

But we know the real truth; that the little girl with the princess inside...

...is really a princess with a little girl inside.