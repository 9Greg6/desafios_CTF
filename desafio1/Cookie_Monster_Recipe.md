# Cookie Monster Secret Recipe
Resolvido por Gabriel Gregório de Oliveira
> Este CTF é sobre exploração web, inspeção de elementos e cookies
## Sobre o desafio
A descrição do desafio sugere que uma receita de biscoitos (flag da questão) seja encontrada no página "Cookie Monster" fornecida: http://verbal-sleep.picoctf.net:60118/.
## Resolução
Inicialmente, acessando o site é pedido um usuário e senha, não sendo importantes para a resolução da questão.

Como nenhuma informação a mais pode ser obtida se faz necessário analisar os elementos que compõe essa página, atento a dica explícita no enunciado da questão, "Cookies". Dessa forma, com o atalho F12 inspeciona-se o site buscando informações sobre os tais cookies, encontrando-os em "Application":
[![Inspe-o.png](https://i.postimg.cc/g0Dg7Dsh/Inspe-o.png)](https://postimg.cc/NyK89RWG)


Nota-se que encontrando os cookies referentes a URL da página, a recipe_secret (receita secreta) aparece como um amaranhado de caracteres, fato que não configura a flag no formato correto, mas sim em formato base64. Com isso, alguma operação a ser feita com o que foi achado mostrará a bandeira.
Utilizando o base64 decode, podemos decodificar os caracteres e encontrar a flag:
[![Decode.png](https://i.postimg.cc/FRHTXLCB/Decode.png)](https://postimg.cc/KKCPnR2P)



>`picoCTF{c00k1e_m0nster_l0ves_c00kies_A964A134}`
 
