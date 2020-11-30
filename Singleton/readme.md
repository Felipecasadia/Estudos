# Template Singleton

Singleton é um (anti-)padrão de projeto de software (do inglês Design Pattern). Este padrão garante a existência de apenas uma instância de uma classe, mantendo um ponto global de acesso ao seu objeto.

Nota linguística: O termo vem do significado em inglês para um conjunto (entidade matemática) que contenha apenas um elemento.[1]

Alguns projetos necessitam que algumas classes tenham apenas uma instância. Por exemplo, em uma aplicação que precisa de uma infraestrutura de log de dados, pode-se implementar uma classe no padrão singleton. Desta forma existe apenas um objeto responsável pelo log em toda a aplicação que é acessível unicamente através da classe singleton.

#### Beneficios
Permite o controle sobre como e quando os clientes acessam a instância.
Várias classes singleton podem obedecer uma mesma interface, permitindo assim que um singleton em particular seja escolhido para trabalhar com uma determinada aplicação em tempo de execução.
Com apenas uma implementação interna do singleton pode-se fazer com que o singleton crie um número controlado de instâncias.
É mais flexível que métodos estáticos por permitir o polimorfismo.


#### Contras 
Acoplamento: Usando Singleton você estará acoplando o seu código em uma implementação estática e específica. Isso faz o seu código dependente dessa classe e impede, por exemplo, criar mocks em testes unitários.
Escopo: Se você por alguma razão decidir que para determinado componente da aplicação você precisa de outra implementação terá que alterar manualmente todas as classes.
Falsa segurança: No java, por exemplo, não existe uma classe apenas por JVM. O conceito de carregamento de classes em java é feito por ClassLoader.


#### Estrutura

![Estrutura](https://github.com/Felipecasadia/Estudos/blob/master/Singleton/Singleton.png)

#### Exemplo de código:

[Link do exemplo](https://github.com/Felipecasadia/Estudos/tree/master/Singleton/Exemplo%20Java)
