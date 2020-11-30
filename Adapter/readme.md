# Template Adapter

Adapter (Adaptador, ou também conhecido como Wrapper) é um dos padrões de projeto estruturais do GoF (Gang of Four).

De forma exemplificável por um adaptadores de cabos, o padrão Adapter converte a interface de uma classe para outra interface que o cliente espera encontrar, "traduzindo" solicitações do formato requerido pelo usuário para o formato compatível com o a classe adaptee e as redirecionando. Dessa forma, o Adaptador permite que classes com interfaces incompatíveis trabalhem juntas. Veja a aba exemplos.

#### Motivação
Muitas vezes uma classe que poderia ser reaproveitada não é reutilizada justamente pelo fato de sua interface não corresponder à interface específica de um domínio requerida por uma aplicação.


#### Aplicabilidade 
O padrão Adapter pode ser utilizado quando:

se deseja utilizar uma classe existente, porém sua interface não corresponde à interface que se necessita;
o desenvolvedor quiser criar classes reutilizáveis que cooperem com classes não-relacionadas ou não-previstas, ou seja, classes que não possuem necessariamente interfaces compatíveis;
(exclusivamente para adaptadores de objetos) é necessário utilizar muitas subclasses existentes, porém, impossível de adaptar essas interfaces criando subclasses para cada uma. Um adaptador de objeto pode adaptar a interface de sua classe mãe.

#### Consequências
Cada adaptador de classes e de objetos tem diferentes soluções de compromisso. Um adaptador de classe:

adapta a classe Adaptee a Target através do uso efetivo de uma classe Adapter concreta. Em consequência disso, um adaptador de classe não funcionará quando quisermos adaptar uma classe e todas as suas subclasses;
permite que a classe Adapter substitua algum comportamento da classe Adaptee, uma vez que Adapter é uma subclasse de Adaptee;
introduz somente um objeto, e não é necessário endereçamento indireto adicional por ponteiros para chegar até a classe Adaptee.
Um adaptador de objeto:

permite a um único Adapter trabalhar com muitos Adaptees, ou seja, o Adaptee em si e todas as suas subclasses (caso existam);
torna mais difícil redefinir um comportamento de uma classe Adaptee. Ele exigirá a criação de subclasses de Adaptee e fará com que a classe Adapter referencie a subclasse, ao invés da classe Adaptee em si.

#### Estrutura

![Estrutura](https://github.com/Felipecasadia/Estudos/blob/master/Adapter/Adapter.jpg)

#### Exemplo de código:

[Link do exemplo](https://github.com/Felipecasadia/Estudos/tree/master/Adapter/Exemplo%20Java)
