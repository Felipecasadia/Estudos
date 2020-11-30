# Template Factory Method

Factory Method ou Construtor virtual, na ciência da computação, é um padrão de projeto de software (design pattern, em inglês) que permite às classes delegar para subclasses decidirem, isso é feito através da criação de objetos que chamam o método fabrica especificado numa interface e implementado por um classe filha ou implementado numa classe abstrata e opcionalmente sobrescrito por classes derivadas.

#### Utilização
Este padrão é muito utilizado em frameworks para definir e manter relacionamentos entre objetos. O framework Spring, dependendo da configuração, pode utilizar um Factory Method para criar os seus beans.

Este padrão pode ser utilizado na construção de um framework que suporta aplicações que apresentam múltiplos documentos ao usuário. Normalmente este tipo de aplicação manipula um número variável de formatos de documento e, por isso, este framework deve ser flexível o bastante para suportar qualquer formato. Uma solução para este problema poderia disponibilizar, no framework, o código para alguns dos formatos mais utilizados. Mas, na prática, esta solução seria uma implementação pouco flexível, e até mesmo incompleta, já que é custoso implementar os mais variados formatos. O padrão Factory Method propõe uma solução que deixa para o cliente (a implementação da aplicação) a tarefa de suportar os formatos necessários e para o framework o papel de definição de uma abstração que oferece uma interface única para criação de documentos.

Este framework seria baseado em duas classes abstratas, que representam a Aplicação e o Documento. O cliente do framework fornece um par de classes concretas, uma aplicação e o respectivo documento, para cada um dos formatos de Documento suportados pela Aplicação. Se for necessário apresentar um documento que suporte desenho, por exemplo, o cliente deve disponibilizar as classes AplicacaoDesenho e DocumentoDesenho (supondo que o sufixo "Desenho" indique classes que suportam esta funcionalidade).

O objetivo do Factory Method está em diversas classes que implementam a mesma operação, retornarem o mesmo tipo abstrato, mas internamente instanciam diferentes classes que o implementam. Com o Factory Method o criador do objeto faz uma escolha de qual classe instanciar para o cliente. Para ser um Factory Method o método precisa retornar uma interface ou uma classe abstrata e, dependendo das necessidades do cliente, criar um objeto determinado como retorno. Um exemplo clássico do Factory Method são os iteradores tanto em Java como em .NET.


#### Aplicabilidade 
Quando a classe não antecipa a classe do objeto que quer criar.
Uma classe quer suas subclasses para especificar os objetos que cria.
Quando você não quer que o usuário tenha que saber de cada subclasse.
Encapsular a criação de objetos.

#### Consequências
Positivas: Baixo acoplamento, maior flexibilidade e elimina a necessidade de acoplar classes específicas para aplicação em nível de código.
Negativas: Alto número de classes, podendo sobrecarregar o sistema.

#### Estrutura

![Estrutura](https://github.com/Felipecasadia/Estudos/blob/master/FactoryMethod/FactoryMethod.png)

#### Exemplo de código:

[Link do exemplo](https://github.com/Felipecasadia/Estudos/tree/master/FactoryMethod/Exemplo%20Java)
