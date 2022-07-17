# Classe-Math-
constantes, principais métodos e chamando métodos de outras classes



Vamos estudar uma importante classe, a Class Math, que provém várias funcionalidades matemáticas que nos ajudarão bastante em nosso curso de Java.

Aliado a essa grande e poderosa classe com a nossa seção de Métodos, vamos aprender como usar os methods que estão declarados em uma classe diferente daquela que estamos fazendo a chamada.

## Usando métodos de outras classes em Java

Até o presente momento em nossa apostila online Java Progressivo, chamamos os métodos da seguinte maneira:

*nome_do_metodo(argumentos);*

Fizemos isso porque definimos esses métodos dentro da mesma classe (até o momento só fizemos aplicativos Java contendo uma classe. Na próxima seção estudaremos classes).
Porém, quando o método não está presente na classe em que estamos fazendo a chamada, a sintaxe é diferente, ela é a seguinte:

*Nome_da_classe.Nome_do_metodo(argumentos);*

Vale salientar que a declaração é feita dessa maneira pois esses métodos são estáticos (static). Ou seja, não foi necessário criar um objeto da classe Math (diferente da [classe Scanner](http://javaprogressivo.blogspot.com/2012/08/java-recebendo-dados-do-usuario-classe.html), por exemplo).
Na próxima seção do curso, sobre Classes, você entenderá mais sobre *static.*

### A Classe Math (Class Math) do Java

Para ilustrar o uso de métodos de outras classes e,  de quebra, para nos auxiliar nos cálculos de constantes (como do número pi, do número de euler), no cálculo de funções trigonométricas (senos, cossenos, tangentes etc) e outras funcionalidades, vamos apresentar e usar a classe Math.

Essa classe já está na package (pacote) java.lang. Ou seja, não precisamos importar, que nem fazemos com a [classe Scanner](http://javaprogressivo.blogspot.com/2012/08/java-recebendo-dados-do-usuario-classe.html).

**Constantes da classe Math:**

Vamos imprimir o valor de Pi e da constante de euler, o 'e' dos números exponenciais.
Esses valores estão armazenados nas constantes PI e E, da classe Math. As constantes de outras classes são acessadas da mesma maneira que os métodos, ou seja:
*Math.PI*
*Math.E*

Vamos imprimir esses valores:

```
public class constantes {
    
    public static void main(String[] args){
        System.out.println("O valor de pi é: " + Math.PI);
        System.out.println("O valor de E é: " + Math.E);
    }

}
```

**Exponencial e potenciação na classe Math**
Para calcular valores do tipo: e^x
usamos o método: exp() , que recebe um double e retorna um double.

*numero = Math.exp(argumento)*

Para calcular qualquer tipo de potências, da forma: a^b
onde a e b são do tipo double, usamos o método pow() da classe Math

*numero = Math.pow(a,b)*

Veja:

```
public class Mathtest {
public static void main(String[] args){ 
System.out.println("'e' elevado ao quadrado = "+ Math.exp(2)); 
System.out.println("2 elevado ao cubo = " + Math.pow(2, 3));   
 }
}
```

Lembre-se que estes métodos retornam double.
Caso você tenha declarado um float e queira receber o resultado no sua variável float, use o cast.
Por exemplo, no caso dos nossos methods para o cálculo de IMC, o 'quadrado' retorna um float, então fazemos:
*(float)Math.pow(altura,2);*

Assim, o método Math.pow() irá retorna um float, ao invés do double.
Veja como ficariam os nossos métodos:

```
public static float IMC(float peso, float altura){
        return peso/(float)Math.pow(altura, 2);
    }
    
    public static float quadrado(float num){
        return Math.pow(num,2);
    }
```

Na verdade, nem precisaríamos mais do método quadrado(), pois o pow() já faz isso.

**Calculando a Raiz quadrada em Java através da classe Math**
Para calcular a raiz quadrada de um número positivo, usamos o método sqrt(), de square root (raiz quadrada em inglês).
Que recebe e retorna um double.

Por exemplo, um programa que mostra a raiz quadrada de PI:

```
public class RaizDePi {
    
    public static void main(String[] args){
        System.out.println("A raiz quadrada de Pi é = "+ Math.sqrt( Math.PI ) );
    }
}
```

**Calculando logaritmos naturais em Java através da classe Math**
Calcula logaritmos naturais (ou seja, de base 'e') através do método: log()
que recebe e retorna um double.

Por exemplo, um programa que mostra o logaritmo de natural de 10 e do número 'e':

```
public class logaritmos {
    
    public static void main(String[] args){
        System.out.println("O logaritmo natural de 10 é = "+ Math.log(10) );
        System.out.println("O logaritmo natural de 'e' é = "+ Math.log( Math.E ) );
    }

}
```

**Calculando senos, cossenos, tangentes e outras funções trigonométricas em Java através da classe Math**
As principais funções trigonométricas são seno, cosseno e tangente, e são calculadas através dos métodos:
Math.sin()
Math.cos()
Math.tan()

Que recebem e retornam valores do tipo double. Porém, os valores que estas funções recebem devem ser em RADIANOS!

```
public class Trigonometricas {
    
    public static void main(String[] args){
        System.out.println("O seno de 90 é = "+ Math.sin( (Math.PI)/2 ) );
        System.out.println("O cosseno de 0 é = "+ Math.cos(0) );
        System.out.println("A tangente de 45 é= "+ Math.tan( (Math.PI)/4 ));
    }

}
```

### **Módulo, máximo, mínimo e arredondamento em Java através da classe Math**

Para calcular o módulo de um número 'numero' usamos: *Math.abs(numero)*
Para calcular o valor mínimo de dois números 'num1' e 'num2', usamos: *Math.min(num1,num2)*
Para calcular o valor máximo de dois números 'num1' e 'num2', usamos: *Math.max(num1,num2)*

Para arredondar um número 'numero' para cima, usamos: *Math.ceil(numero)*
Para arredondar um número 'numero' para baixo, usamos: *Math.floor(numero)*

Estes métodos, assim como todos os outros, recebem e retornam double. Caso deseje receber a passar outro tipo, use cast conforme foi explicado no método *pow()*.


**Mais métodos matemáticos em Java**
Acesse a documentação:
http://docs.oracle.com/javase/6/docs/api/java/lang/Math.html
