Demo.kt

this kotlin code is solely used a practice, to learn how to code in kotlin
and learn practice using git hub.

//=================================================Class Student=================================================
open class Student (e:String){ // make the class open to allow inheritance
    var type:String = ""
    init { // default constructor of the parent class
        type = e
    }
    open fun show(){ // make the method open to allow overriding
        println("Is a Student")
    }
}
//=================================================class Engineer=================================================
class Engineer (n:String, a:String): Student(a){ // declaring a subclass of student with a default constructor
    var name:String = ""
    init {// defining the default constructor
        name = n
    }
    override fun show(){ // overriding the inherited method
        print("$name is a $type") // print both Strings, included the ones inherited
    }
}
//================================================= main =================================================
fun main (args: Array<String>){ // main

    var papa = Engineer("Papa", "Great Edngineer") // object with default constructor
    papa.show() // call the method of the class Engineer
}
//Papa is an Engineer
