**Однозначно правильный ответ невозможен.**

В консоли не выводятся пробельные узлы. Если перед `<h1>` находится пробельный узел, то будет `undefined`, а если нет -- то текст внутри `<h1>`.

Пример с `undefined`:

```html
<!--+ run -->
<body>
  <h1>Привет, мир!</h1>

  <script>
    alert( document.body.firstChild.innerHTML ); // undefined
  </script>
</body>
```

Если убрать из него перевод строки перед `<h1>`, то было бы `"Привет, мир!"`.