# You either know, XOR you don't
###### Solved by @9Greg6
> Esse é um desafio de Introdução ao CryptoHack modelo CTF que aborda operações XOR, bem como codificação de dados e linguagem python
## Sobre o desafio
O enunciado informa que a flag foi criptografa com uma chave secreta, juntamente com um texto em hexadecimal e uma dica muito importante: "Lembre-se do formato da flag", no caso "crypto{...".

[![image.png](https://i.postimg.cc/HsxVfKFZ/image.png)](https://postimg.cc/MXC6Bs6V)


## Resolução
Para resolver essa questão é necessário se atentar a dica ofertada e usar comandos em linguagem python muito semelhantes a questão anterior.

## Passo 1:
Abrir o terminal do Windows (tecla "Windowns" + "terminal") ou qualquer outro.

## Passo 2:
Digitar o comando "python3" para que o terminal execute a interpretação da linguagem python na versão 3:

[![image.png](https://i.postimg.cc/8CFY91bp/image.png)](https://postimg.cc/bGhL2fMW)

## Pass0 3:
Executar o comando "from pwn import*" para que uma biblioteca do python seja importada e realize operações XOR:

[![image.png](https://i.postimg.cc/vTmf2mWX/image.png)](https://postimg.cc/vgp4cb26)

## Passo 3:
Realizar a declaração de variáveis, para que não seja necessário escrever o dado em hexadecimal nos processos seguintes, podendo referenciá-lo pela variável escolhinda:

a = "0e0b213f26041e480b26217f27342e175d0e070a3c5b103e2526217f27342e175d0e077e263451150104"

Juntamente extrai-se o bytes do hexadecimal, referenciado por "b":

b = bytes.fromhex(a)

[![image.png](https://i.postimg.cc/661v5tVJ/image.png)](https://postimg.cc/8sM5Z8nt)

## Passo 4:
Agora, usa-se a dica fornecida, será criada uma variável "c" que fará referência ao formato da flag:

c = b"crypto{"

[![image.png](https://i.postimg.cc/R0sH6mrH/image.png)](https://postimg.cc/kVS4zkgJ)

Essa pista será usada para operar XOR com o hexadecimal, usufruindo da propriedade identidade para obter alguma informação da bandeira.

## Passo 5:
Executar o comando para que o XOR dos bytes do hexadecimal ("b") e a dica ("c") seja feito e mostrado na interface do terminal:

print(xor(b,c))

[![image.png](https://i.postimg.cc/h432WFfh/image.png)](https://postimg.cc/CdkGkQCV)

Na resposta do programa, tem-se alguns bytes que serão a chave final para a resolução: "myXORke+y"

Note que "myXORke+y"  --> "myXORke" + "y" = "myXORkey" essa é a chave que será usada

d = "myXORkey"

[![image.png](https://i.postimg.cc/ZRLKBFvD/image.png)](https://postimg.cc/zbV14hjn)

## Passo 6:
Operar XOR dos bytes do hexadecimal com a chave ("d"), mostrando o resultado:

print(xor(b,d))

[![image.png](https://i.postimg.cc/tg3Vk6VF/image.png)](https://postimg.cc/bGvJNsgv)

Flag encontrada!


O desafio envolve apliações das propriedades do XOR, juntamente com a criptografia, explorando também a questãp de transformação de dados.

As contribuições desse tipo de CTF são excepcionais para o desenvolvimento da lógica computacional assim como as ferramentas da Cyber Segurança.

>`crypto{1f_y0u_Kn0w_En0uGH_y0u_Kn0w_1t_4ll}`
 
