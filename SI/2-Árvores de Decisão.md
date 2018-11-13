**Árvores de Decisão**
Funcionam basicmente separando valores em suas bifurcações através de vários critérios ate que se atinja a precisão desejada ou se esgotem as variáveis disponíveis sobre as quais fazer decisões. Árvores de decisão são uma abordagem simples, porém efetivas quando se tratando de conjuntos fixos de variáveis e cujo os outputs são limitados, de preferência, binários. Mas també podem funcionar para atributos contínuos, definindo-se faixas de valores, por exemplo.
Algumas aplicações comuns incluem: análise de crédito e dignóstico de pacientes e equipamentos.\
[Uma Introdução Visual ao Aprendizado de Máquina](http://www.r2d3.us/uma-introducao-visual-ao-aprendizado-de-maquina-1/)\
**Algoritmo ID3**
O algoritmo vai construindo a árvore de cima para baixo, testando os atributos de forma que os atributos mais importantes fiquem no nós superiores. Esse processo é repetido até que a árvore esteja completa.\
**Entropia e Ganho de Informação**
Entropia pode ser definida como uma medida de incerteza.
![Equação da Entropia](https://raw.githubusercontent.com/LinuxUserIRS/Notes/master/SI/Resources/Entropia.png)\
Levando em consideração esta defnição de entropia, podemos partir para a definição de ganho de informação, que é basicamente o quão bom um determinado atributo é em redzir a entropia do sistema.
![Ganho de Entropia](https://raw.githubusercontent.com/LinuxUserIRS/Notes/master/SI/Resources/GanhoDeEntropia.png)\
Sendo assim, o algoritmo ID3 escolhe como nó raiz o atributo que melhor organiza os dados e segue escolhendo dessa forma até que todos os atributos tenham se esgotado ou que a árvore consiga classificar os dados com precisão suficiente.\
**Overfitting**
O efeito que algritmos possuem de classificar dados do dataset de treinamento melhor que o dataset de testes. Isso ocorre por várias razões, dataset de treino pequeno ou ruidoso ou árvore complexa demais.
![Ganho de Entropia](https://raw.githubusercontent.com/LinuxUserIRS/Notes/master/SI/Resources/Overfitting.png)\
**Evitando o Overftting**
- Parar de crescer a árvore antes que ela consiga classificar perfeitamente todos os dados do dataset.
  - Usamos um dataset diferente do dataset de treinamento, o dataset de validação que é usado para medir o desempenho de vários tamanhos de árvore possíveis e então é escolhido o melhor tamanho.
- Permitir que árvore cresça até classificar perfeitamente o dataset, mas podá-la depois.
  - Para podar, remove-se uma sub-árvore de um deerminado nó e a transforma-se em folha. A classificação desta folha será a classificação mais comum dada por aquela sub-árvore a seus elementos. A poda só é feita, logicamente, se a árvore resultante for melhor que a anterior nos testes de validação.
