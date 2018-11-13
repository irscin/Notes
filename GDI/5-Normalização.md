- Normalização é uma técnica necessária para garantir:  
1 – A eficiência das operações no DB. 
2 – Menor consumo de espaço de armazenamento 
3 - Representação mais fiel do mundo por parte do modelo. 

- Dependência Funcional: Sejam os atributos X e Y, há dependência funcional de X para Y (X -> Y) se com um valor de X, se chega em Y e com apenas um valor só. 

- Dependência Funcional Total: Funciona nos dois sentidos. X <- -> Y 

- Dependência Transitiva: X -> Y -> Y então X -> Z 

- 1NF: Uma relação está na 1NF se todos os seus atributos são atômicos. 

- Regra Normalização - 1NF: Separar os componentes de um atributo até que tudo esteja atômico. 

- 2NF: Todo atributo não chave é plenamente dependente da chave primária. 

- Regra Normalização - 2NF: Para cada subconjunto de atributos que formam a chave primária, separar em relações com esses atributos como chave primária. Cada nova relação deve ser composta pelo subconjunto mínimo. 

- 3NF: Nenhum atributo não chave é transitivamente dependente da chave primária. 

- Regra Normalização - 3NF: Cada atributo que não chave candidata, remover da relação os atributos que dependem dele para criar uma nova relação em que esse atributo é chave primária. 

- De uma maneira mais legível pra mim: Todas as colunas daquela tabela precisam depender da chave primária daquela tabela. Se houver uma coluna que depende de outra coluna que não seja chave primária, elas merecem sua própria tabela e devem ser referenciadas como chave estrangeira na primeira tabela. 