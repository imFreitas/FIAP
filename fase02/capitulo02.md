<div id="fase02" align="center">
<h1>FASE 2 - PROTOTYPING</h1>
<h2>Capítulo 02: Quando a máquina começa a tomar decisões. </h2>
</div>

<div align="center">

## Introdução! 

</div>

## Variável

### O que são variáveis?

São espaços utilizados na memória RAM para armazenar temporariamente alguma informação que os algoritmos utilizam.

São dados temporários, importantes para a solução.

### Tipos de variáveis:

Nos fluxogramas e pseudocódigos, a indicação do tipo de uma variável é feita no momento de sua criação, como ocorre na maior parte das linguagens de programação.

<div align="center">

Tipos básicos | Descrição | Exemplos
--------------|-----------|------------
int | Número inteiro | 1, 20, 1000
float | Números reais (ponto flutuante) | 7.5, 2.07, 50.29
complex | Números complexos | 4j, 5+2j, 15j
bool | Valores lógicos | True, False, 1, 0
string (str) | Textos | "Bom dia", "x", "12", "f5"

</div>

### Importante:

1. O `comando type()` permite identificar o tipo de uma variável.

2. Para ***converter uma variável de um tipo para outro***, chamar o tipo para o qual gostaríamos de converter, como no exemplo:

~~~python
variavel_float = 5.2
print(variavel_float)
# resultado = 5.2

variavel_int = int(variavel_float)
print(variavel_int)
# resultado = 5
~~~

--- 

<div align="center">

## Desvio condicional

</div>

## O que é um Desvio Condicional? `if`

Estrutura que permite realizar um teste lógico e executar alguma ação, dependendo do resultado do teste. Ou seja, o algoritmo realizará um desvio na sua execução com base em uma condição!

1. `Desvio condicional simples`: apresenta um desvio apenas, se a condição testada for verdadeira; caso contrário, o programa segue o fluxo normal.

2. `Desvio condicional composto`: capaz de realizar uma ação para o caso de a condição ser verdadeira, e outra ação para o caso de a condição ser falsa.

3. `Desvio condicional encadeado`: dependendo do resultado de uma condição, permite a realização de um segundo teste.

## If simples em Python

### Exemplo:

"A FIAP está propondo a formação de um time de Esportes para representar a instituição e, para isso, realizará um campeonato interno no qual os alunos podem se inscrever. Porém, há uma condição: só podem ser inscritos alunos que são maiores de idade."

1. Algoritmo:

~~~
variáveis
  idade: inteiro
  rm: alfanumérico
início
  Escreva “Por favor, digite seu RM”
  Leia rm
  Escreva “Por favor, digite sua idade”
  Leia idade
  Se idade >=18 então
    Escreva “Sua participação foi autorizada, aluno de RM”, rm
      Escreva “Mais instruções serão enviadas ao seu e-mail cadastrado na FIAP!”
  Fim_se
Fim
~~~

2. Sintaxe da estrutura condicional simples em Python:

~~~python
if <condição>:
  <ação a ser realizada se a condição for verdadeira>
~~~

---

## If composto em Python

### Exemplo:

Considerando o exemplo anterior, podemos exibir também uma mensagem para os alunos menores de idade.

1. Algoritmo:

~~~
variáveis
  idade: inteiro
  rm: alfanumérico
início
  Escreva “Por favor, digite seu RM”
  Leia rm
  Escreva “Por favor, digite sua idade”
  Leia idade
  Se idade >=18 então
    Escreva “Sua participação foi autorizada, aluno de RM”, rm
      Escreva “Mais instruções serão enviadas ao seu e-mail cadastrado na FIAP!”
  Senão
    Escreva “Sua participação não foi autorizada por causa da sua idade”
  Fim_se
Fim
~~~

2. Sintaxe do desvio condicional composto em Python:

~~~python
if <condição>:
  <ação a ser realizada se a condição for verdadeira>
else:
  <ação a ser realizada se a condição for falsa>
~~~


---

## If encadeado em Python

Consiste na aplicação de um if dentro de outro.

### Exemplo:

Dado o elevado número de alunos com menos de 18 anos interessados em se inscrever no campeonato, a FIAP resolveu abrir vagas para aqueles que possuam autorização escrita dos responsáveis. Portanto:

1. Pseudocódigo:

~~~
variáveis
  idade: inteiro
  rm: alfanumérico
  autorizado: caractere
início
  Escreva “Por favor, digite seu nome”
  Leia rm
  Escreva “Por favor, digite sua idade”
  Leia idade
  Se idade >=18 então
    Escreva “Sua participação foi autorizada, aluno de RM”, rm
    Escreva “Mais instruções serão enviadas ao seu e-mail cadastrado na FIAP!”
  Senão
    Escreva “Você possui autorização dos responsáveis para participar? S – SIM ou N – NÃO”
      Leia autorizado
      Se autorizado = “S” então
        Escreva “Sua participação foi autorizada, aluno de RM”, rm
        Escreva “Mais instruções serão enviadas ao email dos seus responsáveis”
      Senão
        Escreva “Sua participação não foi autorizada por causa da sua idade”
      Fim_se
  Fim_se
Fim
~~~


---

## Python e o poder do `elif`

Utilizado caso seja necessário testar uma série de condições em sequência.

O elif serve como substituto do bloco else, quando queremos realizar uma nova verificação de condição dentro do senão. 

### Exemplo:

Uma operadora de celular concede bônus em consumo da franquia de internet, dependendo da pontuação dos clientes: 
- clientes que fizerem mais de 1000 pontos recebem 3GB adicionais em sua franquia.
- clientes que fizerem mais de 500 pontos recebem 1,5GB adicionais em sua franquia.
- clientes que fizerem mais de 200 pontos recebem 500MB adicionais em sua franquia. 
- Os demais não recebem nada.


---


<div align="center">

## Operando a lógica

</div>

## Operador lógico `OR`

É a conexão entre dois testes lógicos, e retornará verdadeiro caso qualquer um dos testes seja verdadeiro.

<div align="center">

A | B | A or B
--|---|--------
False | False | False
False | True | True
True | False | True
True | True | True

</div>

## Operador lógico `AND`

É a conexão entre dois testes lógicos, e retornará verdadeiro apenas se ambos os testes retornarem verdadeiro!

<div align="center">

A | B | A and B
--|---|--------
False | False | False
False | True | False
True | False | False
True | True | True

</div>

## Importante:

O Python tem uma característica especial que não está presente na maior parte das outras linguagens de programação. Ele permite a avaliação de condições em cadeia. 



---

[Voltar ao início!](https://github.com/imFreitas/FIAP)
