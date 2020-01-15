Exercício - Herança e Polimorfismo
Neste exercício você ira praticar os novos conceitos referente a classes. Ira criar uma classe enum de Espécies, uma classe de Consulta, Uma classe Pessoa e as classes Cliente, Funcionario e Fornecedor que herdam Pessoa, e a classe Vendedor que herda Funcionario. 
Em algumas destas classes haverá métodos sobrecarregados (overloading) e sobreescritos (overriding), construtores para que seja possível criar objetos da mesma já passando informações na hora da criação.
 
 1: Crie uma classe enum pública para Especie no pacote com.targettrust.model, e acresente o o atributo Especie na classe Animal, não esquece de criar os geters e seters na classe Animal.

Anfíbios, Mamíferos, Vertebrados, Peixes, Répteis, Invertebrados, Aves;

 

public class Animal {

      private Especie especie;

......

}

 

 2: Retire da classe Pessoa o atributo animal e acresente na classe Pessoa (no pacote com.targettrust.model) os seguintes atributos privados:

      private long codigo;

      private String nome;

      private Date dataCadastro;

   private Date dataNascimento; 

Crie os geters e setrs quando necessario e um construtor que receba como parâmetros todos os atributos da classe.

 

 3: Crie as classe pública Cliente herdando a classe Pessoa , nestas classes defina o seguinte atributo privado:

private Animal animal;

Crie os geters e setrs quando necessário  e um construtor que receba como parâmetros todos os atributos da classe. Não esqueça de usar a palavra reservada super.

 

 4: Crie as classes públicas Funcionario e Fornecedor herdando a classe Pessoa, nestas classes defina os seguintes atributos privados:

Fornecedor

      private boolean ativo;

   private String material;

 

Funcionario

      protected float salario;

      private final float VALOR_HORA = 15f;

      private String cargo;

   private Funcionario gerente;

Crie os geters e setrs quando necessario e um construtor que receba como parâmetros todos os atributos das classes. Não esqueça de usar a palavra reservada super.

 
 5: Crie as classes públicas Vendedor herdando a classe Funcionario, nestas classes defina o seguinte atributo privado:

private float comissao;

Crie os geters e setrs quando necessario e o construtor default(se necessario) e um construtor que receba como parâmetros todos os atributos da classe. Não esqueça de usar a palavra reservada super.

 

 6: Defina na classe Funcionario um método para calcular o Salaria do funcionário, utilizando o valor da constante do valor hora.

return  this.salario * VALOR_HORA;

 
 7: Defina na classe Funcionario outro  método para calcular o Salario do funcionário, agora utilizando o valor da hora passado como atributo na chamada do metodo.

return  this.salario * valorHora;

 

 8: Defina na classe Vendendor um método para calcular o Salaria do Vendedor, seja capaz de redefinir o comportamento (overriding) método public float getSalario() herdado da classe Funcionario. Observe que este tem o mesmo nome do método que está sendo herdado da classe Funcionário. 
 Esse método deve calcular o salario da seguinte forma :  valor do salario mais a comissão.

      float salario =   (super.getSalario() + getComissao();

 

 9: Crie uma classe Aplicacao executar o programa. Crie um algoritmo que imprima os dados do Cliente

O resultado da impressão deverá ficar parecido com:

Cliente: Zé Ninguem - Identificador: 45

Possui o animal: Rex

Peso: 45.0Kg

Altura: 120cm

O Animal esta Vivo:SIM

A Especie é: Mamíferos

 

 10: Crie agora uma classe pública Aplicacao2, declare nesta classe o método main e dentro deste método crie objetos das classes Funcionario e Vendedor.  
 Atribua informações para este objeto através do método construtor. Logo em seguida mostre os dados do objeto através dos seus métodos de leitura, os get’s.
 

As impressões devem fica parecida com os resultados abaixo

Funcionario: João Ninguem de QualquerCoisa - Identificador: 99664488

-----------------------------------------------------------

Cargo: Auxiliar

Salario com Hora Fixa: 180.0

Salario com Hora variada: 300.0

Data de Cadastro: 02/06/2014

Data de Nascimento: 15/06/1993

 

 

Funcionario: Ze Vende Tudo - Identificador: 4547895158

-----------------------------------------------------------

Cargo: Vendedor

Salario com Hora variada: 225.0

Salario + Comissão: 335.0

Data de Cadastro: 02/06/2014

Data de Nascimento: 15/06/1988