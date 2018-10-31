- Problemas resolvidos no passado são **instâncias**, que são recuperadas e adaptadas para novos problemas.
- Sempre que uma nova instância é adicionada, é computada uma função objetivo com base nas instâncias passadas.
- É uma abordagem incremental.\
**Lazy Learning**\
Método de aprendizagem em que a generalização dos dados de treinamento é adiada ao máximo, até que uma consula seja feita ao sistema.\
**Eager Learning**\
É o oposto do Lazy Learning, tenta generalizar antes que seja feita uma consulta.\
**Algoritmo k-NN**
- Todas as instâncias são pontos em um espaço n-dimensional.
- A vizinhança é definida por uma função de distância, ou similaridade
- Maior similridade=Menor distância
- Uma nova instância é classificada de acordo com os vizinhos mais próximos
- A saída da função de cálculo de similaridade pode ser discreta ou um valor contínuo, calculado a partir da ponderação das saídas mais próximas
- **Atenção:** Valores numericamente maiores podem "puxar" o cálculo de similaridade para o seu lado. Por isso é bom sempre normalizar esses valores entre algum intervalo padrão, como (0,1) ou (0,100) por exemplo.\
**Distância de Hamming**\
Usada para atributos categóricos.\
![Distância de Hamming](https://raw.githubusercontent.com/LinuxUserIRS/Notes/master/SI/Resources/DistanciaHamming.png)\
**Distância entre valores faltantes**
- Atributos categóricos: dist=1.
- Atributos numéricos:
  - Se ambos os atributos comparados estão faltando, então: dist=1.
  - Se apenas um dos valores está faltando, então: dist=máx(tamanho normalizado do atributo presente, 1-tamanho normalizado do atributo presente).\
**Escolha dos valores de K**\
O valor de K pode ter grande influência sobre a classificação da nova instância. Veja:\
![Classificação quando K=3](https://raw.githubusercontent.com/LinuxUserIRS/Notes/master/SI/Resources/K=3.png)\
![Classificação quando K=5](https://raw.githubusercontent.com/LinuxUserIRS/Notes/master/SI/Resources/K=5.png)\
Sendo assim, precisamos escolher bem o valor de K.
- Valores baixos:
  - Baixo custo computacional.
  - Suscetível à influência de valores ruidosos
- Valores altos:
  - Aumentam a contribução de valores pouco similares e, sendo assim, irrelevantes.
  - Mais resistente ao ruído
- Frequentemente escolhido na tentativa e erro.\
**Empate na classificação de uma classe**
Quando ocorrer um empate, repete-se o algoritmo com k-1. Em caso de novo empate, isso é repetido até que se tenha uma resposta.\
**Uso de pesos**
- Instâncias mais distantes da instância a ser classificada têm uma influência menor na classificação.
- Se os atributos relevantes da entrada não forem bem definidos, isso pode levar a resultados ruins.
Por exemplo, temos 10 atributos nas instâncias de exemplo, mas apenas 2 atributos são relevantes, se não filtrarmos isso, os outros 8 atributos podem interferir na classificação da nova instância.\
**Discussão**
- Vantagens:
  - Fácil de implementar
  - Não requer etapa de treinamento
  - Bom para datasets médios e pequenos
  - Paralelizável
- Desvantagens
  - Sensível a ruído, elementos irrelevantes ou redundantes
  - Custo computacional e de armazenamento imprátco em algumas situações
