## Java Docs

> * Linguagem de programação de alto nível orientada a objetos.
> * Plataforma independente
> * Não usa ponteiros
> * Multithread
> * Perfomace
> * Segurança
> * Case sensiteve
> * Fortemente tipada
> * Write once , run everywhere
________________________________________________________
>Fortemente tipada: Fornecer um tipo a variáveis e objetos
> ````java
 > int valor = 100;
> System.out.println(valor)
 ____________________________________________________________
### JRE:
> Agrega á máquina virtual e alguns recursos para a execução de
> aplicações java

### JDK:
> Conjunto de utilitários que oferece suporte ao desenvolvimento
> de aplicações.

### Código:

> myprogram.java ---> compiler ----> myprogram.class ---> jvm ---> bytecode ---> myprogram

_________________________________________________________________

### Tipos primitivos:
> Inteiro : byte , short, int , long
> 
> Real: float , double
>
> Caracter : char
>
>lógica : boolean

________________________________________________________________

### Classes

> Diversos objetos que compartilham um conjunto de caracteres
> em comum.

````java
public class Pessoa {
   public String nome;
   public String email;
   public String cpf;
   
}
````
#### Sintaxe: 
````java
modificador de acesso  + palavra reservada (class)+ NomeDaClasse{

//Local onde atributos , construtores e métodos são criados

}
````
#### Exemplo: classe Pessoa
````java
 public class Pessoa {
    public String nome;
    public String email;
    public String cpf;
    
    public exibirDados (){
        System.out.printf("Dados da pessoa");
        
        this.nome = "Nome";
        this.email = "nome@gmail.com";
        this.cpf = "012345678910";
    }
}
````
#### Convenção:
> 1. Manter o nome simples e descritívo;
> 2. Usar palavras inteiras sem siglas e  abreviações;
> 3. A primeira letra de cada palavra interna deve sempre ser maisúcula. 

#### Como declarar:
> Se declara uma classe da mesma maneira como se  declara uma
> variável de tipo primitiva.
> Declaramos o tipo seguido do nome da variável.
````java
Pessoa pessoa1 = new Pessoa ();
````
### Objetos
> Os objetos são caracteristicas definidas pela classe. Neles é 
> permitido instaciar objetos da classe para inicializar os 
> atributos e invocar métodos.

#### Atributos :
> Os atributos são propriedades de um objeto, também são conhecidados
> como variáveis ou campos. Essas propriedades definem o estado de um 
> objeto , fazendo com que esses valores possam sofrer alterações.

#### Exemplo: classe Cachorro
````java
public class Cachorro {
    public String nome;
    public int peso;
    public String corDosOlhos;
    public String raca;
}
````
#### Exemplo: classe TestaCaes
````java
public class TestaCaes{

    Cachorro cachorro1 = new Cachorro();
    cachorro1.nome = "Krypto";
    cachorro1.peso = 50;
    cachorro1.corDosOlhos = "Azuis";
    cachorro1.raca = "Labrador";

    Cachorro cachorro2 = new Cachorro();
    cachorro2.nome = "Mufasa";
    cachorro2.peso = 65;
    cachorro2.corDosOlhos = "Pretos";
    cachorro2.raca = "Pastor Alemão";

    Cachorro cachorro3 = new Cachorro();
    cachorro3.nome = "Zeus";
    cachorro3.peso = 80;
    cachorro3.corDosOlhos = "Pretos";
    cachorro3.raca = "Dog alemão";
}
````
### Métodos
