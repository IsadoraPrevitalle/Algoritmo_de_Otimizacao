# **Otimização por Colônia de Formigas**
A Otimização por Colônia de Formigas, *Ant Colony Optimization* - ACO, é uma técnica inspirada na busca por fonte de alimento realizada por colônias de formigas, a qual é aplicada a problemas discretos de otimização.

A metáfora central da ACO reside no mecanismo de comunicação indireta através de sinais químicos (feromônios), empregado por muitas espécies de formigas sociais, na busca por fontes de alimentos. As formigas buscam aleatoriamente por fontes de alimento próximas aos seus ninhos, sendo que a “força” da trilha de feromônio cresce rapidamente para fontes próximas e para trilhas mais curtas. As trilhas surgem ao longo do tempo, como uma memória coletiva, formando uma rota entre a colônia e a fonte de alimento (Figura 1).

Figura 1. Depósito de feromônio entre o ninho (N) e a fonte de alimento (F)

<img src="https://drive.google.com/uc?id=1oCFZzpApf-ctuWxZ_ZiqmcinVMr3UvDC" width="500">

# **Seleção e Formulação do Problema**

O primeiro passo para utilizar a ACO é mapear o problema selecionado para um grafo no qual a rota (trilha mais forte de feromônios) representa a solução do problema. A tarefa é encontrar um caminho ótimo através do grafo.

Dessa forma, nada mais natural do que escolher o clássico **Problema do Caixeiro Viajante**. O **Problema do Caixeiro Viajante**, ou *Travelling Salesman Problem*, reside no objetivo de encontrar a menor rota possível para visitar um conjunto de cidades, passando por cada uma delas uma única vez, e retornar à origem.
* O espaço de estados para esse problema pode ser representado por um grafo completamente conexo. Os vértices são as cidades e as arestas representam vias entre cidades, havendo uma distância (custo) associada.
* O trecho de código abaixo gera um grafo para o problema do caixeiro viajante.
  * O usuário pode escolher o número de cidades;
  * O grafo é gerado em uma matriz bidimensional, sendo as distâncias valores inteiros aleatórios no intervalo [10, 100].
    
# **Processamento da ACO**
A Figura 2 apresenta o pseudocódigo simplifica do algoritmo da ACO. Em cada iteração do algoritmo o feromônio em cada aresta, além de atualizado com o depósito, sofre evaporação.

Figura 2. Pseudocódigo da ACO

<img src="https://drive.google.com/uc?id=1gjVPxanOnvi4Pyge86hZzlJCgzzqbMG9" width="700">

No pacote ACO-Pants, esse processamento do algoritmo é transparente ao usuário.
