1. Por que a execução do Java é realizada em pilha?
   R: Porque essa é a melhor forma de implementar a estrutura sequencial de um programa e 
   para que nenhum objeto seja tratado antes das suas dependências. 
   
2. Em programação, qual(is) a(s) utilidade(s) de *debugar* um código?
   R: Um código pode ser debugado para companhar sua execução/funcionamento para se observar e(ou) encontrar erros.

3. Em Java, qual efeito as exceções possuem sobre o fluxo de execução da pilha? Por que, em muitos casos, o próprio desenvolvedor escreve códigos que intencionalmente lançam essas exceções?
   R: Em java exceções desviam o fluxo da aplicação pra que a exceção seja tratada. 
   Desenvolvedores utilizam dessa funcionalidade para controlar o fluxo de suas aplicações e evitar erros.

4. O que são e qual(is) a(s) diferença(s) entre as classes `Throwable`, `Exception` e `RuntimeException`?
   R: **Throwable** é a superclasse de todas as exceções do java.
   **Exception** é a classe que contém as exceções checadas e podem ser tratadas, com exceção de RuntimException.
   **RuntimeException** é a classe que contém as exceções não checadas que serão lançadas em tempo de execução. 

5. O que são e qual(is) a(s) diferença(s) entre exceções _checked_ e _unchecked_?
   R: Exceções **checked** são as que deverão ser tratadas pela aplicação em runtime. 
   **unchecked** são as exceções que não podem ser tratadas em runtime.

6. Qual(is) a(s) diferença(s) entre uma exceção e um erro em Java?
   R: Todas as exceptions, exceto a RuntimeException, são checadas(checked) na compilação podem receber tratamento em runtime.
   Todos os erros não são checados nem devem ser tratados em runtime, pois se tratam de erros severos lançados pela jvm.

7. Explique as *keywods* `try`, `catch`, `finally`, `throw` e `throws`.
   R: De forma resumida, todos os blocos que precisam ser monitorados em busca exceções devem ser cercados por um **try**, no caso de uma exceção ser lançada a mesma pode ser trada com um **catch**. 
   Para lançar uma exceção manualmente utilizamos **throw** e qualquer método que deva lançar exceções deve ter as mesmas específicadas com a clausula **throws**.
   Quando precisamos que um bloco seja executado após um try utilizamos **finally**.  

8. O que é e para que serve a interface `AutoCloseable`? Como funciona o *try with resources*?
   R: É a interface utilizada para automatizar o fechamento de recursos como I/Os ou Streams evitando o esgotamento de recursos da máquina.
   Quando passamos declaração dos recursos como "argumento" de um bloco try estamos fazendo o try-with-resourses.

9. Sobre pacotes, é correto afirmar que:
   1. - [X] É boa prática nomear os pacotes na estrutura `{site_ao_contrário}.{nome_do_projeto}`;
   2. - [X] Não devemos criar muitos pacotes, pois prejudica a navegação e legibilidade dentro do projeto;
   3. - [X] O uso de pacotes corretamente está diretamente relacionado à qualidade arquitetural de um projeto, já que eles servem para organizá-lo;

10. Explique a(s) diferença(s) entre os modificadores de acesso `private`, `default` `protected` e `public` em Java.
   R: Do mais visível para o menos visível:
   **public** visível dentro e fora do pacote e classe de origem.
   **protected** visível dentro do mesmo pacote ou subclasses fora do pacote de origem.   
   **default** visível somente dentro do mesmo pacote. Não é necessário específicar esse modificador de acesso.
   **private** visível somente dentro da mesma classe.
   
11. Qual a ordem correta dos itens abaixo, considerando a estrutura de um arquivo Java onde há somente uma importação e uma classe vazia? (considere * como _wildcard_)

   1. - [ ] `package *;`, `imports *;` e `class * {}`;
   2. - [X] `package *;`, `import *;` e `class * {}`;
   3. - [ ] `pack *;`, `imports *;` e `class * {}`;
   4. - [ ] `pack *;`, `import *;` e `class * {}`;

