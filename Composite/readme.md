# Template Composite

Compor objetos em estruturas que permitam aos clientes tratarem de maneira uniforme objetos individuais e composição de objetos.
Algumas aplicações exigem que o mesmo tratamento seja dado tanto a objetos simples como estruturas formadas por vários objetos.
O padrão Composite descreve como usar a composição de forma que os clientes não precisem distinguir objetos simples de estruturas complexas. 

#### Aplicabilidade
Representação de hierarquias todo-parte de objetos.
Clientes devem ser capazes de ignorar a diferença entre composições de objetos e objetos individuais. 

#### Conseqüências
Referências explícitas aos pais.
Compartilhamento de componentes
Maximização da interface de Component

#### Componente
Declara a interface para objetos nessa composição.
Implementa o comportamento padrão para a interface comum à todas as classes.
Declara uma interface para acessar os componentes-filho.
(Opcional) - Define uma interface para acessar os componentes-pai na estrutura recursiva, e a implementa se for apropriado.

#### Folha
Representa o objeto folha na composição. A folha não tem nenhum componente-filho.
Define o comportamento para objetos primitivos na composição.
Herda todos os métodos de Component porém só implementa de fato os que lhe interessam,neste caso o método Operation, nos outros são inseridos exceções que serão geradas em tempo de execução.

#### Cliente
Manipula objetos da composição através da interface do Componente.

Exemplo de como deve ser uma estrutura Composite:

![Estrutura](https://github.com/Felipecasadia/Estudos/blob/master/Composite/Estrutura%20Composite.png)
