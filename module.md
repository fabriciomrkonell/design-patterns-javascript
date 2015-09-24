**Permite organizar o código sem expor as variáveis globais.**

Executa a função imediatamente ápós sua definição

```bash
(function(){
	// alert('module')
})
```

Injeção de dependência (JQuery)

```bash
(function($){
  // alert('module')
})(jQuery);
```

**Funções podem ser executadas e receber parâmetros.**

Implementação que é muito simples quebrar o encapsulamento e manipular o atributo ```Counter.count``` diretamente.

```bash
var Counter = {
	count: 0,
  increment: function() {
    return this.count += 1;
  }
};

Counter.increment();
Counter.increment();
Counter.increment();
Counter.count; // Imprime 3
Counter.count = 10;
Counter.count; // Imprime 10
```

Mesma implementação utilizando o padrão Module. Neste caso é encapsulado todo o seu comportamento.

```bash
var Counter = (function(){
  var count = 0;
  return {
    count: function() {
      return count;
    },
    increment: function() {
      return count += 1;
    }
  };
})();
```
