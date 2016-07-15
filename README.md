# Linguagem de Programação Crystal

Esta é a documentação da linguagem de programação Crystal.

Crystal é uma linguagem de programação que tem os seguintes objetivos:

* Ter uma sintaxe semelhante à de Ruby (mas nosso objetivo não é compatibilidade)
* Ter checagem de tipos estática, mas sem ter que especificar o tipo das variáveis ou dos argumentos dos métodos.
* Poder chamar código em C através de _bindings_ escritos em Crystal.
* Ter avaliação e geração de código em tempo de compilação, para evitar código de _boilerplate_.
* Compilar em código nativo eficiente.


## Build

```
$ npm install -g gitbook-cli
$ gitbook build --gitbook=2.3.2
```

O Html será salvo no diretório `_book`.
