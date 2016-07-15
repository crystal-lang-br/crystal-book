# O Programa

O programa é um objeto global onde você pode definir tipos, métodos e variáveis locais em relação ao arquivo.

```crystal
# Define um método no programa
def somar(x, y)
  x + y
end

# Invoca o método somar no programa
somar(1, 2) #=> 3
```

O valor de um método é o valor de sua última expressão, não existe a necessidade de escrever instruções `return` explícitas. No entanto, elas são possíveis:

```crystal
def par?(num)
  if num % 2 == 0
    return true
  end

  return false
end
```

Ao invocar um método sem um receptor, como por exemplo `somar(1, 2)`, ele será procurado no programa se não for encontado no tipo atual ou em algum de seus ancestrais.

```crystal
def somar(x, y)
  x + y
end

class Foo
  def bar
    # invoca o método somar do programa
    somar(1, 2)

    # invoca o método baz de Foo
    baz(1, 2)
  end

  def baz(x, y)
    x * y
  end
end
```

Se você quiser invocar o método do programa, mesmo que o tipo atual define um método com o mesmo nome, coloque o prefixo `::`:

```crystal
def baz(x, y)
  x + y
end

class Foo
  def bar
    baz(4, 2) #=> 2
    ::baz(4, 2) #=> 6
  end

  def baz(x, y)
    x - y
  end
end
```

As variáveis declaradas em um programa não são visíveis dentro de métodos:

```crystal
x = 1

def somar(y)
  x + y # error: undefined local variable or method 'x'
end

somar(2)
```

Os parênteses são opcionais nas invocações de métodos:

```crystal
somar 1, 2 # a mesma coisa que somar(1, 2)
```

## Código Principal

O código principal, aquele código que executa quando você compila e roda um programa, pode ser escrito diretamente no arquivo de código fonte sem a necessidade de colocá-lo em um método especial "main":

```crystal
# Este é um programa que imprime "Olá Crystal!"
puts "Olá Crystal!"
```

O código principal também pode ser colocado dentro de declarações de tipo:

```crystal
# Este é um programa que imprime "Hello"
class Hello
  # 'self' aqui é a classe Hello
  puts self
end
```
