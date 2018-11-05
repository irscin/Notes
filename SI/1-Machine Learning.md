**Modelo de Machine Learning**\
Formalizando o modelo de aprendizado de máquina, temos um input, um output, um dataset com tuplas de inputs e outputs, uma função alvo e uma hipótese.
Usamos os exemplos e um conjunto de possíveis hipóteses como input do algoritmo de aprendizado, que tem como output a hipótese final. O algoritmo e o conjunto de hipóteses possíveis são chamados de modelo de aprendizagem.\
**Regiões de Separação**
Umas das formas de resolver um problema de ML é utilizando combinações lineares das variáveis envolvidas e então separando-as de acordo com uma fronteira.\
![Exemplo de Separação Linear](https://raw.githubusercontent.com/LinuxUserIRS/Notes/master/SI/Resources/SeparacaoLinear.png)\
Nem sempre os elementos irão se separar perfeitamente de forma que seja possível traçar uma linha clara entre os grupos, para isso, podemos umas o teorema de Cover, que diz que quando aumentamos as dimensões das variáveis, elas tendem a se linearizar.
**Fases da ML**
- Fase de Treinamento
É nessa fase que o algoritmo de ML usa seu dataset para ajustar seus parâmetros.
- Fase de Testes
É onde o seu desempenho é avaliado utilizando um conjunto de dados de teste.
**Paradigmas de ML**
- Simbólico
Constrói uma representação simbólica de um conceito atráves de análises de exmplos e contraexemplos.
Algumas formas comuns incluem:
1. Expressões Lógicas
2. Árvores de Decisão
3. Regras de Produção
4. Redes Semânticas
- Baseado em Instâncias
Classificam dados baseado em dados similares cuja a classificação já é conhecida.
Ex:
1. Raciocínio de Casos
2. K-Vizinhos mais próximos
- Paradigma Estático
Constrói um modelo estático do problema, normalmente usando a **Regra de Bayes**
Podem ser:
1. Paramétricas
2. Semi-paramétricas
3. Não paramétricas
- Paradigma evolucionário
Usam modelos computacionais baseados na teoria da evolução.
- Paradigma conexionista
Frande númro de unidades de processamento conectadas entre si.
**Tipos de ML**
- Aprendizado supervisionado
O algoritmo recebe o dataset "mastigadinho", já com todos os seus elementos classificados e precisa, a partir daí, ser capaz de classificar novos elementos.
- Aprendizado não supervisionado
É dado um dataset sem qualquer informação adicional, o algoritmo então precisa precisa separar esses elementos por conta própria e então enteder como esses grupos se relacionam ou o que representam.
