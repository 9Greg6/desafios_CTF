# Flag Hunters
###### Resolvido por Gabriel Gregório de Oliveira
> O CTF é sobre engenharia reversa e análise de código
## Sobre o desafio
A descrição do desafio sugere que há uma letra de uma canção, porém o programa não revela o refrão, insinuando que se algo puder ser feito para que esse refrão seja mostrado, a flag pode ser revelada.
## Resolução
Inicialmente é fornecido o programa em python (https://challenge-files.picoctf.net/c_verbal_sleep/9f2b86c1e1068d492f783b106f4535aeb137b0c0e31e43351f8cb82a39456a84/lyric-reader.py) juntamente com o comando netcat para executar o programa (nc verbal-sleep.picoctf.net 56688).

Executando o comando, é solicitado um entrada de dados:

[![Input-inicial.png](https://i.postimg.cc/zX66w02X/Input-inicial.png)](https://postimg.cc/bs0mpHjK)


Digitando "refrão" por exemplo, a execução finaliza e nenhuma flag é revelada. Assim, faz-se necessário analisar o código como única saída para a resolução.
No início do código, tem-se:

[![An-lise1.png](https://i.postimg.cc/LsBWpR9n/An-lise1.png)](https://postimg.cc/d7362bTY)

ou seja, introdução secreta aparecerá junto com a flag.

Pela análise do código e da execução do programa, fica claro que digitando o refrão correto na entrada de dados, pode-se ter a tal introdução e flag secretas.
No código, encontramos as informações que inferem ser o possível refrão correto, ";", "RETURN " e o valor [0]:
[![Encontrando-refr-o.png](https://i.postimg.cc/L57CT8T0/Encontrando-refr-o.png)](https://postimg.cc/hQL14gN9)

Assim, executando o programa com esse refrão, a flag é revelada:
[![Flag-encontrada.png](https://i.postimg.cc/4N7F3p4C/Flag-encontrada.png)](https://postimg.cc/mt4SXzFV)

>`picoCTF{70637h3r_f0r3v3r_75053bc3}`
