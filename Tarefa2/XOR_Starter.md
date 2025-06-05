# XOR Started
###### Resolvido por @9Greg6
> Esse é um desafio de Introdução ao CryptoHack no modelo CTF, envolvendo operações XOR e codificação de dados.
## Sobre o desafio abordado
O enunciado da questão apresenta a ferramenta XOR com uma breve introdução do seu funcionamento, exemplificando o XOR bit a bit, sendo a comparação dos bits e em caso de igualdade, há retorno de 0 (zero). Além disso, também é explicado a importância da codificação de dados no caso de XOR com strings ou com número inteiros ao invés do binário. Por fim, recebe-se a string "label" e o inteiro 13, informando que o XOR de cada caracter com o inteiro retornará a flag do desafio.


[![image.png](https://i.postimg.cc/yxvGZWPH/image.png)](https://postimg.cc/rRRg6V3n)


## Resolução do Desafio
Inicialmente, tem-se a string "label" e o número inteiro 13, sendo necessário realizar a operação XOR de cada caracter com o valor informado.

## Passo 1:
A ferramenta XOR Calculator (https://xor.pw/) é utilizada para a resolução de forma simples e rápida. Acessando o site, as abas "Input:" e "Output:" permitem que dados em diferentes formatos sejam processados e realizada a operação:

[![Captura-de-tela-2025-06-03-221107.png](https://i.postimg.cc/GhWBtJSr/Captura-de-tela-2025-06-03-221107.png)](https://postimg.cc/dL9QSdYS)


## Passo 2:
No primeiro "Input" é colocado o valor inteiro informado "13" com o formato "decimal(base10)". No segundo coloca-se os caracteres no formato "ASCII(BASE 256)", evidenciando que como o desafio sugere o XOR bit a bit, será feito o operação de 13 com "l", guardando o resultado, depois de 13 com "a" e assim por diante até usar todos os caracteres da string. No parâmetro "Output" usa-se o formato "ASCII(base256)" visto que busca-se a flag em formato de strings:

[![Captura-de-tela-2025-06-03-222318.png](https://i.postimg.cc/yNMBXvcY/Captura-de-tela-2025-06-03-222318.png)](https://postimg.cc/hJ1HK82H)


## Passo 3:
Clicando em "Calculate XOR" obtém-se o primeiro caracter da flag que é anotado para garantir a organização da resolução do desafio. 
Replicando esse processo com cada letra da string, a flag é montada: 

[![Captura-de-tela-2025-06-03-222906.png](https://i.postimg.cc/8Pz8vq9m/Captura-de-tela-2025-06-03-222906.png)](https://postimg.cc/Lhw0K0HJ)


Resaltando que o processo de transformação de dados é feita pelo programa selecionando o formato tido e o que se busca, objetivando automatizar e facilitar, porém pode ser feito manualmente convertendo 13 para binário (1101) e também convertendo cada caracter com a tabela base: https://qph.cf2.quoracdn.net/main-qimg-45ad8916ef8091a4ccc248e6428337ae-pjlq.


Esse desafio explora conceitos importantes da Cyber Segurança e testa habilidades como a compreensão da operação XOR a nível de bits e habilidade para manipular diferentes representações de dados (ASCII, hex, bytes), mesmo tendo um programa que o realize é valorizado o entendimento do processo por trás como explicitado.

Foi possível enriquecer meu conhecimento na criptografia simétrica com princípio básico de usar uma mesma chave para cifrar e decifrar, a exemplo da propriedade da auto-inversão, além de favorecer meu pensamento computacional, desenvolvendo o raciocínio lógico de resolução.


>`crypto{aloha}`
 
