<div style="display: inline-block;">
<img src="https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white"/> 
<img src="https://img.shields.io/badge/Visual_Studio_Code-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white"/> 
<img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white"/> 
</a> 
</div>

# Depth-First Search-DFS
<div align="justify">
 A busca em profundidade (DFS) é um algoritmo utilizado para percorrer ou buscar itens dentro das estruturas de dados grafos ou árvores. Sua característica básica é percorrer todos os nós filhos ao nó raiz o mais profundo possível para somente depois retroceder. Iremos compreender a aplicação dessa mecânica no decorrer desse algoritmo.
	<p> </p>	
 Existem várias formas de implementar uma busca em profundidade. Pela natureza de percorrer o grafo ou árvore enquanto houverem filhos não visitados, uma solução natural é utilizar recursão. Outra abordagem é utilizar um algoritmo iterativo e utilizar uma pilha (LIFO) para controlar os nós a serem visitados.
</div>

## A Estrutura Pilha
<div align="justify">
A pilha possue uma regra básica que deve ser obedecida, essa se refere a forma como inserimos e removemos elementos dessa estrutura. Antes de iniciarmos essa discussão, observe um exemplo ilustrativo desse tipo de dados na figura abaixo.

<div align="center">
	<p> </p>
	<img src="img/pilha.png"/> 
	<p> </p>
</div>

Observe que nesse tipo de estrutura há apenas um <b>único ponteiro</b> chamado <b>Topo</b>. Os métodos associados ao tipo pilha, os quais impõem as regras, são chamados PUSH (i.e., empilhar) e POP (i.e., desempilhar).

>Logo, temos como regra básica dessa estrutura: 
> 1. O último elemento que entra sempre será o primeiro a ser removido. 

Como a pilha é definida a partir de um vetor, muitas das caracteristicas de implementação observadas no tipo lista são aproveitados para compor sua execução. A diferença está apenas na composição da regra de manipulação, o que as diferencia em termos de execução. 

</div>

## Algoritimo
<div align="justify">
Em nosso algoritmo, utilizaremos o método DFS para encontrar o caminho de saída de uma matriz quadrática que é um labirinto, onde as posições poderão ter dois valores possíveis:
 <ul>
  <li> 0 - Representa os lugares onde pode se passar;</li>
  <li> 1 - Representa os lugares onde NÃO pode se passar, as barreiras do labirinto.</li>
 </ul>

Lê-se um arquivo .txt onde:
<ul>
 <li> A primeira linha é o tamanho da matriz, representando o número de linhas e número de colunas, respectivamente;</li>
 <li> As outras linhas são as posições onde são encontradas as barreiras do labirinto.</li>
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
Na primeira etapa da execução do algoritmo, ele empilha a posição 0, 0 (o início) da matriz. Então, ele confere a posição abaixo e percorre ela até bater em um obstáculo ou no fim da matriz, empilhando todas as posições percorridas. Nesse processo, as posições que já foram percorridas, recebem o valor 2 e não podem mais ser percorridas.
	
As posições que apresentam uma barreira fazem com que o algoritmo percorra outro caminho. Seguindo a ordem de olhar para baixo, direita, esquerda e acima, caso necessário. Caso o algoritmo se encontre preso entre barreiras, ele desempilha o topo da matriz e atribui o valor 1 a ela, dessa forma não passando mais por tal caminho, e em busca de outra posição para que ele possa percorrer.

Em sequência, ele desenfilera a cabeça da fila e olha a próxima posição, que seria a nova cabeça. Esse processo de desenfileirar e olhar a cabeça seguinte se repete até que se alcance a posição [N, N] da matriz. Como dito anteriormente, a forma encontrada para evitar que o algoritmo passe pela mesma posição repetidas vezes, é setando um novo valor para a posição já visitada e enfileirada, um valor diferente de 0.

O algoritmo imprime a variável que conta o número de interações que ele necessitou para conseguir alcançar o final do labirinto.
Por fim, imprime a matriz novamente, mostrando, a partir dos 2 colocados nas posições já percorridas, por onde o algoritmo passou no labirinto.
 
>*Interações:* 
 > - Variável que define o número de vezes que o algoritmo teve que conferir alguma posição. É incrementado +1 toda vez que uma posição é empilhada, dessa forma, o primeiro e o último valor também são contabilizados.
>
</div>

# Compilação e Execução

O algoritmo DFS disponibilizado possui um arquivo Makefile que realiza todo o procedimento de compilação e execução. Para tanto, temos as seguintes diretrizes de execução:

<div>

| Comando                |  Função                                                                                           |
| -----------------------| ------------------------------------------------------------------------------------------------- |
|  `make clean`          | Apaga a última compilação realizada contida na pasta build                                        |
|  `make`                | Executa a compilação do programa utilizando o gcc, e o resultado vai para a pasta build           |
|  `make run`            | Executa o programa da pasta build após a realização da compilação                                 |

</div>

# Contatos

<div style="display: inline-block;">
 <p align="justify"> Thaissa Vitória</p>
<a href="https://t.me/thaissadaldegan">
<img align="center" src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white"/> 
</a>

<a href="https://www.linkedin.com/in/thaissa-vitoria-daldegan-6a84b9153/">
<img align="center" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

</div>


<div style="display: inline-block;">
 <p align="justify">Bárbara Gualberto</p>
<a href="https://t.me/barbrinas">
<img align="center" src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white"/> 
</a>

<a href="https://www.linkedin.com/in/barbara-gualberto/">
<img align="center" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

</div>

