# XOR Properties
###### Resolvido por @9Greg6
> Esse é um desafio de Introdução ao CryptoHack modelo CTF que aborda propriedades e operações XOR, bem como codificação de dados
## Sobre o desafio
O enunciado descreve a operação XOR representada por "⊕" como capaz de desfazer uma cadeia de operações que criptografou a flag. Em seguida as propreidades são apresentadas: comutativa, associativa, identidade e auto-inverso, juntamente com a explicações de cada uma delas e o tipo de ferramenta que está sendo trabalhada.

Recebe-se a chave 1; o XOR da chave 1 com a 2; o XOR da chave 2 com a 3; por fim o XOR da flag com as chaves 1, 2 e 3, todos em formato hexadecimal (base 16). Qual é a flag?

[![image.png](https://i.postimg.cc/PJTGDgnm/image.png)](https://postimg.cc/WFWfLf33)


## Resolução
Para a resolução será usada a ferramenta XOR Calculator (https://xor.pw/#) para facilitar e automatizar os processos.
Inicialmente é necessário entender as propriedades para poder aplicá-las da forma correta:

## Propriedades:
Identidade: A ⊕ 0 = A -> Essa propriedade diz que o XOR de uma chave A com a identidade "0" é a prórpia chave A

Auto-inverso: A ⊕ A = 0 -> Essa propriedade diz que o XOR de uma chave A com ela mesma resultado na identidade, visto que houve a comparação de bits e sendo A = A, foi retornado 0 pela igualdade.

## Passo 1:
A primeira operação é feita com a chave 1 e a chave proveniente do XOR da chave 1 com a 2, seguindo o seguinte raciocínio:


chave1 ⊕ (chave2 ⊕ chave 1): pela propriedade associativa, pode-se escrever essa operação como (chave1 ⊕ chave1) ⊕ chave 2


O XOR de "(chave1 ⊕ chave1)" resulta em 0 (auto-inverso), com isso tem-se: "0 ⊕ chave 2" resultando na chave 2 (identidade)

[![Captura-de-tela-2025-06-03-234455.png](https://i.postimg.cc/x8BntQX7/Captura-de-tela-2025-06-03-234455.png)](https://postimg.cc/1V0k3Lcc)


## Passo 2:
Adiante usaremos a mesma lógica para a segunda operação. XOR da chave 2 com a chave proveniente do XOR da chave 2 e 3:

chave2 ⊕ (chave3 ⊕ chave 2): reescrevendo tem-se (chave2 ⊕ chave2 ) ⊕ chave 3

O XOR de "(chave2 ⊕ chave2 )" resulta em 0, assim "0 ⊕ chave 3"  =   chave 3

[![Captura-de-tela-2025-06-03-235417.png](https://i.postimg.cc/2SkrG0yC/Captura-de-tela-2025-06-03-235417.png)](https://postimg.cc/fJrGTjYP)

## Passo 3:

Tendo as 3 chaves, faz-se o XOR da chave proveniente de 1 e 2 com a chave 3, obtendo uma quarta chave referente a:

(chave1 ⊕ chave2) ⊕ chave 3 = chave1 ⊕ chave2 ⊕ chave 3 = chave 4

[![Captura-de-tela-2025-06-04-000956.png](https://i.postimg.cc/q7gtbJqB/Captura-de-tela-2025-06-04-000956.png)](https://postimg.cc/GBwh91v6)

## Passo 4:

Por fim, com a chave vinda de (flag ⊕ CHAVE1 ⊕ CHAVE2 ⊕ CHAVE3) é feito XOR com a chave 4:

(flag ⊕ CHAVE1 ⊕ CHAVE2 ⊕ CHAVE3) ⊕ chave 4 = 

flag ⊕ [(CHAVE1 ⊕ CHAVE2 ⊕ CHAVE3) ⊕ chave 4] =

flag ⊕ (chave 4 ⊕ chave 4) =

flag ⊕ 0 = flag

[![Captura-de-tela-2025-06-04-001154.png](https://i.postimg.cc/sDVgHj0F/Captura-de-tela-2025-06-04-001154.png)](https://postimg.cc/F1Bv744G)

## Passo 5:

Essa flag está em formato hexadecimal (base 16), então no "Output" seleciona-se "ASCII" para obter o formato em strings. Flag encontrada.

[![Captura-de-tela-2025-06-04-001251.png](https://i.postimg.cc/WbWT9Mkr/Captura-de-tela-2025-06-04-001251.png)](https://postimg.cc/SJMBRYVN)


Na resolução do desafio, foi optado por um desenvolvimento detalhado da ferramenta XOR bem como suas propriedades, encontrando as três chaves, mesmo havendo formas mais simples de se resolver, priorizando o aprendizado do assunto e enfatizando a multiplicidade de formas de resolução.

Nesse CTF foi possível aprender a usar essa importante ferramenta e explorar o raciocínio lógico por trás das propriedades aplicando-as no processo de encontrar a flag.

>`crypto{x0r_i5_ass0c1at1v3}`
 
