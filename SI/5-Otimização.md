Temos nossa função de perda, queremos um algoritmo que possa variar os parâmetros para minimizar essa perda e, consequentemente, melhorar a taxa de acerto dos modelos de previsão.\
**Estratégia 1:** Busca aleatória. Péssima estratégia, obviamente, é custosa e demorada, embora até possa apresentar bons resultados, não vale o esforço.\
**Estratégia 2:** Seguir a inclinação da função que descreve a perda. Em uma dimensão, temos uma derivada, em duas ou mais, um gradiente, que é um vetor de derivadas parciais.\
Temos duas formas de analisar os gradientes:
- Numericamente: Podemos somar pequenas variações nos outputs da função de perda e então calcular a derivada para cada output, no final, teremos um vetor de derivadas, que será nosso gradiente.
- Analiticamente: Visto que a perda é uma função do peso W, podemos analisar direto a esquação, sem necessariamente precisar calcular valores.
- Comparativo:
Gradiente Numérico: Apxoimado, lento, fácil de implementar\
Gradiente Analítico: Exato, Rápido, Sujeito a erros 
