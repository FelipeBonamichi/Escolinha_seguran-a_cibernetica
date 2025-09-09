
###### Solved by @felipebonamicheelias

> This is a CTF about Cryptography

## Desafio: Flag Hunters
#### Introdução

Este desafio da plataforma [picoCTF](https://play.picoctf.org/)
envolve análise de criptografia em muitiplas camadas. O objetivo é analizar e descobrir a ordem certa para decodificar


#### Análise Inicial

O desafio fornecia uma **string codificada** que precisava ser analisada para encontrar a flag. A ideia principal do desafio era clara: **engaging in various decoding processes is of u* — ou seja, aplicar diferentes processos de decodificação é essencial para revelar o conteúdo oculto.

As informações fornecidas pelo desafio incluíam:

- Um texto aparentemente ilegível, indicando que havia algum tipo de codificação.
- A necessidade de interpretar corretamente a sequência de codificações para revelar a flag.

A partir desses elementos, ficou claro que o desafio envolvia **decodificação em múltiplas etapas**, e que o primeiro passo seria identificar o tipo de codificação utilizada.

#### Solução

A solução consistiu em aplicar as decodificações em sequência, respeitando a ordem das camadas. Primeiro, utilizamos a ferramenta [dcode.fr](https://www.dcode.fr/base64-encoder-decoder) para realizar a primeira decodificação Base64, inserindo o texto na caixa de decodificação e obtendo a primeira saída. Em seguida, aplicamos novamente Base64 sobre a saída obtida, revelando o texto cifrado com César. Por fim, utilizando a ferramenta [dcode.fr Caesar Cipher](https://www.dcode.fr/caesar-cipher), testamos diferentes deslocamentos até que a mensagem fizesse sentido, revelando finalmente a flag oculta.



#### Conclusão

Flag:
>`	picoCTF{caesar_d3cr9pt3d_ea60e00b}`

Este desafio demonstra a importância de compreender **camadas de codificação** e a ordem correta de decodificação.  

Além disso, reforça conceitos de **criptografia básica e decodificação em CTFs**, mostrando como múltiplas técnicas podem ser combinadas para ocultar informações e como ferramentas online podem acelerar a análise de mensagens criptografadas.