12. Explique o que é FQN (Fully Qualified Name), sua estrutura e como evitamos ter de utilizá-lo sempre que referenciamos uma classe.
   R: É o caminho e nome completo de uma classe. É estruturado da segunte forma: pacote.subpacote.Nome 
   Basta importar a classe em questão para evitarmos de ter que importar a mesma em todas as utilizações. 

13. O que é, para que serve, como adquirir e como utilizar um arquivo JAR?
   R: Um arquivo JAR é uma coleção de arquivos e classes fechados em um executável. 
   Serve para portar uma aplicação ou parte dela.
   Pode ser um das formas de exportar classes e resursos de uma aplicação ou a aplicação por completo.
   Pode ser utilizado abrindo o .jar para que máquinas habilitadas o executem ou importados em outras aplicações.    

14. O que é o pacote `java.lang` e por que ele é tão essencial para qualquer código Java?
   R: É o pacote que contém as classes fundamentais da linguagem. 
   É essencial por conter classes como a Object que é a classe raiz de todos os objetos. 

15. O que é uma `CharSequence` e qual(is) a(s) diferença(s) entre ela e uma `String`?
   R: CharSequence é uma interface generalista de diversas classes incluindo as classes String, StringBuffer e StringBuilder. 
   Representa uma sequência de caracteres e provê acesso a diversas formas de apresentar os mesmos.
   String é a classe que implementa CharSequence, tem os métodos padrão dos objetos como equals e hashcode, representa uma sequência de caracteres e todas as sequências de caracteres em java são implementados como instâncias dessa classe. 

16. Descreva os métodos da classe String citados abaixo:

    1. `.replace(char oldChar, char newChar);`
		R: Troca todos os caracteres em oldChar por newChar.
    2. `.replaceAll(String regex, String replacement)`;
		R: Troca todas as substrings que batem com o regex utlizado pelo que está em replacement.
    3. `.toLowerCase()`;
		R: Troca todos os caracteres pelos seus homólogos minúsculos. 
    4. `.concat(String str)`;
		R: Concatena str ao final da string.
    5. `.contains(CharSequence s)`;
		R: Retorna um booleano com o resultado da verificação da existência de s dentro da string. 
    6. `.equals(Object anObject)`;
		R: Retorna um booleano com o resultado da comparação da string com o objeto em anObject. 
    7. `.equalsIgnoreCase(String anotherString)`;
		R: Retorna um booleano com o resultado da comparação da string com anotherString considerando caracteres homólogos em lowercase e uppercase iguais.
    8. `.isBlank()`;
		R: Retorna um booleano com o resultado da comparação da string com null ou caracteres whitespace.
    9. `.matches(String regex)`;
		R: Retorna um booleano com o resultado da comparação da string com o regex especificado.

17. Qual(is) a(s) diferença(s) entre `overriding` e `overloading` de métodos? Explique-os dando exemplos úteis da aplicação de ambos.
   R: O overloading ocorre quando implementamos mais de um método com o mesmo nome, porém com assinaturas diferentes.
   Um exemplo simples seria um método que calcula juros, poderiamos chamar calculaJuros e implementar métodos com assinaturas diferentes para juros simples e compostos.
   O overriding ocorre quando reimplementamos um método herdado para ter um retorno mais específico para a classe filha.
   Um exemplo de overriding seria a reimplementação de um método que calcula e retorna o bônus dos funcionários de uma devida empresa para se ter um calculo mais específico de uma subclasse da classe funcionários poderíamos implementar o método bonus herdado com essa diferença de cálculo.
   Diferênças básicas:
   |   **overloading** |**overriding**|
   |:---:|:---:|
   |Serve para termos diferentes definições de métodos atuando em situações diversas|É utilizado pra termos implementações específicas dos métodos da classe mãe.|
   |É realizado com multiplas implementações do mesmo método na mesma classe.|É feito em classes diferentes que possuem a relação de herança.|
   |Ocorre na compilação.|Ocorre em tempo de execução.|
   |Ordem, tipo ou número de parâmetros precisam diferentes para ocorrer.|Ordem, tipo e número de parâmtros precisam ser iguais ao da classe pai para ocorrer.|
   |As implementações podem ter tipos de retorno diferentes entre si.|Deve ter o mesmo retorno.|

