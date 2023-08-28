# Descrição 

Este trabalho foi desenvolvido durante a disciplina de Circuitos Digitais, ministrada por Ramon Nepomuceno [Ramon Nepomuceno](https://github.com/ramonn76) na Universidade Federal do Cariri (UFCA).

Consiste em um jogo em que os jogadores têm que adivinhar um número secreto. Para iniciar o jogo, clique no botão "Jogar" em 1. Depois disso, basta ficar apertando o botão do jogador, e o jogo indicará se o seu palpite é maior, menor ou igual. Se for igual, você acertou, obtendo o resultado final.



![Imagem do Jogo](/img/8.png)


## Funcionamento 

### Display 

Para ativar o display de 7 segmentos, foram criados 7 chips, cada um com o seu mapa de Karnaugh. A tabela abaixo mostra como foi feito para o primeiro segmento.

| AB / CD | 00 | 01 | 11 | 10 |
| --------| - | - | - | - |
| 00 | 1 | 1 | 0 | 1 
| 01 | 1 | 0 | 1 | 1
|11 | 1 | 1 | 0 | 0 
| 10 | 1 | 0 | 0 | 1

A partir disso, foi gerada a seguinte equação:

$\overline{AB}$ + $\overline{ACD}$ + ${CD}$$\overline{A}$ + ${AD}$$\overline{C}$ + $\overline{BD}$

E o circuito foi implementado da seguinte forma:


![Texto alternativo](/img/1.png)


Esse processo foi repetido para todos os segmentos, resultando no display final:


![Texto alternativo](/img/2.png)

### As operações 

Devido ao tamanho do mapa de Karnaugh ser grande para esse problema, pesquisei na internet e encontrei este [video](https://www.youtube.com/watch?v=wgje9eH3TT0&t=1032s). Isso me permitiu simplificar o circuito.

O circuito do vídeo original era:


![Texto alternativo](/img/3.png)


E foi simplificado para:


![Texto alternativo](/img/4.png)

Os circuitos dos valores menores foram removidos, pois se o valor não é igual nem maior, então ele deve ser menor.

### MUX 

O multiplexador de 1 bit foi ensinado em sala de aula:


![Texto alternativo](/img/5.png)


E o de 4 bits


![Texto alternativo](/img/6.png)

### Multiplexador

O multiplexador é a junção de vários circuitos:


![Texto alternativo](/img/7.png)