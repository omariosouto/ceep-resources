# Artigo em Construção !!!

# Manual Básico de Sobrevivência para lidar com Regex

Aqui serão reunidos algumas dicas básicas e exemplos sobre como trabalhar com Regex.

## O que é regex?
Uma forma de escrita, que permite que encontremos padrões de texto. Estranho né? mas pensa comigo, todo texto tem um padrão.
Ex:  `9-9899-9909`

Esse cara, pode ser um numero de telefone de alguém (se for o seu, me desculpe). Mas usei ele como exemplo, para tentarmos ler o um padrão que ele possui de forma bem genrérica esse cara é representado por:

1 numero, hifen, 4 numeros, hifen e 4 numeros.

Mas ele também pode ser lido como ele é naturalmente: `9-9899-9909` o ponto é, a regex procura padrões que podem variar, ou seja, se fixarmos o numero `9-9899-9909` a unica possibilidade de padrão encontrado de telefone é esse cara, e o que queremos é validar qualquer numero que siga esse padrão.

A expressão regular se baseia nessa forma de interpretação, a leitura de padrões deste cara em regex seria assim: 
> `/\d-\d\d\d\d-\d\d\d\d/` (As barras / no começo e no final, serve para indicar uma das formas de como o JavaScript interpreta uma expressão regular).

**\d** é como a Regex interpreta um digito, cada vez que digitamos \d, estamos validando um caracter.

Caso você queira testar, de uma olhada nesse link https://regex101.com/r/BrgnmQ/1

Agora fica tranquilo para fazermos qualquer operação com números como por exemplo um CPF:

> `/\d\d\d.\d\d\d.\d\d\d.\d\d/`

Porém esse cara ficou meio grandinho né? Uma forma de deixar ele mais curto, é usar a notação de chaves **{numero}** , ela permite que passemos um número de vezes que o caracter que estamos validando vai ser repetido.



## Regex em Textos

> soutomarios@gmail.com

Pode ser intereprado como

> [a-zA-Z]{11}@[a-zA-Z]{5}.[a-zA-Z]{3} // Esse cara está procurando caracteres maiusculos e minusculos quando eu uso o conjunto que são as chaves **[]**, nelas eu consigo especificar um conjunto  de caracteres que podem existir, nesse caso qualquer caracter de a até z. 

## Regex em Textos mistos

E caso meu email tivese números eu poderia adicionar numeros de 0-9 nas chaves, ou utilizar o \w, para validar caracteres alfa numéricos.

> \w{11}@[a-zA-Z]{5}.[a-zA-Z]{3} 

E para eliminar a dependência dos números antes do @, podemos utilizar o seletor +, que permite com que façamos a busca por qualquer caracter que bater com nossa regra do \w, até encontrarmos um @

> \w+@[a-zA-Z]{5}.[a-zA-Z]{3} 



## Onde brincar mais com esses caras?

https://regex101.com/