18. Todas as classes Java herdam a classe `Object`, que possui três métodos comumente sobrescritos: `.equals(Object obj)`, `.hashCode()` e `.toString()`. Explique a utilidade de cada um deles.
   R: O método .equals(Object obj) serve para comparar o conteúdo de dois objetos.
   O método .hashCode() serve gerar um hash do objeto para que operações internas da linguagem operem de forma mais otimizada ao rodar o objeto dentro de uma agoritmo de hash é possível referenciar esse objeto de aforma mais eficiente.
   O método toString() serve para termos uma representação do objeto em um String. Sbrescrever esse método é comum para personalizar essa representação. 

19. Qual(is) das opções expressa(m) uma sintaxe correta para criar um *array* de inteiros?

    1. - [ ] `int[] inteiros = []`;
    2. - [ ] `int[] inteiros = new int[]`;
    3. - [X] `int[] inteiros = new int[]{999}`;
    4. - [X] `int[] inteiros = new int[1]`;
    5. - [X] `int[] inteiros = {999}`;
    6. - [ ] `int... inteiros = {999}`;

20. Por que o primeiro código abaixo exibe o valor `0` no terminal, mas o segundo produz uma exceção?

    ```java
    // código 1
    class App {
        public static void main(String... args) {
            int[] inteiros = new int[1];
            System.out.println(inteiros[0]);
        }
    }
    ```

    ```java
    // código 2
    class Pessoa {
        Endereco endereco;
    }

    class Endereco {
        String cep;
    }

    class App {
        public static void main(String... args) {
            Pessoa[] pessoas = new Pessoa[1];
            System.out.println(pessoas[0].endereco.cep);
        }
    }
    ```
   R: Porque a variável cep e Endereco não foram inicializados;

21. Sobre *type casting*, explique:

    1. *Cast* implícito;
		R: É o tipo de conversão onde não é necessário fzer o cast explicito pois são tipos compatíveis e a conversão não irá gerar perda de dados.
    2. *Cast* explícito; É a conversão onde é necessário forçar pois há perda de dados. Onde o tipo final é menor em memória ou irá gerar perda de algarismos significativos. 
    3. `ClassCastException`; Ocorre quando a conversão gerou erro de incompatibilidade. 

22. Explique o que é e como utilizar o `autoboxing` e o `unboxing`.
   R: Autoboxing e unboxing são as conversões automáticas de tipos primitivos em seus repectivos wrappers.
   Podemos utilizar criando um whapper e inicializando o mesmo com um primitivo.

23. É possível, no momento em que é executada uma aplicação em Java, passar argumentos para a mesma. Como isso pode ser feito e como podemos acessar esses argumentos dentro do código (no método `main()`)?
   R: Os argumentos do método main funcionam de forma a permitir o acesso em linha de comando ou de forma parametrizada a funções do programa criado logo no memento de sua execução.
   Podemos acessar os argumentos criados dentro da aplicação passando na abertura do programa os argumentos criados. 
   
24. Ao utilizar um `array`, o tamanho máximo do mesmo deve ser declarado. Por que isso não acontece quando utilizamos `ArrayList`? E qual é o limite do que essa estrutura pode armazenar?
   R: Não ocorre porque ArrayList tem tamanho dinâmico onde o limite teórico seria o tamanho máximo do primitivo int utilizado para criar os indices, mas isso não ocorre porque não temos máquinas que suportem esse tamanho sem dar erro por falta de memória. 

25. Por que, no geral, o `ArrayList` costuma ser mais utilizado que `arrays` em Java?
   R: Porque além de ter tamanho dinâmico é uma classe com diversos métodos para facilitar o desenvolvimento. 

26. Por que sempre devemos optar pelo uso de `Generics` ao declarar um `ArrayList` (declaração no formato `ArrayList<{tipo}>`)?
   R: Porque assim não temos que nos preocupar com erros por tipos incompatíveis. 

27. Explique os métodos `.add(E e)` e `.contains(Object o)`, da interface `Collection`?
   R: O método add(E e) serve para adicionar elementos a uma collection e retorna um boleano com o resultado dessa operação.
   O método contains(Object o) serve para verificar a existência do objeto dentro da collection.

