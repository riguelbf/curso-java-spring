# While

O termo while pode ser traduzido para o português como “enquanto”. Este termo é utilizado para construir uma estrutura de repetição que executa, repetidamente, uma única instrução ou um bloco delas **“enquanto”** uma expressão booleana for verdadeira.

```java
int idade = 15;
while (idade < 18) {
    System.out.println(idade);
    idade = idade + 1;
}
```

O trecho dentro do bloco do while será executado até o momento em que a condição idade < 18 passe a ser falsa. E isso ocorrerá exatamente no momento em que idade == 18, o que não o fará imprimir 18.

```java
int i = 0;
while (i < 10) {
    System.out.println(i);
    i = i + 1;
}
```

Já o while acima imprime de 0 a 9.

# Do-While

O loop do-while tem comportamento parecido com o while, diferenciando-se somente na validação do loop, que é feita no final de cada iteração.

Sintaxe do do-while:

```java
do {
    //bloco de código
} while (condição);
```

Devido a essa característica, normalmente utilizamos essa estrutura de repetição quando desejamos que o bloco de código declarado no loop seja executado pelo menos uma vez.

Exemplo de uso:

```java
int i = 1;
do {
     System.out.println(i);
    i++;
} while (i < 11);

int area = 2 * 2;
```

Ao executar este código o loop declarado dentro do while será processado até que a condição criada para chamar o break seja verdadeira; neste caso, i ser igual a 5. O resultado será a impressão dos valores de 0 a 4.

# Break
Podemos utilizar nas estruturas de repetição um comando para finalizar um loop caso seja necessário, o comando break. Com ele é possível interromper a execução do loop a qualquer momento.

```java
int i = 0;
while (true) {
    if (i == 5) {
        break;
    }
    System.out.println(i);
    i++;
}
```

Ao executar este código o loop declarado dentro do while será processado até que a condição criada para chamar o break seja verdadeira; neste caso, i ser igual a 5. O resultado será a impressão dos valores de 0 a 4.

# Continue

Além do break, também podemos utilizar nas estruturas de repetição um comando que permite avançar para a próxima iteração do loop, o continue. Com ele conseguimos interromper a execução de uma iteração sem finalizar o loop inteiro.

Exemplo de uso:

```java
int i = 0;
while(i < 10){
    i++;
    if(i % 2 == 0){
        continue;
    }
    System.out.println(i);
}
```

Ao executar este código serão impressos os números ímpares entre 0 e 10.

Exemplo prático
Suponha que você precisa apresentar ao usuário os valores inteiros entre dois números. Para programar esse código, podemos utilizar a estrutura de repetição while.

Exemplo de uso:
```java
int minimo = 10;
int maximo = 30;
int numero = minimo + 1;

while ( numero < maximo) {
    System.out.println(numero);
    numero++;
}
```
Ao executar este código serão impressos os números entre 10 e 30.

# O For

Outro comando de loop extremamente utilizado é o for. A ideia é a mesma do while: fazer um trecho de código ser repetido enquanto uma condição continuar verdadeira. Mas além disso, o for isola também um espaço para inicialização de variáveis e o modificador dessas variáveis. Isso faz com que fiquem mais legíveis, as variáveis que são relacionadas ao loop:

```java
for (inicializacao; condicao; incremento) {
    codigo;
}
```
Um exemplo é o a seguir:

```java
for (int i = 0; i < 10; i = i + 1) {
    System.out.println("olá!");
}
```

Executar código
Repare que esse for poderia ser trocado por:

```java
int i = 0;
while (i < 10) {
    System.out.println("olá!");
    i = i + 1;
}
```

Porém, o código do for indica claramente que a variável i serve, em especial, para controlar a quantidade de laços executados. Quando usar o for? Quando usar o while? Depende do gosto e da ocasião.