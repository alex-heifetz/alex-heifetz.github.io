Для получения вставки буфера нужно отлавливать событие `paste`:
```js
document.addEventListener('paste', function(event) {
  const clipboardData = event.clipboardData || window.clipboardData;
  const pastedText = clipboardData.getData('text');
  
  // Делайте что-то с вставленным текстом
  console.log('Вставленный текст:', pastedText);
});
```

В [[jQuery]] тоже самое можно сделать вот так:
```js
$(document).on('paste', function (event) {
  const clipboardData = event.originalEvent.clipboardData || window.clipboardData;
  const pastedText = clipboardData.getData('text');
  
  // Делайте что-то с вставленным текстом
  console.log('Вставленный текст:', pastedText);
});
```

#JS #jQuery