# interencdec
###### Resolvido por Gabriel Gregório de Oliveira
> Esse CTF é sobre criptografia e decodificação
## Sobre o desafio
A descrição da questão é breve, questionando se é possível entender o conteúdo do arquivo base para a questão (https://artifacts.picoctf.net/c_titan/109/enc_flag).
## Resolução
Inicialmente, faz-se o download do arquivo, abrindo-o em formato de texto para ter ideia do que é necessário ser feito.

[![Bloco-de-notas.png](https://i.postimg.cc/85dN9x3H/Bloco-de-notas.png)](https://postimg.cc/ygNMSp7g)

Tem-se caracteres no formato base64 codificado, portanto, é necessário decodificá-los no Base64 Decode:

[![Decodifica-o.png](https://i.postimg.cc/yxVsHvCz/Decodifica-o.png)](https://postimg.cc/JDd933hT)

Como o resultado obtido ('d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX20wMjEyNzU4fQ==') é semelhante a estrutura de caracteres originais, usa-se esse novo texto novamente no Base64 Decode:

[![Decodifica-o2.png](https://i.postimg.cc/W4gvqQ2v/Decodifica-o2.png)](https://postimg.cc/Lq97rQYC)

Obtém-se algo com a mesma estrutura da flag. Por fim, o dCode identificará qual tipo de cifra se trata e retornará os resultados mais prováveis, encontrando a flag:

[![Flag-expl-cita.png](https://i.postimg.cc/D0YDMg26/Flag-expl-cita.png)](https://postimg.cc/dZr47GZZ)


>`picoCTF{caesar_d3cr9pt3d_f0212758}`
 
