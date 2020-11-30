# Template Memento
O Observer é um padrão de projeto de software que define uma dependência um-para-muitos entre objetos de modo que quando um objeto muda o estado, todos seus dependentes são notificados e atualizados automaticamente. Permite que objetos interessados sejam avisados da mudança de estado ou outros eventos ocorrendo num outro objeto.


#### Motivação
O Padrão Comportamental Memento possui uma grande gama de aplicações onde é necessário a recuperação de um estado anterior de um objeto como um todo, qualquer tipo de editor precisa oferecer uma maneira de desfazer ações como restaurar imagens, textos etc. Para isso, o padrão Memento procura recuperar o estado anterior dessas ações e copiar os mesmos para um objeto a ser restaurado.


#### Aplicabilidade 
O objeto representado na classe Originador cria um novo memento a partir de si próprio, é ele que vai controlar toda a execução do Padrão Memento, criando uma nova instância da classe Armazenador, sempre que haja alguma modificação derivada de ações do sistema e de seu funcionamento padrão, o Originador irá criar um novo Memento, externalizando seu estado interno para um novo objeto que se tornará o Memento que será armazenado para posterior restauração. Além dos métodos e atributos próprios do objeto a ser restaurado, o Originador conta com um atributo que represente o estado atual do mesmo, métodos para definir e atribuir o estado, e métodos para salvar e solicitar o estado a partir do Memento.

Com o estado salvo no Objeto Memento, o Originador volta suas atenções para o Armazenador, quando o método que aciona a ação de modificação é invocado, o Memento é criado e adicionado no Armazenador, que, a partir de agora guardará os Mementos em uma pilha, usando o LIFO, para tanto, o Armazenador possui uma lista do tipo do Memento, possui métodos para adicionar um novo Memento e para acessar o ultimo adicionado na pilha do Armazenador, quando o ultimo for retirado, o topo da lista será o Memento com o estado anterior ao que foi solicitado, e assim por diante, até que não haja mais Mementos para serem acessados, nesse momento deve ser lançada uma exceção.

#### Consequências
O problema do Memento é que por ele sempre estar guardando o estado do objeto, ele pode guardar objetos demais e de maneira desnecessária e assim utilizando muito da memória da máquina.


#### Estrutura

![Estrutura](https://github.com/Felipecasadia/Estudos/blob/master/Memento/Memento.jpg)

#### Exemplo de código:

[Link do exemplo](https://github.com/Felipecasadia/Estudos/tree/master/Memento/Exemplo%20Java)
