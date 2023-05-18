## Java Docs

### Caracterísitcas da linguagem Java

 * Compilada:
> Um programa em Java é compilado para o chamado "bytecod" , que
é próximo as instruções de máquina.
 * Portável:
> Java foi criada para ser portável. O "bytecode" gerado pelo 
compilador para a sua aplicação específica pode ser transportado
entre plataformas distintas que suportam Java.

* Orientadas a Objetos:

> Java suporta herança , mas não herança múltipla compensada pelo
uso de interfaces.

* Segurança:

> Presença de coleta automática de lixo,  que evita erros comuns
ao acessar diretamente a memória.

> Presença de mecanismos de tratamento de exceções que torna as 
aplicações mais robustas , não permitindo que elas abortem , mesmo
que rodando sob condições anormais;

* Cocorrência:
> Permite, de maneira fácil, a criação de vários "threads" de execução;

* Eficiente:

> Exige pouco espaço , pouca memória comparando-se com outras 
linguagens.
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
> **Declaramos o tipo seguido do nome da variável.**
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
### Estruturas condicionais

 * If/Else:
> O if/else é uma estrutura de condição em que uma expressão 
> booleana é analisada

 > V || V = V

 > F || V = V

 > V || F = V

 > F || F = F
  ____________________________________________
 > F && V = F

 > V && F = F

 > V && V = V

 > F && F = F

 * Switch/case:
 > A estrutura condicional switch/case vem como alternativa 
> em momentos em que temos que utilizar múltiplos ifs no
> código.
 
> O switch/case testa o valor contido em uma
 > variável, realizando uma comparação com cada uma das opções. Cada uma
 > dessas possíveis opções é delimitada pela instrução case.
```java
public class Exemplo {
	
    public static void main(String[] args) {
        int mes = 2;
        switch (mes) {
            case 1:
                System.out.println(“O mês é janeiro”);
                break;
            case 2:
                System.out.println(“O mês é fevereiro”);
                break;
            case 3:
                System.out.println(“O mês é março”);
                break;
            case 4:
                System.out.println(“O mês é abril”);
                break;
            case 5:
                System.out.println(“O mês é maio”);
                break;
            case 6:
                System.out.println(“O mês é junho”);
                break;
          
            default:
                System.out.println(“Mês inválido”);
                break;
        }
    }
	
}
```
 ### Estruturas de repetição

* For: O for é uma estrutura de repetição na qual seu ciclo 
será executado por um tempo ou condição pré-determinados e 
em uma quantidade de vezes que determinamos.
  
```java
 for(<varíavel_de_controle> , <análise_de_variável_de_controle) , <incremente_da_variavel_de_controle>) {
    // código a ser executado
        }
```
>Quando utilizamos o for, precisamos de uma variável para
> auxiliar a controlar a quantidade de repetições a serem executadas. Essa variável é chamada de variável de controle 
> e é declarada no primeiro argumento do for.

> O segundo argumento do for é utilizado para definir até 
> quando o for será executado. Geralmente, trata-se de uma 
> condição booleana em cima da variável de controle.

>O terceiro argumento indica o quanto a variável de 
> controle será modificada no final de cada execução dentro do for.

```java
public class Exemplo {
	
    public static void main(String[] args) {
        for (int i = 0; i <= 10; i++) {
            System.out.println(“A variável i agora vale “ + i);
        }
    }
	
}
```
 * While:
> utilizamos o while quando não sabemos exatamente quantas 
> vezes o código será repetido.

```java
while (<condição>) {
        // Trecho de código a ser repetido
        }
```

### Métodos
> Os métodos são ações ou
> procedimentos, onde podem interagir e se comunicarem
> com outros objetos.
> Como boas práticas, é indicado sempre usar o nome dos métodos 
> declarados como verbos

#### Sintaxe:
[modificador de acesso] + tipo_retorno +nome_do_metodo ([argumentos]) {

}
#### Exemplo:
````java
class Cachoroo {
    int tamanho;
    String nome;
    
   public void latir(){
        if(tamanho > 60){
            System.out.println("Woof Woof");
        }else if (tamanho > 20){
            System.out.println("Woof");
        }else{
            System.out.println("ZzZzZz");
        }
    }
}
````
````java
public class TestaCachorro{
    public static void main(String[] args) {
        Cachorro bob = new Cachorro();
        bob.tamanho = 70;
        
        Cachorro rex = new Cachorro();
        rex.tamanho = 59;
        
        Cachorro zeus = new Cachorro();
        zeus.tamanho = 19;
        
        bob.latir();
        rex.latir();
        zeus.latir();
    }
}
````
### Construtores
> Também conhecidos pelo inglês constructors, os construtores são os responsáveis por criar o objeto em 
> memória, ou seja, instanciar a classe que foi definida.

