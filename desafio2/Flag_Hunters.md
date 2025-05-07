# Flag Hunters
###### Resolvido por Gabriel Gregório de Oliveira
> O CTF é sobre engenharia reversa e análise de código
## Sobre o desafio
A descrição do desafio sugere que há uma letra de uma canção, porém o programa não revela o refrão, insinuando que se algo puder ser feito para que esse refrão seja mostrado, a flag pode ser revelada.
## Resolução
Inicialmente é fornecido o programa em python (https://challenge-files.picoctf.net/c_verbal_sleep/9f2b86c1e1068d492f783b106f4535aeb137b0c0e31e43351f8cb82a39456a84/lyric-reader.py) juntamente com o comando netcat para executar o programa (nc verbal-sleep.picoctf.net 56688).

Executando o comando, é solicitado um entrada de dados:

![Input_inicial](https://github.com/user-attachments/assets/31ac7a56-1702-4ae2-bd75-b25bd454a9ad)


Digitando "refrão" por exemplo, a execução finaliza e nenhuma flag é revelada. Assim, faz-se necessário analisar o código como única saída para a resolução.
No início do código, tem-se:

![Análise1](https://github.com/user-attachments/assets/809c33ce-da65-4e79-a903-0c8ab03b4a8e)

ou seja, introdução secreta aparecerá junto com a flag.

Pela análise do código e da execução do programa, fica claro que digitando o refrão correto na entrada de dados, pode-se ter a tal introdução e flag secretas.
No código, encontramos as informações que inferem ser o possível refrão correto, ";", "RETURN " e o valor [0]:
![Encontrando_refrão](https://github.com/user-attachments/assets/0d679986-e0cb-482f-a682-1d2ba0e3dbc6)

Assim, executando o programa com esse refrão, a flag é revelada:
![Flag_encontrada](https://github.com/user-attachments/assets/bd3b1625-9fda-4ecd-bcd5-7cf60fcc5d9e)

>`picoCTF{70637h3r_f0r3v3r_75053bc3}`
