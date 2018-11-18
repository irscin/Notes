**Desafios da classificação de imagens**\
- Variação de ponto de vista
- Variação intraclasse
- Variação de iluminação
- Deformação
- Oclusão
- Ruído de fundo
-Escala\
**Modelos Lineares**\
Pense nas instâncias de treinamento como pontos em um espaço n-dimensional, onde cada dimensão é uma feature. Alguns classificadores agem como minimizadores de função de perda, onde o objetivo do classificador é reduzir a distância entre a classificação que ele deu para uma instância e a classificação correta da instância.\
w.x+b>t onde w é o peso, x o input, b o bias e t o threshold. Para simplificar os algoritmos, podemos nos livrar do threshold escrevendo: w.x+b-t>0 e colocando o threshold em 0. Podemos simplificar ainda mais, colocando o bias e uma feature adicional, ficando assim com apenas w.x>0.\
A função do bias, é permitir que as linhas (ou planos) de separação entre as categorias de instâncias possam se mover para os lados, possam shiftar. Movimento que não é possível sem ele. Já o peso, sever para ajustar a inclinação das retas (ou planos).