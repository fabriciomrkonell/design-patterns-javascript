**Padrão simples que é extremamente útil e poderoso.**

O padrão Facade tem como objetivo escoder a complexidade do código. Ele provém uma interface unificada para um conjunto de subsistemas.

```bash
function addEvent(element, event, callback) {  
  if(window.addEventListener) {
    element.addEventListener(event, callback, false);
  } else if(document.attachEvent) {
    element.attachEvent('on' + event, callback);
  } else {
    element['on' + event] = callback;
  }
}
```
