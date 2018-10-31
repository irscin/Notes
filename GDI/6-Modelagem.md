Modelagem do diagrama ER para tabelas normalizadas têm regras úteis a serem seguidas. 

1. Para cada entidade comum, criar uma relação com os atributos dessa entidade, exceto os multivalorados. 

2. Entidades fracas têm todos os seus atributos, mais a chave primária da entidade forte a qual a entidade fraca é ligada. 

3. Em relacionamentos 1:1 coloca-se todos os atributos de uma das entidades participantes (exceto os multivalorados) e põe-se a chave primária da outra entidade participante do relacionamento como chave estrangeira. 

4. Em relacionamentos 1:N coloca-se todos os atributos da entidade do lado N da relação e as chaves primárias das entidades do lado 1 como chaves estrangeiras. 

5. Em relacionamentos N:M deve-se criar uma nova relação para representar o relacionamento. Essa nova relação deve ter as chaves primárias dos relacionamentos participantes e eventuais atributos do relacionamento. Deve-se criar uma nova relação para guardar atributos multivalorados. Essa nova relação deve ter os atributos em si e a chave primária da entidade a qual eles pertencem. 