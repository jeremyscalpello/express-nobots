# express-nobots
Keep Bots And Crawlers Away From Your Express App

This simple to integrate module uses the user-agent header to determine whether or not a request is made from a bot, and if so, either blocks it or tags the request.

Installation
=====

```bash
npm install express-nobots --save
```

Usage
=====
Make sure to include this as the first middleware!

Blocking Bots:
```javascript
var noBots = require('express-nobots');

....

app.use(noBots());
//or
app.use(noBots({block:true}));
```

Tagging Bots (this will set req.isBot to true if a bot makes a request):
```javascript
var noBots = require('express-nobots');

....

app.use(noBots({block:false}));
```