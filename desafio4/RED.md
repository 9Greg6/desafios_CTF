# RED
###### Resolvido por Gabriel Gregório de Oliveira
> Esse CTF é sobre análise de informações ocultas em imagens
## Sobre o desafio
O desafio fornece uma descrição "RED, RED, RED, RED" e uma imagem (https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png) a ser analisada.
## Resolução
Abre-se a imagem fornecida e nada é possível encontrar em primeira análise:

[![red.png](https://i.postimg.cc/CKXgRwyJ/red.png)](https://postimg.cc/XZfhhSYy)

Sendo assim, utiliza-se o CyberChef para fazer pesquisa minuciosa pelo arquivo da foto. Faz-se upload do arquivo.png e é necessário a ferramenta Extract LSB, devidamente configurada como R,G,B,A (RED, GREEN, BLUE, ALPHA), dica fornecida na questão. Então, serão extraídos os bits da imagem e a configuração feita trará caracteres codificados em base64:

[![Captura-de-tela-2025-05-07-224151.png](https://i.postimg.cc/BZyKJKw1/Captura-de-tela-2025-05-07-224151.png)](https://postimg.cc/xqvCRcQ0)

Nota-se a repetição de: "cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==", assim utilizando a ferramenta From Base64, tem-se a flag:

[![Flag4.png](https://i.postimg.cc/CKLGRVCZ/Flag4.png)](https://postimg.cc/RWy6YyD9)


>`picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}`
 
