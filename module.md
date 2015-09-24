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

Implementação que é muito simples quebrar o encapsulamento e manipular o attributo ### Counter.count
diretamente.
