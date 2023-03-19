# Anotações

## Boas práticas em Python
- O Python utiliza snake_case para nomes de variáveis

## Comandos relevantes

### Comando: help()
- Use o comando `help()` para saber mais sobre outros comandos do Python
- Aperte `q` para sair

### Comando: print()
- Repare que o `print` tem o parâmetro `file=sys.stdout` mas que pode ser mudado para printar em outra saída, um arquivo por exemplo
- Já o parâmetro `end='\n'` se trocar por `end=''` o print deixa de pular uma nova linha
- O parâmetro `sep=''` é responsável por lidar com o caractere que estará entre as strings que você passa para o print, então se tivermos algo como `print('ola', 'mundo', 'doido', sep='-')` teremos `ola-mundo-doido`

### Comando: range(x,y)
- Quando precisamos usar um intervalo para percorrer por exemplo `for i in range(1,10):`. Lembrando que o intervalo é aberto à direita, ou seja no nosso exemplo o `10` não está incluso `(1,2, ..., 8, 9)`
- Se usarmos o range e passarmos somente 1 parâmetro, o range considera como o parâmetro de `stop`, `range(stop) -> range object` a partir de 2, temos o intervalo de `start` e `stop` com `range(start, stop) -> range object`
- Se você passar somente 1 parametro para o `range`, ele considera como o parametro de `stop`, ou seja ele considera que você está indo de `0` até o `stop (não incluso)`. Por exemplo: `range(4) -> (0, 1, 2, 3)`
- `range` tem um parâmetro opicional de `step` que é o intervalo entre cada ponto do intervalo maior, o default é de 1 em 1, mas pode ter outros valores como por exemplo `range(1,10, 3)` que produz o resultado de `(1, 4, 7)`

## Laços
- Temos o `while` e o `for`, normalmente usarmos o laço `for`
- Quando queremos parar uma iteração podemos usar o `break` assim, saimos do `loop`. Por exemplo:
  ```python
  for i in range(1,10):
    print(i)
    if(i == 5):
      break
  ```
  A saida seria:
  ```bash
  > 1
  > 2
  > 3
  > 4
  > 5
  ```

## Tipos
- Tudo em Python é um obejto [referência](https://panda.ime.usp.br/pensepy/static/pensepy/13-Classes/classesintro.html#revisao-de-objetos)
  - Diferente do JavaScript, como tudo vira um objeto no Python, somar `10 + "10"` dá um erro e não retorna um resultado válido
- Tipagem no Python é dinâmica