28. Explique as interfaces `Comparator<{tipo}>` e `Comparable<{tipo}>`.
   R: A interface Comparable<{tipo}> serve para podermos ter na mesma a funcionalidade de ordenação. Após uma classe implementar a interface podemos utilizar métodos como sort().
   A interface Comparator<{tipo}> serve para definir uma forma além da padrão de comparação ou seja para persolalizar outras formas de sort. 
   
29. Qual(is) a(s) diferença(s) entre as interfaces `List` e `Set`?
   R:
   |List|Set|
   |:---:|:---:|
   |Permite duplicação de elementos|Não permite duplicação de elementos|
   |Manter a ordem de inserção|Não mantem a ordem de inserção|
   |Permite adicionar inumeros nulls|Permite adicionar somente um null|
   |É implementada por LinkedList e ArrayList|É implementada por TreeSet, HashSet e LinkedHashSet|

30. Como funciona a implementação `HashSet`? Qual a relação dela com o método `.hashCode()`?
   R: HashSet é a implementação de uma lista onde cada elemento tem sua assinatura hash chamado de hashcode.

31. Por que é recomendado que o *overriding* dos métodos `.equals(Object obj)` e `.hashCode()` seja realizado sempre em pares (ao sobreescrever um, o outro também deve ser sobreescrito)?
   R: Porque um está intimamente ligado ao outro na busca por hash e ao alterar um podemos estar quebrando a implementação do outro. 
   
32. Qual é a estrutura de uma expressão *lambda*, em Java? Explique e dê um exemplo, em código.
   R: A estrutura segue o formato (argumento)->(corpo). Espressões lambda servem principalmente para diminuir a verbosidade do java adicionando inferência de tipos e implementação interna das estruturas mínimas de funções.
   Exemplos: 
      ()-> 10;
      (String s) -> {System.out.println(s)}

33. Qual é a estrutura de uma expressão *lambda* utilizando *method reference*, em Java? Explique e dê um exemplo, em código.
   R: A estrutura segue o formato (classe::metodo) e representa o referenciamento direto de métodos dentro da expressão lambda.
   Exemplo:
   ```java
      public class App {
         public static void main(String[] args) {
            List<Integer> list = Arrays.asList(0, 1, 2, 3);
            list.stream().map(App::timesSeven);
         }
      static Integer timesSeven(Integer i){return i * 7;}
      }
   ```
   
34. Qual é a estrutura de uma `stream`, em Java? Explique e dê um exemplo, em código.
   R: A estrutura segue o formato sequência.stream() onde sequaência é qualquer objeto sequancial ou paralelo que pode ser iterado.
   Exemplo:
		List<Integer> list = Arrays.asList(0, 1, 2, 3);
		
		list.stream()
		   .map(f -> f * 7)
		   .filter(f -> f > 0)
		   .forEach(System.out::println);

   
35. O que falta no código abaixo para ser considerado um teste útil?

    ```java
    // package & imports
    class CalculadoraTest {

    	@Test
    	public void deveSomarDoisValores() {
            Calculadora calculadora = new Calculadora();
            int resultado = calculadora.somar(2, 2);
    	}

    }
    ```
	
	R: Falta ter um retorno do teste. Assert.assertEaquals(4, resultado);

36. Como é aplicado o TDD? Qual(is) benefício(s) ele traz e quando devemos utilizá-lo?
   R: É aplicado invertendo a ordem de desenvolvimento DESENVOLVIMENTO->TESTES para um método voltado aos testes onde implementamos os testes e refatoramos a implementação até termos passado em todos os testes. TESTES -> IMPLEMENTAÇÃO -> REFATORAÇÃO
   Com o TDD terminamos a implementação com os testes feitos, em qualquer refatoração temos a segurança dos testes feitos para testaralém de ajudar a focar o desenvolvimento somente nas regras de negócio. 

37. Quais métodos podemos utilizar para validar o lançamento de exceções em testes automatizados?
   R: Podemos utilizar o assertThrows(exceção.class, () -> classe.método()); ou com um break entro do try(){fail}catch(){};