* nota: Em Java apenas as Interfaces não possuem construtores.

#### Exemplo:
````java
public class Carro{
    //construtor da classe Carro
    public Carro (){
        // code
    }
}
````
#### Sintaxe:
> modificadores de acesso (public nesse caso) + nome da classe (Carro nesse caso) + parâmetros (nenhum definido
neste caso). 

> O construtor pode ter níveis como: public, private ou protected.

```java
public class Carro {
    
}

public class Aplicacao {
    
    Carro fiat = new Carro();
    // construtor chamado sem parâmetro.
}
```
````java
public class Carro{
    public String nome;
    public String placa;
    public String cor;
    
    public Carro(String nome , String placa , String cor){
        this.nome = nome;
        this.placa = placa;
        this.cor = cor;
    }
    public class Concessionaria{
        Carro ferrari = new Carro("Palio", "air-023","Vermelha");
        // construtor com 3 parâmetros
    }
}
````
### Modificadores de acesso
> Os modificadores de acesso são palavras-chave na
> linguagem Java. Eles servem para definir a visibilidade que
> determinada classe ou membro terá diante das outras.

#### tipos de modificadores de acesso:
* **public**: Com este modificador,
o acesso é livre em qualquer lugar do programa.
* **private:** Com este modificador, o acesso é permitido somente dentro da 
classe onde ele foi declarado. Por padrão, é a visibilidade definida para métodos e atributos em uma classe.
* **Protected**: Com este modificador, apenas a classe que contém
o modificador e os tipos derivados dessa classe tem o acesso.

_____________________________________________________________________
### POO (Programação orientada a objetos)

#### Abstração:
> Como estamos lidando com uma representação de um objeto real 
> (o que dá nome ao paradigma), temos que imaginar o que esse objeto irá realizar dentro de nosso sistema. São três pontos que devem ser levados em consideração nessa abstração.
* Identidade: É preciso dar uma identidade ao objeto que será criado.
Essa identidade deve ser única dentro do sistema para que não haja conflito.


* Propriedades: No mundo real qualquer objeto possui elementos que
o definem. Dentro da programação orientada a objetos, essas características são nomeadas propriedades. 
Por exemplo, as propriedades de um objeto “Cachorro” poderiam ser “Tamanho”, “Raça” e “Idade”.

* Métodos: Por fim, a terceira parte é definirmos as ações 
que o objeto irá executar. Essas ações, ou eventos, são chamados métodos. Esses métodos podem ser 
extremamente variáveis, desde “Acender()” em um objeto lâmpada até “Latir()” em um objeto cachorro.

#### Encapsulamento:
>Se trata de um dos elementos que adicionam segurança à
> aplicação em uma programação orientada a objetos pelo fato de esconder as propriedades, criando uma espécie de caixa preta.

> A maior parte das linguagens orientadas a objetos implementam o encapsulamento baseado em propriedades privadas, ligadas
> a métodos especiais chamados getters e setters, que irão retornar e setar o valor da propriedade, respectivamente. Essa atitude evita o acesso direto a propriedade do objeto, adicionando uma outra camada de segurança à aplicação.

 > Para fazermos um paralelo com o que vemos no mundo real, temos o encapsulamento em outros elementos.
 > Por exemplo, quando clicamos no botão ligar da televisão, não sabemos o que está acontecendo internamente. 
 > Podemos então dizer que os métodos que ligam a televisão estão encapsulados.
 
#### Herança: 
>  Essa característica otimiza a produção da aplicação em tempo e linhas de código.

> Para entendermos essa característica, vamos imaginar uma família: a criança, por exemplo, está herdando características de seus pais. Os pais, por sua vez, herdam algo dos avós, o que faz com que a criança também o faça, e assim sucessivamente.
> Na orientação a objetos, a questão é exatamente assim 

#### Polimorfismo :
> Na natureza, vemos animais que são capazes de alterar sua forma conforme a necessidade, e é dessa ideia que vem o polimorfismo na orientação a objetos. Como sabemos, os objetos filhos herdam as características e ações de seus “ancestrais”. Entretanto, em alguns casos, é necessário que as ações para um mesmo método seja diferente. 
> Em outras palavras, o polimorfismo consiste na alteração do funcionamento interno de um método herdado de um objeto pai.

> Como um exemplo, temos um objeto genérico “Eletrodoméstico”.
> Esse objeto possui um método, ou ação, “Ligar()”. Temos dois objetos, “Televisão” e “Geladeira”, que não irão ser ligados da mesma forma. Assim, precisamos, para cada uma das classes filhas, reescrever o método “Ligar()”.