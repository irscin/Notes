**Tipos**\
Tipos são definições de um objeto, são como classes. Eles não armazenam informação em si, apenas modelam os atributos e os métodos de um tipo.\
É separado em:
- Especificação (Público)
  - Declaração de Atributos
  - Declaração de Métodos
- Corpo (Privado)
  - Implementação de Métodos
Primeiramente se definem os tipos mais primitivos, que serão usados para compor os tipos mais complexos.
Por exemplo, um tipo endereço e um tipo telefone que fazem parte de um tipo empresa.\
**Tipos e Palavras Chave**\
**NOT FINAL:** Não permite criação de subtipos (É o default de um método, já um objeto é, por default, FINAL)\
**NOT INSTANTIABLE:** Não permite a instanciação em tabelas, mas pode ser usado na declaração de outros tipos.\
**Métodos**\
- MEMBER: Permite acesso aos dados da instância do objeto.
- MAP ou ORDER: Realiza comparações.
- CONSTRUCTOR: Cria uma nova instância daquele objeto, tem o mesmo nome do tipo e é criado implicitamente. (É permitido overloading)
Um tipo de objeto sempre tem um construtor, pode ter nenhum ou mais métodos membros e um MAP ou um MEMBER, mas não ambos.\
**Diferenças entre MAP e ORDER**\
**MAP**
- Não precisa de parâmetro
- Compara vários objetos
- Só pode ser declarado em subtipo se houver sido declarado no supertipo
**ORDER**\
- Não pode ser definido em subtipos
- É menos eficiente que MAPs
- Exige como parâmetro o objeto ao qual será comparado
