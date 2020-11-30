# Template State
Em certas ocasiões, quando o contexto em que está a desenvolver requer um objeto que possua comportamentos diferentes dependendo de qual estado se encontra, é difícil manejar a mudança de comportamento e os estados desse objeto, tudo dentro do mesmo bloco de código. O padrão State propõe uma solução para esta complicação, criando basicamente, um objeto para cada estado possível do objeto que o chama.


#### Motivação
O padrão State é motivado por aqueles objetos que, em seu estado atual, varia o seu comportamento devido as diferentes mensagens que possa receber. Como exemplo, tomamos uma classe Livro, um objeto desta classe terá respostas diferentes, dependendo do seu estado(Disponível ou Emprestado). Por exemplo invocando o método reservar de um objeto da classe Livro seu comportamento será diferente, se o Livro está no estado Disponível ou no estado Emprestado.


#### Objetivo 
Permite que um objeto altere seu comportamento de acordo com o estado interno que se encontra em um momento dado.

#### Consequências
Há uma extrema complexidade no código quando tentamos gerênciar comportamentos diferentes, dependendo de um número de estados diferentes. Também manter o código torna-se difícil, e mesmo em alguns casos, podem apontar a uma inconsistência de estados atuais na forma de implementação dos diferentes estados no código (por exemplo, com variáveis ​​para cada estado).

#### Estrutura

![Estrutura](https://github.com/Felipecasadia/Estudos/blob/master/State/State.png)

#### Exemplo de código:

[Link do exemplo](https://github.com/Felipecasadia/Estudos/tree/master/State/Exemplo%20Java)
