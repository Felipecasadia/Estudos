# Template Abstract Factory

Abstract Factory é um padrão de projeto de software (também conhecido como design pattern em inglês). Este padrão permite a criação de famílias de objetos relacionados ou dependentes por meio de uma única interface e sem que a classe concreta seja especificada. Uma fábrica é a localização de uma classe concreta no código em que objetos são construídos . O objetivo em empregar o padrão é isolar a criação de objetos de seu uso e criar famílias de objetos relacionados sem ter que depender de suas classes concretas. Isto permite novos tipos derivados de ser introduzidas sem qualquer alteração ao código que usa a classe base . O uso deste padrão torna possível trocar implementações concretas sem alterar o código que estas usam, mesmo em tempo de execução. No entanto, o emprego deste padrão, como acontece com outros padrões semelhantes, pode resultar em uma complexidade desnecessária e trabalho extra no início do código. Além disso, os níveis mais elevados de abstração podem resultar em sistemas que são mais difíceis de manter. A essência do padrão Abstract Factory é fornecer uma interface para criar famílias de objetos relacionados ou dependentes sem especificar suas classes concretas.


#### Utilização
A fábrica determina o tipo concreto do objeto a ser criado, e é nela que o objeto é realmente criado. No entanto, a fábrica só retorna um ponteiro abstrato para o objeto concreto criado.

O código do cliente não tem conhecimento algum do tipo concreto. Objetos concretos são, de fato criados pela fábrica, mas o código do cliente acessa tais objetos só através da sua interface abstrata.

A adição de novos tipos concretos é feita modificando o código do cliente para usar uma fábrica diferente, uma modificação que é tipicamente uma linha em um arquivo. A nova fábrica, em seguida, cria objetos de um tipo de concreto diferente, mas ainda retorna um ponteiro do mesmo tipo abstrato como antes. Isto é significativamente mais fácil do que modificar o código de cliente para instanciar um novo tipo. Se todos os objetos de fábrica são armazenados globalmente em um objeto Singleton, e todo o código do cliente passa pelo Singleton para acessar a fábrica adequada para a criação do objeto, então alterar as fábricas se torna tão fácil como mudar o objeto Singleton.


#### Exemplo de Aplicação
O padrão Abstract Factory pode ser utilizado na implementação de um toolkit que disponibilize controles que funcionem em diferentes interfaces gráficas, tal como Motif, GTK+ (GNOME) ou Qt (KDE). Estas GUIs possuem diferentes padrões de controles visuais e, para facilitar a construção de aplicativos que interajam facilmente com diferentes interfaces gráficas, é interessante que se defina interfaces comuns para acesso aos controles, independentemente da GUI utilizada. Este problema pode ser resolvido por meio de uma classe abstrata que declara uma interface genérica para criação dos controles visuais e de uma classe abstrata para criação de cada tipo de controle. O comportamento específico, de cada um dos padrões tecnológicos contemplados, é implementado por meio de uma classe concreta. O aplicativo, ou "cliente", interage com o toolkit por meio das classes abstratas sem ter conhecimento da implementação das classes concretas.
Um exemplo bem simplista seria um projeto com interface para Mobile e para Desktop, uma boa opção para reaproveitar os mesmos controles de interface seria criar pacotes com classes abstratas e os pacotes com as classes concretas implementando apenas as diferenças. Esse padrão também se aplica na padronização de ambientes, por exemplo, tamanhos de botões, fontes, cores de fundo, largura de bordas. Com isso e havendo uma política que exija que os desenvolvedores usem essas classes em vez das nativas da linguagem, ajudará a padronizar a aparência e comportamento das aplicações.


#### Estrutura

![Estrutura](https://github.com/Felipecasadia/Estudos/blob/master/Abstract%20Factory/Abstract_Factory.png)

#### Exemplo de código WidgetFactory:

[Link do exemplo](https://github.com/Felipecasadia/Estudos/tree/master/Abstract%20Factory/Exemplo%20Java)
