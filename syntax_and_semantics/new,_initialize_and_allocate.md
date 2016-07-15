# new, initialize e allocate

Você pode criar uma instância de uma classe invocando o método `new` da classe:

```
pessoa = Pessoa.new
```

Aqui `pessoa` é uma instância de `Pessoa`.

Não podemos fazer muita coisa com a `pessoa`, então vamos adicionar alguns conceitos a ela. Uma `Pessoa` tem um nome e uma idade. Na seção "Tudo é um objeto", nós dissemos que um objeto tem um tipo e responde a alguns métodos, que são a única maneira de interagir com os objetos, então nós precisaremos dos métodos `nome` e `idade`. Vamos armazenar essa informação em variáveis de instâncias, que são sempre prefixadas com um caractere de *arroba* (`@`). Também queremos que uma Pessoa venha a existir com um nome de nossa escolha e a idade zero. Nós programamos a parte de "vir a existir" com um método especial `initialize`, que normalmente é chamado de *construtor*:

```crystal
class Pessoa
  def initialize(nome : String)
    @nome = nome
    @idade = 0
  end

  def nome
    @nome
  end

  def idade
    @idade
  end
end
```

Agora podemos criar pessoas da seguinte maneira:

```crystal
joao = Pessoa.new "João"
pedro = Pessoa.new "Pedro"

joao.nome #=> "João"
joao.idade #=> 0

pedro.nome #=> "Pedro"
```

(Se você estiver se perguntando porque precisamos especificar que `nome` é uma `String`, mas não precisamos fazer isso para a `idade`, consulte a seção [algoritmo de inferência de tipo global](type_inference.html))

Perceba que criamos uma `Pessoa` com `new`, mas nós definimos a inicialização em um método `initialize`, não em um método `new`. Por que isso?

A resposta é que quando criamos um método `initialize`, Crystal definiu um método `new` para nós, parecido com esse:

```crystal
class Pessoa
  def self.new(nome : String)
    instance = Pessoa.allocate
    instance.initialize(nome)
    instance
  end
 end
```

Primeiramente, perceba a notação `self.new`. Isso significa que o método pertence à **classe** `Pessoa`, e não a instâncias em particular dessa classe. É por isso que conseguimos chamar `Pessoa.new`.

Em segundo lugar, `allocate` é um método de classe de baixo nível que cria um objeto não-inicializado de um dado tipo. Basicamente ele aloca a memória necessária para ele. Então o método `initialize` é invocado nele e então você recebe a instância. Geralmente você nunca invoca `allocate`, já que ele é [unsafe](unsafe.html), mas esse é o motivo pelo qual `new` e `initialize` estão relacionados.
