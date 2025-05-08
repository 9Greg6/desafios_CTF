# interencdec
###### Resolvido por Gabriel Gregório de Oliveira
> Esse desafio CTF é sobre criptografia e decodificação
## Sobre o desafio
A descrição da questão é breve, questionando se é possível entender o conteúdo do arquivo base para a questão (https://artifacts.picoctf.net/c_titan/109/enc_flag).
## Resolução
Inicialmente, faz-se o download do arquivo, abrindo-o em formato de texto para ter ideia do que é necessário ser feito.

![Bloco_de_notas](https://github.com/user-attachments/assets/f9ceb5a6-a24a-4e88-bef2-812c09c51e6d)

Tem-se caracteres no formato base64 codificado, portanto, é necessário decodificá-los no Base64 Decode:

![Decodificação](https://github.com/user-attachments/assets/7fa162c9-2fde-4140-a5ce-8b68e1e1f242)

Como o resultado obtido ('d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX20wMjEyNzU4fQ==') é semelhante a estrutura de caracteres originais, usa-se esse novo texto novamente no Base64 Decode:

![Decodificação2](https://github.com/user-attachments/assets/31e34cc8-9978-401e-bbf1-dff5b527811a)

Obtém-se algo com a mesma estrutura da flag. Por fim, o dCode identificará qual tipo de cifra se trata e retornará os resultados mais prováveis, encontrando a flag:

![Flag_explícita](https://github.com/user-attachments/assets/fc166825-a225-41d7-a0af-caa7730d2a93)


>`picoCTF{caesar_d3cr9pt3d_f0212758}`
 
