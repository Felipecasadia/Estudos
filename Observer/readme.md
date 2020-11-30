# Template Observer

O Observer é um padrão de projeto de software que define uma dependência um-para-muitos entre objetos de modo que quando um objeto muda o estado, todos seus dependentes são notificados e atualizados automaticamente. Permite que objetos interessados sejam avisados da mudança de estado ou outros eventos ocorrendo num outro objeto.


#### Motivação
Um objeto que possua agregações deve permitir que seus elementos sejam acessados sem que a sua estrutura interna seja exposta. De uma maneira geral pode-se desejar que estes elementos sejam percorridos em várias ordens.

Como garantir que objetos que dependem de outro objeto percebam as mudanças naquele objeto?

Os observadores (observer) devem conhecer o objeto de interesse.
O objeto de interesse (subject) deve notificar os observadores quando for atualizado.
Os objetos devem interligar-se entre si de forma a que não se conheçam em tempo de compilação de forma a criar o acoplamento e desfazê-lo a qualquer momento em tempo de execução. Solucionar isso fornece uma implementação muito flexível de acoplamento de abstrações.


#### Aplicabilidade 
O padrão Observer pode ser usado quando uma abstração tem dois aspectos, um dependente do outro. Encapsular tais aspectos em objetos separados permite que variem e sejam reusados separadamente. Quando uma mudança a um objeto requer mudanças a outros e você não sabe quantos outros objetos devem mudar ou quando um objeto deve ser capaz de avisar outros sem fazer suposições sobre quem são os objetos. Em outras palavras, sem criar um acoplamento forte entre os objetos.

#### Consequências
Possibilita baixo acoplamento entre os objetos dependentes (os observers) e o assunto.
Acoplamento abstrato.
Suporte para broadcast.
Dificuldade em saber o que foi mudado.

#### Estrutura

![Estrutura](https://github.com/Felipecasadia/Estudos/blob/master/Observer/Observer.png)

#### Exemplo de código:

[Link do exemplo](https://github.com/Felipecasadia/Estudos/tree/master/Observer/Exemplo%20Java)
