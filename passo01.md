# Primeiros passos com python

Infelizmente esse tutorial foi pensado para ser ministrado em apenas três horas, o que nos deixa com pouco tempo para aprofundar na linguagem, aqui serão apresentados apenas alguns conceitos que serão necessários para o restante do tutorial.

Caso tenha chegado aqui por outros meios que não a Semana de Tecnologia, e não tenha conhecimento na linguagem, recomendo dar uma parada, e assistir as excelentes aulas do Professor Masanori. O [python para zumbis](https://www.youtube.com/watch?v=6La690qlH5w&list=PLUukMN0DTKCtbzhbYe2jdF4cr8MOWClXc) tem sido uma excelente porta para muitas pessoas.

Neste capítulo experimente abrir o console python através do comando `python3` e teste os comandos enquanto lê.

## Olá mundo

Olá Mundo em python é tão simples como `print('Olá mundo')` por isso um Olá mundo mais pythonico seria `import antigravity`.

Python é conhecido por suas baterias incluídas, ou seja, muita coisa já vem junto com ele, e até mesmo o "Olá mundo" pode ser importado `import __hello__`.

```python
>>> import __hello__
```

## Por Favor e Obrigado

Duas funções que podem ser bastante úteis durante o desenvolvimento python e que costumo dizer que são como "por favor" e "obrigado", são as funções help e dir.


A função "help" pede ajuda sobre um determinado recurso, funcionando inclusive com palavras reservadas como 'if'. É retornado é a documentação daquele recurso.
```python
>>> help(abs)
Help on built-in function abs in module builtins:

abs(x, /)
    Return the absolute value of the argument.

>>> help('if')
The "if" statement
******************

The "if" statement is used for conditional execution:

   if_stmt ::= "if" expression ":" suite
               ( "elif" expression ":" suite )*
               ["else" ":" suite]
...

```

A função "dir" lista todos os atributos e métodos de uma determinada instância. Como em python tudo é objeto, esta função mostra como a instância do objeto se comporta e quais são seus atributos.
```python
>>>dir(5)
['__abs__', '__add__', '__and__', '__bool__', '__ceil__', '__class__', '__delattr__', '__dir__', '__divmod__', '__doc__', '__eq__', '__float__', '__floor__', '__floordiv__', '__format__', '__ge__', '__getattribute__', '__getnewargs__', '__gt__', '__hash__', '__index__', '__init__', '__init_subclass__', '__int__', '__invert__', '__le__', '__lshift__', '__lt__', '__mod__', '__mul__', '__ne__', '__neg__', '__new__', '__or__', '__pos__', '__pow__', '__radd__', '__rand__', '__rdivmod__', '__reduce__', '__reduce_ex__', '__repr__', '__rfloordiv__', '__rlshift__', '__rmod__', '__rmul__', '__ror__', '__round__', '__rpow__', '__rrshift__', '__rshift__', '__rsub__', '__rtruediv__', '__rxor__', '__setattr__', '__sizeof__', '__str__', '__sub__', '__subclasshook__', '__truediv__', '__trunc__', '__xor__', 'bit_length', 'conjugate', 'denominator', 'from_bytes', 'imag', 'numerator', 'real', 'to_bytes']
```

## Estrutura de chave e valor

Python possui por padrão uma estrutura de dados que é chamado dicionário. Esta estrutura armazena valores associando uma chave a seu conteúdo. Veja abaixo algumas tarefas rudimentares com esta estrutura.

```python

>>> tarefas = {} # inicializando uma estrutura vazia

>>> tarefas[1] = 'tarefa 1' # definindo uma tarefa de chave 1, com contéudo 'tarefa 1'

>>> print(tarefas[1])  # exibindo a tarefa 1

>>> tarefas[2] = 'tarefa 2' # definindo uma tarefa de chave 2, com contéudo 'tarefa 2'

>>> tarefas[3] = 'tarefa-3' # definindo uma tarefa de chave 3, com contéudo 'tarefa 3'

>>> tarefas[3] = 'tarefa 3' # editando uma tarefa

>>> del tarefa[1] # removendo a tarefa

```

## Listas

São conjutos de elementos armazenados em uma estrutura de dados similar a uma lista. Estas listas possuem algumas operações que vamos explorar abaixo.

```python

>>> lista = [] # inicializando uma lista vazia

>>> lista.append(1) # estou armazenando um elemento em uma lista

>>> lista[0] # acessa o primeiro elemento da lista(inicia-se por 0 a posição)

>>> lista.remove(1) # procura pelo elemento 1 para ser removido da lista

```

## Percorrendo estruturas

O laço de repetição da linguagem Python é através de iteração de coleções. Tudo que pode ser percorrível pode ser utilizado em uma estrutura de repetição.

```python
>>> for tarefa in tarefas:
        print(tarefa)
```

## Compreensão de listas

É uma sintaxe diferente para criação de uma nova lista com base em outra e inclusive nos é permitido fazer filtro dos elementos.

Algumas operações divertidas são.

```python
>>> lista = [1, 2, 3, 4]

>>> # percorre a lista e somente adiciona a nova lista chamada pares os valores pares, que o resto da divisão por 2 é igual a 0(numero % 2 == 0).
>>> pares = [numero for numero in lista if numero % 2 == 0]
>>> print(pares)

>>> # cria uma nova lista com o quadrado dos números originais.
>>> # dessa vez eu não filtrei os elementos(if), porém realizei a operação de exponenciação.
>>> quadrado = [numero ** 2 for numero in lista]
>>> print(quadrado)


```

## Funções

Porção de código que resolve um problema muito específico. Boas práticas dizem que uma função deve fazer somente uma coisa e fazer isto bem.

```python
def soma(x, y):
   return x + y
```

## Decorador

É um açucar sintático que nos permite alterar mais convenientemente funções e métodos. Pode ser definido como uma função, que ao invés de retornar algum resultado, retorna a função recebida como parametro modificada.

```python
def sentido_da_vida(func):
    def funcao_modificada(x, y):
        return 42
    return sentido_da_vida

@sentido_da_vida
def soma(x, y):
    return x + y
```

Ficaram muitas dúvidas? Sugiro que veja o curso "Python para zumbis" que foi indicado acima e também os links na referência, eles vão ajudar a se sentir mais confiante com a linguagem. Quando se sentir preparado, avance para o passo 2.

## Referências

- [Aprendendo x in y minutos](https://learnxinyminutes.com/docs/pt-br/python3-pt/)

- [Entendendo os decorators](https://pythonhelp.wordpress.com/2013/06/09/entendendo-os-decorators/)

- [How to think like a computer scientist](http://interactivepython.org/runestone/static/thinkcspy/index.html)

[Ir para o passo 2 :arrow_right:](passo02.md)

[:leftwards_arrow_with_hook: Voltar ao README ](README.md)
