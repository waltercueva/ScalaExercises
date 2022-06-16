```scala
import java.io._
object Main extends App{
  def funcion(a:Int):Int=5*a
  println(funcion(10))
}
```

## Singleton

```scala
object Calculadora{
  def sum(a:Int=0, b:Int=0): Int =a+b
  def res(a:Int=0, b:Int=0): Int =a-b
}
object Main {
  def funcion(a:Int):Int=5*a
  def main(args: Array[String]): Unit = {

    System.out.println(Calculadora.sum(10,5))
    println(Calculadora.res(10,5))
  }
}
```

## Creando Objeto

```scala
class Calculadora(){
  def sum(a:Int=0, b:Int=0): Int =a+b
  def res(a:Int=0, b:Int=0): Int =a-b
}
object Main {
  def main(args: Array[String]): Unit = {
    val c =new Calculadora()
    System.out.println(c.sum(10,5))
    println(c.res(10,5))
  }
}
```

## Tipedef

```scala
object Main {
  def main(args: Array[String]): Unit = {
    type Correo= String
    val c=new Correo("waltercueva@gmail.com")
    print(c)

  }
}
```

## Case Class

```scala
case class Universidad(nombre:String, ubigeo:Int)
object Main {
  def main(args: Array[String]): Unit = {
    val objU=Universidad("UPC",1234)
    val objU2=Universidad("PUCP",4567)
    println(objU.hashCode())
    //print(objU.nombre)
    //print(objU.ubigeo)
    println(objU.toString)
    println(objU.equals(objU2))
    println(objU.equals(objU))
  }
}
```

## Herencia

```scala
class Universidad(var nombre:String, var ubigeo:Int){
  nombre=nombre.toUpperCase
  ubigeo=ubigeo+2
  override def toString= nombre+"\t" +ubigeo+"\n"
}
class Demo(nombre:String, ubigeo:Int) extends Universidad(nombre, ubigeo){
  nombre.toLowerCase()  
}
object Main {
  def main(args: Array[String]): Unit = {

    val objU=new Demo("uPc",1234)
    println(objU.ubigeo)
    println(objU.nombre)
  }
}
```

## POJO

```scala
class Universidad(var nombre:String, var ubigeo:Int){
  nombre=nombre.toUpperCase
  ubigeo=ubigeo+2
  override def toString= nombre+"\t" +ubigeo+"\n"
}
class Demo(nombre:String, ubigeo:Int) extends Universidad(nombre, ubigeo){
  nombre.toLowerCase()
}
object Main {
  def main(args: Array[String]): Unit = {

    val objU=new Demo("uPc",1234)
    println(objU.ubigeo)
    println(objU.nombre)
  }
}
```

```scala
class Cuenta(val n:String, val p:String){
  var nombre:String=n
  var password:String =p  
  def _print(): Unit ={
    print(nombre+"\t" +password+"\t")
  }
}
class Free(override val n:String,override val  p:String, val pl:String ) extends Cuenta(n, p){
  var plan:String=pl
  override def _print(): Unit ={
    super._print()
    println(pl)
  }
}

object Main {
  def main(args: Array[String]): Unit = {
    val objF1=new Free(p="walter2022",n="walter",pl="F")
    objF1._print()

  }
}
```

## Traits

```scala
trait Cuenta

trait Impresion{
  def _print:Unit//definido mas no implementado
}

trait Free{
  val permisos:String
  def historial():String="historial"
}

class Personal extends  Cuenta with Free with Impresion{
  override val permisos:String="Generar Contrsenha"
  override def _print(): Unit ={//reescribo el metodo abstracto
    println(permisos)
  }
}

object Main {
  def main(args: Array[String]): Unit = {
    val objF1=new Personal
    objF1._print()
  }
}
```
