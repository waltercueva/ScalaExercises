## Funciones

```scala
def suma(a:Int, b:Int)=a+b
suma(10,4)

def multiplicacion(a:Int, b:Int):Int =a*b
multiplicacion(10,4)

def multiples(a:Int, b:Int)={
	val c=a*b
	val d=c+10;
	d/c
}

```

## Lazy

```scala
val x=1/0
lazy val y=1/0
print(y)
```

## Operador

```scala
"UPC"=="PUCP"
"UPC"=="PUCP"||"UPC"=="PUCP
!("UPC"=="PUCP"||"UPC"=="PUCP")
```

## Condicional

```scala
val  x=10
if(x>2)
	print("es mayor")
else {
	print("es menor")
}

var edad=40
var res=if(edad>30)"mayor" else "menor"
```

## Pattern Matching

```scala
var color="orange"
color match{
case color if(color=="blue"||color=="xyz") => print("azul")
case "red"|"orange"  => print("rojo")
case _ => print("Otros")
}

```

## Bucles

```scala
def funcion()={
	var i=0
	while(i<50){
	println(i)
	i=i+1
	}
}
```

```scala
object Ejemplo{

def main(args: Array[String])={
	var i=0
	while(i<50){
	println(i)
	i=i+1
	}
}
}

```

```scala
object Ejemplo{

def main(args: Array[String])={
	var i=0	
	for(z<-1 to 50){
	println(i)
	i=i+1
	}
}
}

```

```scala
object Ejemplo{

def main(args: Array[String])={
	var i=0	
	for(z<-1 until 50){
	println(i)
	i=i+1
	}
}
}

```

```scala

def demo()={
	for(z<-1 until 50 if z%3==0){
	println(z)
	}
}

```

## Decompiler en Java

```scala
//
// Source code recreated from a .class file by IntelliJ IDEA
// (powered by FernFlower decompiler)
//

import java.io.Serializable;
import scala.runtime.BoxesRunTime;
import scala.runtime.IntRef;
import scala.runtime.ModuleSerializationProxy;
import scala.runtime.RichInt.;

public final class Ejemplo$ implements Serializable {
    public static final Ejemplo$ MODULE$ = new Ejemplo$();

    private Ejemplo$() {
    }

    private Object writeReplace() {
        return new ModuleSerializationProxy(Ejemplo$.class);
    }

    public void main(final String[] args) {
        IntRef i = IntRef.create(0);
        .MODULE$.until$extension(scala.Predef..MODULE$.intWrapper(1), 50).foreach((z) -> {
            scala.Predef..MODULE$.println(BoxesRunTime.boxToInteger(i.elem));
            int var3 = i.elem + 1;
            i.elem = var3;
        });
    }
}
```

## Rangos

```scala
var rango = 1 to 50
print(rango)
```

```scala
var rango = 1 until 50
print(rango)
```

```scala
var rango = 1 to 50 by 5
print(rango)
```

```scala
var letras = 'a' to 'j' by 2
for(x<-letras){
print(x)
}
print(rango)
```

## String

```scala
cadema="ABC"
cadena.length()
cadena.last
cadena.toUpperCase()
cadena.foreach(println)
cadena.toUpperCase.foreach(println)
println(s"Lema: $cadena .... $anho!")
```

## Colecciones

```scala
//Traversable
//Iterable

var lista=List("Walter","Franco","Daniel")
var lista=List("Walter","Franco",10)
lista.last
lista.head
lista.length

```

Trabajo 

- Traits
- Arrays
- Singleton
- Units
