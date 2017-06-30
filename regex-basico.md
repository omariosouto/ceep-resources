# Manual Básico de Sobrevivência para lidar com Regex

Aqui serão reunidos algumas dicas básicas e exemplos sobre como trabalhar com Regex.

## O que regex?
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

Só que para validarmos um email por exemplo, não poderiamos utilizar esse cara. Pois o meu email por exemplo, nem sequer tem um numero

> soutomarios@gmail.com

Felizmente, o cara que criou as expressões regulares pensou nesse cenrio e criou mais um carinha na regex que é o **\w**, ele permite que nós validemos 

## Regex em Textos mistos


## Onde brincar mais com esses caras?

https://regex101.com/
