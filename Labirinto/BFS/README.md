<div style="display: inline-block;">
<img src="https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white"/> 
<img src="https://img.shields.io/badge/Visual_Studio_Code-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white"/> 
<img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white"/> 
</a> 
</div>

# Breadth-first search-BFS
<div align="justify">
 A busca em largura (BFS) é um algoritmo utilizado para percorrer ou buscar itens dentro das estruturas de dados grafos ou árvores. Como característica temos que a busca sempre ocorre nos filhos ou nós mais próximos ao nó pelo qual a busca foi iniciada. Vamos entender isso melhor no decorrer desse artigo. A imagem abaixo exemplifica a busca em largura em grafo.

 A busca em largura pode ser implementada de várias formas. As mais utilizadas são através de recursão, que utiliza pilha (LIFO), ou iterativamente, através de uma fila (FIFO), que será o caso desse algoritmo.
</div>

## A Estrutura Fila Dinâmica
<div align="justify">
 Na estrutura fila dinâmica, lidamos com ponteiros, criamos blocos em memória, tratamos do acesso e navegação utilizando o ponteiro próximo ( prox ) e, com isso, definimos e manipulamos os ponteiros frente e fundo sob um modelo circular, como na imagem abaixo. 

<div align="center">
 <p> </p>
 <img src="img/fila.png" alt=RepresentaçãoFila>
 <p> </p>
</div>

  Para inserções, utilizamos sempre o ponteiro de fundo. Em contra partida, utilizamos o ponteiro de frente para as remoções. Essa característica torna esse modelo de estrutura em um modelo do tipo First In First Out - FIFO. Mesma regra encontrada em sua vertente estática [vide git](https://github.com/mpiress/linear_queue).

 Com relação às estruturas dinâmicas básicas de lista e pilha, há uma diferença sutil de construção que deve ser observado na fila, a ligação do último elemento inserido à "cabeça" da estrutura. Essa modificação fará com que a estrutura se comporte exatamente da mesma forma de sua variante estática,ou seja, de forma circular.
</div>

## Algoritimo
<div align="justify">
Em nosso algoritmo, utilizaremos o método BFS para encontrar o caminho de saída de uma matriz quadrática que é um labirinto, onde as posições poderão ter dois valores possíveis:
 <ul>
  <li> 0 - Representa os lugares onde pode se passar;</li>
  <li> 1 - Representa os lugares onde NÃO pode se passar, ou seja, as barreiras do labirinto.</li>
 </ul>

Lê-se um arquivo .txt onde:
<ul>
 <li> A primeira linha do arquivo é o tamanho da matriz, e apresenta o número de linhas e número de colunas, respectivamente;</li>
 <li> As outras linhas são as posições onde são encontradas as barreiras do labirinto, ou seja, os locais por onde ele não pode passar.</li>
</ul>
 
 >*Observações:* 
 > - A primeira e a última posição da matriz NÃO podem ter o valor 1 (valor de barreira)
 > - O método de leitura do arquivo permite apenas matrizes menores ou iguais a 9.
>

 Como exemplo, temos o arquivo abaixo, o programa irá ler esse arquivo "Matriz.txt":
 <div style="display: inline-block;" align="center">
  <p> </p>
 <img src=img/arquivo.png alt=arquivo.txt>
  <p> </p>
 </div>
 
 A matriz gerada a partir do arquivo lido será:
  <div style="display: inline-block;" align="center">
   <p> </p>
 <img src=img/matriz.png alt=matriz> 
   <p> </p>
 </div>

Na primeira etapa da execução do algoritmo, ele enfileira a posição 0, 0 (o início) da matriz. Então, ele confere e enfileira as posições adjacentes disponíveis a ele ([0, 1] e [1, 0]). Nesse processo, as posições que já foram percorridas, recebem o valor 2 e não podem mais ser percorridas. 
 
Em sequência, ele desenfilera a cabeça da fila e olha a próxima posição, que seria a nova cabeça. Esse processo de desenfileirar e olhar a cabeça seguinte se repete até que se alcance a posição [N, N] da matriz. Como dito anteriormente, a forma encontrada para evitar que o algoritmo passe pela mesma posição repetidas vezes, é setando um novo valor para a posição já visitada e enfileirada, um valor diferente de 0.

O algoritmo imprime a variável que conta o número de interações que ele necessitou para conseguir alcançar o final do labirinto.
Por fim, imprime a matriz novamente, mostrando, a partir dos 2 colocados nas posições já percorridas, por onde o algoritmo passou no labirinto.
 
>*Interações:* 
 > - Variável que define o número de vezes que o algoritmo teve que conferir alguma posição, é incrementado +1 toda vez que uma posição é enfileirada. Dessa forma, o primeiro e o último valor também são contabilizados.
>
</div>

# Compilação e Execução

O algoritmo BFS disponibilizado possui um arquivo Makefile que realiza todo o procedimento de compilação e execução. Para tanto, temos as seguintes diretrizes de execução:

<div>

| Comando                |  Função                                                                                           |
| -----------------------| ------------------------------------------------------------------------------------------------- |
|  `make clean`          | Apaga a última compilação realizada contida na pasta build                                        |
|  `make`                | Executa a compilação do programa utilizando o gcc, e o resultado vai para a pasta build           |
|  `make run`            | Executa o programa da pasta build após a realização da compilação                                 |

</div>

# Contatos

<div>
<p align="justify"> Thaissa Vitória</p>
<a href="https://t.me/thaissadaldegan">
<img align="center"  src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white"/> 

<a href="https://www.linkedin.com/in/thaissa-vitoria-daldegan-6a84b9153/">
<img align="center"  src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>
</div>


<div>
<p align="justify"> Bárbara Gualberto</p>
<a href="https://t.me/barbrinas">
<img align="center" src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white"/> 

<a href="https://www.linkedin.com/in/barbara-gualberto/">
<img align="center" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>
</div>



