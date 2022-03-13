
1. Qual comando possibilita a visualização de forma resumida dos commits realizados em um repositório?
	1. - [ ] `git log --short`
	2. - [x] `git log --oneline`
	3. - [ ] `git show --all`
	4. - [ ] `git commits --summary`
	5. - [ ] `git log --summary`

2. Quais os comandos para configurar sua identidade no Git? (desconsidere o uso de flags)
	1. - [ ] `git config username "John Doe"`, `git config email "john.doe@db1.com.br"`
	2. - [ ] `git config user.name "John Doe"`, `git config email "john.doe@db1.com.br"`
	3. - [ ] `git config user.name "John Doe"`, `git config user.mail "john.doe@db1.com.br"`
    4. - [x] `git config user.name "John Doe"`, `git config user.email "john.doe@db1.com.br"` 
	5. - [ ] `git config user.username "John Doe"`, `git config user.email "john.doe@db1.com.br"`
   
3. Qual(is) a(s) diferença(s) entre os comandos `git merge` e `git rebase`?
	R: O git merge mantém o histórico de alterações dos ramos subsequentes e gera um novo commit para fazer a 		união das branches ao passo que git rebase deleta o histórico de commits e faz o união na head da main.

4. No Git, é possível salvar o estado atual de seu trabalho e voltar ao estado do último commit da branch. Nesse caso, qual comando devemos utilizar? E para recuperar o trabalho posteriormente, qual é o comando?
	R:	Para salvar o estado atual e voltar ao último commit da brach utilizamos o git stash. 
		Para encontrar as mudanças salvas usamos git stash list
		Para utilizar a mudança salva, git stash @{n}

5. No contexto do Git, o que são, para que servem e em quais casos devemos criar `issues`?
	R:	Issue é um local no github onde podemos reportar sobre erros ou melhorias no código. Issues devem ser criadas para para reportar bugs e melhorias e controlar tarefas por essas.  

6. O que é e para que serve o `cherry-pick`?
	R:	Serve para pegar um commit específico de alguma branch com o git log. É utilizado para recuperar commits específicos de alguma branch ou fazer hot-fixes.

7. No cotidiano de um desenvolvedor, é comum que conflitos apareçam, e é de responsabilidade do mesmo resolvê-los. Qual o processo mostrado em curso para a resolução de um conflito?
	R:	Inicialmente podemos deixar o git resolver os conflitos de forma automática, caso a aplicação não consiga fazer podemos resolver os conflitos alterando manualmente a versão final para que está tenha somente os trechos necessários. 

8. Existe uma estratégia de branching chamada Git Flow, muito comumente aplicada no desenvolvimento de software. Qual das opções abaixo representam as branches presentes nessa estratégia, de acordo com o conteúdo?
	1. - [ ] `master`, `develop`, `feat`, `hotfix` e `release`
	2. - [ ] `master`, `develop`, `feature`, `fix` e `release`
	3. - [x] `master`, `develop`, `feature`, `hotfix` e `release`
	4. - [ ] `master`, `develop`, `feat`, `fix` e `release`
	5. - [ ] `master`, `develop`, `feat`, `fix` e `rc`

9. Qual(is) a(s) diferença(s) entre JRE e JDK?
	R:	JDK é um conjunto de ferramentas de desenvolvimento que inclui o JRE e a JVM. O JRE é o conjunto de ferramentas, aplicações e bibliotecas para executar aplicações java, incluindo a JVM.

10. O que é um workspace, no contexto do Eclipse?
	R:	É o conjunto de configurações, views, editores, usuários e senhas, referências a plugins de cada projeto no eclipse que quando salvos na pasta .metadata podem ser recuperados para recriar um ambiente específico para cada projeto em que trabalhamos.

11. Em Java, o operador `+` possui duas funções básicas. Quais são elas? Dê um exemplo em código de cada uma delas.
	R:	O operador + possui a função de aritmético de adição e de operador de incremento ++.
	 * Operador aritmético +
		 - int x = 1+1;
	 * Operador de incremento ++
		 - int x = 1;
		 - x++;

12. Ao realizar a operação abaixo, qual será o resultado mostrado no console?

    ```java
    class App {
        public static void main(String... args) {
            double divisionResult = 5 / 2;
            System.out.println(divisionResult);
        }
    }
    ```

    1. - [ ] `2`
    2. - [ ] `3.0`
    3. - [ ] `3`
    4. - [ ] `2.5`
    5. - [x] `2.0`

