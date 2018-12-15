# VUE.js

## Grundstruktur
index.html:
```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Page Title</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bigfishtv-turret/4.0.0/turret.min.css"
        crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
    <script src="main.js"></script>
</head>

<body>
    <h1>Hello World</h1>
    <div id="app">{{test}}</div>
</body>

</html>
```

main.js:
```javascript
new Vue({
    el: '#app',
    data: {
        test: 'Hier bin ich :)'
    }
})
```
