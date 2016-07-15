# Métodos e variáveis de instância

Podemos simplificar nosso construtor usando uma sintaxe mais curta para atribuir o argumento de um método a uma variável de instância:

```crystal
class Pessoa
  def initialize(@nome : String)
    @idade = 0
  end
end
```

No momento não podemos fazer muita coisa com uma pessoa: criá-la com um nome, pedir qual é seu nome e sua idade, que é sempre zero. Então vamos adicionar um método para fazer uma pessoa envelhecer:

```crystal
class Pessoa
  def envelhecer
    @idade += 1
  end
end

joao = Pessoa.new "João"
pedro = Pessoa.new "Pedro"

joao.idade #=> 0

joao.envelhecer
joao.idade #=> 1

pedro.idade #=> 0
```

Nomes de métodos começam com uma letra minúscula e, como convenção, só contém letras minúsculas, underscores e números.

Como uma observação, podemos definir `envelhecer` dentro da definição original de `Pessoa`, ou em uma definição separada: Crystal combina todas as definições em uma única classe. O código a seguir funciona normalmente:

```crystal
class Pessoa
  def initialize(@nome : String)
    @idade = 0
  end
end

class Pessoa
  def envelhecer
    @idade += 1
  end
end
```

## Redefinindo métodos e previous_def

Se vocÊ redefinir um método, a última definição tomará precedência.

```crystal
class Pessoa
  def envelhecer
    @idade += 1
  end
end

class Pessoa
  def envelhecer
    @idade += 2
  end
end

pessoa = Pessoa.new "João"
pessoa.envelhecer
pessoa.idade #=> 2
```

Você pode invocar o método previamente definido com `previous_def`:

```crystal
class Pessoa
  def envelhecer
    @idade += 1
  end
end

class Pessoa
  def envelhecer
    previous_def
    @idade += 2
  end
end

pessoa = Pessoa.new "João"
pessoa.envelhecer
pessoa.idade #=> 3
```

Sem argumentos e nem parênteses, `previous_def` recebe os mesmos argumentos que o método em que é invocado. Doutra forma, ele recebe os argumentos que você passar para ele.

## Inicialização Catch-all

Variáveis de instância também podem ser inicializadas fora de métodos `initialize`:

```crystal
class Pessoa
  @idade = 0

  def initialize(@nome : String)
  end
end
```

Isso inicializará `@idade` com zero em todos os construtores. Isso é útil para evitar duplicação e também para evitar o tipo `Nil` ao reabrir uma classe e adicionar variáveis de instância a ela.
