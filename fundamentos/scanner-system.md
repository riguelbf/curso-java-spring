# Usando a Classe Scanner no Java

Quando se começa a conhecer os princípios da programação, com o tempo surge a vontade do desenvolvedor iniciante a trabalhar com programas no modo texto (console). Com esse princípio, muitos começam a usar a classe Scanner, pois tem justamente a finalidade de facilitar a entrada de dados no modo Console. Essa classe apareceu a partir do Java 5, antes dessa versão era complicado criar programas que recebiam valores de variáveis no modo Console.

## Conceito da Classe Scanner no Java
O significado da classe Scanner para muitos no começo é um pouco complicado de entender, mas com o tempo o programador acaba se acostumando com a sua definição. Um scanner de texto simples pode analisar os tipos primitivos e strings usando expressões regulares.

A classe Scanner tem como objetivo separar a entrada dos textos em blocos, gerando os conhecidos tokens, que são sequências de caracteres separados por delimitadores que por padrão correspondem aos espaços em branco, tabulações e mudança de linha.

Com essa classe podem ser convertidos textos para tipos primitivos, sendo que esses textos podem ser considerados como objetos do tipo String, InputStream e arquivos.

## Na Prática
Antes de tudo, é necessário saber algumas funções e aspectos que essa classe tem para exercer o funcionamento dentro do esperado. Quando invocada a classe Scanner, o compilador pedirá para fazer a seguinte importação:

```java
import java.util.Scanner;
```

Listagem 1: Importando a classe Scanner.
Como descrito na introdução, essa classe ajuda na leitura dos dados informados. Para fazer essa ação na prática, é necessário criar um objeto do tipo Scanner que passa como argumento o objeto System.in dentro construtor, do seguinte modo:

```java
import java.util.Scanner;

public class TestaDeclaracaoScanner {
  public static void main(String[] args) {
    //Lê a partir da linha de comando
    Scanner sc1 = new Scanner(System.in);
    String textoString = "Maria Silva";
    //Lê a partir de uma String
    Scanner sc2 = new Scanner(textoString);
  }
}
```

### Declarações do Scanner.
```java
import java.util.Scanner;

public class ContaTokens {
  public static void main(String[] args) {
    int i = 0;
    Scanner sc = new Scanner(System.in);
    System.out.print("Digite um texto:");
    while(sc.hasNext()){
      i++;
      System.out.println("Token: "+sc.next());
    }
    sc.close(); //Encerra o programa
  }
}
```

### Contagem de tokens em uma string.
O objeto System.in é o que faz a leitura do que se escreve no teclado. Veja abaixo como são invocados alguns dos métodos principais que correspondem com a assinatura que retorna um valor do tipo que foi invocado. Ou seja, para cada um dos primitivos existe uma chamada do método para retornar o valor especificado na entrada de dados, sempre seguindo o formato **nextTipoDado()**.

```java
Scanner sc = new Scanner(System.in);

float numF = sc.nextFloat();
int num1 = sc.nextInt();
byte byte1 = sc.nextByte();
long lg1 = sc.nextLong();
boolean b1 = sc.nextBoolean();
double num2 = sc.nextDouble();
String nome = sc.nextLine();
```