13. Por que o type casting "implícito" do Java não é possível no caso abaixo?

    ```java
    class App {
        public static void main(String... args) {
            float pi = 3.14;
        }
    }
    ```
	R: Porque o implicit type casting só ocorre quando o tipo final tem um tamanho de alocação maior que o inicial.   

14. Observe o código abaixo. Ele compilará? Qual a diferença entre as variáveis `firstValue` e `secondValue`?

    ```java
    class App {
        public static void main(String... args) {
            char firstValue = 'a';
            char secondValue = 97;
        }
    }
    ```
	R:	Sim o código irá compilar. O tipo char pode receber qualquer valor da tabela unicode com enconding UTF-16 seja utilizado na inicialização um caractere ou o código decimal unicode desse caractere. 

15. Observe os códigos abaixo. Ao serem compilados e executados, o que é exibido no terminal?

    ```java
    // código 1
    class App {
        boolean hasValue;
        public static void main(String... args) {
            System.out.println(hasValue);
        }
    }
    ```
	R: Nesse caso ocorre um erro por conta do código estar tentando acessar uma variável não estática dentro de um contexto estático, o método main. Para resolver poderíamos tornar a variável hasValue estática.

    ```java
    // código 2
    class App {
        public static void main(String... args) {
            boolean hasValue;
            System.out.println(hasValue);
        }
    }
    ```
	R: Nesse caso o erro ocorre porque a variável hasValue não foi inicializada. 

16. Para que serve e quando utilizar o comando `break`?
R: O comando break serve para interromper o fluxo de um loop, deve ser utilizado para controlar loops saindo dele em alguma condição e evitando loops infinitos. 

17. Quais as diferenças entre classe, objeto e referência?
R:	 Classes são modelos de referência que definem todos os métodos, propriedades e comportamentos associadas a ela. Objetos são as instâncias dessas classes, funções ou comportamentos. Referências são os nomes/endereços/ponteiros utilizados para determinar uma instância/objeto de determinada classe.

18. O que é exibido no terminal ao executar o código abaixo, considerando que ClasseExemplo não sobreescreveu o método `toString()`? Explique cada parte da estrutura do que é mostrado.

    ```java
    class App {
        public static void main(String... args) {
            ClasseExemplo exemplo = new ClasseExemplo();
            System.out.println(exemplo);
        }
    }
    ```
	R: É mostrado "ClasseExemplo@1b6d3586". Primeiro temos o nome da classe e em seguida vem o hashcode dessa classe. 

19. O que é exibido no terminal ao executar o código abaixo?

    ```java
    class Pessoa {
        Endereco endereco;
    }

    class Endereco {
        String cep;
    }

    class App {
        public static void main(String... args) {
            Pessoa aluno = new Pessoa();
            System.out.println(aluno.endereco.cep);
        }
    }
    ```
	R: Temos o erro java.lang.NullPointerException pois a variável cep não foi inicializada. 

20. Em Java, existem atributos e métodos de classe. Explique como declará-los e qual(is) a(s) diferença(s) entre eles e os atributos e métodos de instância.
	 * R: Atributos e métodos de classe:
		- São declarados utilizando static.
		- Estão presentes na própria classe (Não podem acessar atributos e métodos de instância)
		- Não é necessário gerar uma instância para utilizá-los. 
	 * Atributos e métodos de classe:
		- São declarados sem static.
		- Estão presentes na instância (Podem acessar atributos e métodos de classe e de instância)
		- É necessário gerar uma instância para utilizá-los. 

