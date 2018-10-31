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
- **Atenção:** Valores numericamente maiores podem "puxar" o cálculo de similaridade para o seu lado. Por isso é bom sempre normalizar esses valores entre algum intervalo padrão, como 0~1 ou 0~100 por exemplo.\
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
