# Favourite byte
###### Resolvido por Gabriel Gregório de Oliveira
> Esse desafio da Introdução ao CryptoHack modelo CTF aborda cryptografia básica com XOR em um único byte e decodificação de dados
## Sobre o desafio
O enunciado propõe que uma quebra-cabeça XOR seja resolvido. Alguns dados foram escondidos usando XOR em um único byte secreto, ressaltando a necessidade de decodicação do texto em hexadecimal dado para a reolução.
https://cryptohack.org/courses/intro/xorkey0/
## Resolução
Inicialmente se faz necessário entender o desafio para facilitar a resolução: tem-se dados em hexadecimal e fazendo XOR com o byte secreto dados ocultados serão revelados, entre eles estará a flag.
O desenvolvimento discorrerá utilizando o terminal Windows (tecla Windows + "terminal"), juntamente com a linguagem python, usando comandos simples e práticos.

Com o terminal aberto, será digitado "python3", isso fará com que o terminal execute a interpretação da linguagem python na terceira versão, garantindo maior compatibilidade:

[![Captura-de-tela-2025-06-04-152841.png](https://i.postimg.cc/j2njfj39/Captura-de-tela-2025-06-04-152841.png)](https://postimg.cc/BPss9J0c)

Adiante, o comando "from pwn import *" importará uma poderosa biblioteca do python usada em CTF e exploração de binários:

[![Captura-de-tela-2025-06-04-153629.png](https://i.postimg.cc/sfJzn77c/Captura-de-tela-2025-06-04-153629.png)](https://postimg.cc/4nnjyK87)

Após isso, inicia-se o pequeno código para resolver. Primeiro será feito fazer uma declaração de variável para que ao decorrer da questão não seja necessário escrever o dado em hexadecimal:

[![Captura-de-tela-2025-06-04-154344.png](https://i.postimg.cc/0j4ctVfj/Captura-de-tela-2025-06-04-154344.png)](https://postimg.cc/YL160fTB)

Próximo passo é fazer a decodificação de hexadecimal para bytes, usando o comando "bytes.fromhex(a)", note que o "a" é a variável que foi declarada:

[![Captura-de-tela-2025-06-04-154632.png](https://i.postimg.cc/0jzCJpss/Captura-de-tela-2025-06-04-154632.png)](https://postimg.cc/xNSmwN8x)

O grifado em branco mostra os bytes do hexadecimal.

Agora, como não se sabe qual o byte usando para realizar XOR, usa-se uma estrutura de repetição "for" para que o xor dos bytes obtidos sejam testado com valores que podem ser o bytes secreto.
Um byte pode ser 256 valores possíveis, mas para fins de otimização, pode-se testar menos e ver se a flag já aparece.

A repetição tem a seguinte estrutura: "for i in range(0,99):" isso mostra que o "i" vai variar de 0 a 98, valor menor que 256 escolhido.

[![Captura-de-tela-2025-06-04-155849.png](https://i.postimg.cc/pdDj4s2r/Captura-de-tela-2025-06-04-155849.png)](https://postimg.cc/qtvgCX6H)

Na próxima linha dá-se um "Tab" e será escrito o comando para mostrar o resultado dos testes que seram feitos:

print(xor(bytes.fromhex(a),i)) --> o "print" mostra uma saída de dados, o "xor" executa a operação XOR com os bytes vindos do hexadecimal e o "i" variando de 0 a 98. Clicando duas vezes "Enter" muitas mensagens serão mostradas:

[![Captura-de-tela-2025-06-04-160442.png](https://i.postimg.cc/wBcVLqRw/Captura-de-tela-2025-06-04-160442.png)](https://postimg.cc/kVGKddcS)

Analisando os resultados, note que já a flag já foi encontrada:

[![Captura-de-tela-2025-06-04-160602.png](https://i.postimg.cc/QNPpB9nX/Captura-de-tela-2025-06-04-160602.png)](https://postimg.cc/HjwJRxgK)


Esse CTF envolve operações com XOR e um breve conhecimento de python para automatizar a resolução da questão, explorando também a decodificação de dados muito importante na área de Cyber Segurança.

Foi possível explorar ferramentas do python além de reforçar o trabalho envolvendo mudança de formatos de dados.

>`crypto{0x10_15_my_f4v0ur173_by7e}`
 
