# O if e o else

A sintaxe do if no Java é a seguinte:

```java
if (condicaoBooleana) {
    codigo;
}
```

Uma condição booleana é qualquer expressão que retorne true ou false. Para isso, você pode usar os operadores **<, >, <=, >** e outros. Um exemplo:

```java
int idade = 15;
if (idade < 18) {
    System.out.println("Não pode entrar");
}

```

Além disso, você pode usar a cláusula else para indicar o comportamento que deve ser executado no caso da expressão booleana ser falsa:

```java
int idade = 15;
if (idade < 18) {
    System.out.println("Não pode entrar");
} else {
    System.out.println("Pode entrar");
}
```

Você pode concatenar expressões booleanas através dos operadores lógicos "E" e "OU". O "E" é representado pelo **&&** e o "OU" é representado pelo **||**.

Um exemplo seria verificar se ele tem menos de 18 anos e se ele não é amigo do dono:

```java
int idade = 15;
boolean amigoDoDono = true;
if (idade < 18 && amigoDoDono == false) {
    System.out.println("Não pode entrar");
}
else {
    System.out.println("Pode entrar");
}
```

Esse código poderia ficar ainda mais legível, utilizando-se o operador de negação, o **!**. Esse operador transforma o resultado de uma expressão booleana de false para true e vice versa.

```java
int idade = 15;
boolean amigoDoDono = true;
if (idade < 18 && !amigoDoDono) {
    System.out.println("Não pode entrar");
}
else {
    System.out.println("Pode entrar");
}
```

Para comparar se uma variável tem o mesmo valor que outra variável ou valor, utilizamos o operador **==**. Repare que utilizar o operador **=** dentro de um if vai retornar um erro de compilação, já que o operador = é o de atribuição.

```java
int mes = 1;
if (mes == 1) {
    System.out.println("Você deveria estar de férias");
}
```