21. Os códigos mostrados até agora não respeitam os pilares da Programação Orientada a Objetos. Descreva cada um deles e explique seus benefícios e aplicações. 
	 * R: Os quatro pilares da programação orientada a objetos são:
		 * Abstração: Significa que podemos esconder partes do objeto expondo apenas interfaces simples. Permite acessar funções e métodos que fazem operações complexas apenas oferecendo as entradas corretas e estando preparado para colher as saídas. Pode ser aplicado em objetos para esconder a complexidade do mesmo ou para proteger a forma de execução.  
		 * Encapsulamento: Se refere ao modo de construir os objetos de forma a proteger os dados limitando o acesso somente dados diretamente relacionados entre si. Serve para aumentar a segurança e organização do código. Pode ser aplicado ao agrupar propriedades e métodos dentro de um mesmo objeto para que essas propriedades e métodos sejam acessadas apenas pelo objeto.
		 * Herança: É a característica de criar arvores/níveis de complexidade diferentes para objetos relacionados para aproveitar o código gerado. Permite a reutilização de código através da herança de propriedades e métodos. Pode ser aplicado ao criar 'subclasses' com características mais específicas aproveitando código de 'superclasses' mais genéricas. 
		 * Polimosfismo: É a possibilidade de se utilizar objetos diferentes com o mesmo nome porém implementações diferentes. Permite implementar código mais robusto ao aceitar entradas de números e tipos diferentes sem a necessidade de gerar validações e tratamentos.

22. Em Java, conseguimos aplicar a herança entre classes com a _keyword_ `extends`. Explique quais os benefícios de utilizar esse conceito no código.
	 * R: A palavra chave extends define a herança de uma classe a outra, assim a classe herdará todos os atributos e métodos da classe herdada. Os benefícios são principalmente no que diz respeito a reutilização de código, organização e manutenção do mesmo. 

23. Explique a(s) diferença(s) entre as *keywords* `this` e `super`. No caso da `super`, ela pode ser utilizada tanto no formato `super.` quanto `super()`, porém com aplicações diferentes - explique essas duas aplicações e dê exemplos de quando utilizar cada uma.
	 * R: A keyword **this** acessa o método da **classe atual** enquanto **super** acessa o método da **classe base**.
	 * A diferença entre super e super() é que super irá acessar o devido método da classe base ao passo que super() irá acessar o construtor padrão da classe base. 

24. No exemplo abaixo, a classe `Cachorro` é herdada de `Mamifero`. Por que o código não compila, como seria possível ajustá-lo para que compilasse e, após ajustado, o que ele exibirá quando for executado?

    ```java
    class Mamifero {
    	public void fazerSom() {
    		System.out.println("...");
    	}
    }

    class Cachorro extends Mamifero {
    	public void fazerSom() {
    		this.latir();
    	}

    	private void latir() {
    		System.out.println("Woof woof");
    	}
    }

    class App {
        public static void main(String... args) {
            Cachorro beethoven = new Mamifero();
            beethoven.fazerSom();
        }
    }
    ```
	 * R: O erro que ocorre é o seguinte: *`java: incompatible types: Mamifero cannot be converted to Cachorro`* ou seja, não existe instância do objeto Cachorro gerando o erro de incompatibilidade de tipos. 
	 * Para resolver bastaria instanciar Cachorro ao invés de Mamífero.

25. Sobre construtores, qual(is) das alternativas abaixo está(ão) correta(s)?

    1. - [x] O construtor `default` do Java deixa de existir assim que algum outro é declarado;
    2. - [x] O construtor `default` do Java possui como parâmetros todos os atributos da classe;
    3. - [ ] É obrigatória a criação de construtores explícitos quando a classe é herdada em algum local;
    4. - [ ] Os construtores sempre precisam ter o modificador de acesso `public`. Caso contrário, o código não compila;
    5. - [ ] O construtor `super()` precisa sempre ser chamado de forma explícita, em todos os casos de herança.

26. Qual a utilidade de classes abstratas em Java? E de métodos abstratos?
	 * R: Classes abstratas servem apra implementar parcialmente uma classe que servirá de molde para diversas outras classes.  

27. Qual a utilidade de interfaces em Java?
	 * R: Servem para obrigar um determinado grupo de classes a ter métodos ou propriedades comuns para existir.

28. Como funciona a composição em Java?
	 * R: A interdependência ou relação de objetos instanciados dentro de outros objetos configuram a composição dos mesmos.

29. Quando devemos utilizar classes abstratas (herança) e quando devemos utilizar interfaces? Qual o principal problema que o uso da segunda opção pode gerar, se não for feito da forma correta?
	 * Sempre que precisarmos de uma base comum para um conjunto de classes devemos utilizar classes abstratas. Quanto a preocupação for com a implementação de comportamentos padrão devemos utilizar as interfaces. 
	 * Se qualquer um dos métodos assinados não for implementado corretamente nas classes teremos erros. 
