- [Java OOP](#java-oop)
  - [Klassen vs. Objekte](#klassen-vs-objekte)
- [Java Klassen und Objekte](#java-klassen-und-objekte)
  - [Aufbau von Klassen](#aufbau-von-klassen)
  - [Klasse erstellen](#klasse-erstellen)
    - [Mehrere Klassen](#mehrere-klassen)
  - [Objekt erstellen](#objekt-erstellen)
    - [Mehrere Objekte erstellen](#mehrere-objekte-erstellen)
- [Java Klassen Attribute](#java-klassen-attribute)
- [Java Konstruktor](#java-konstruktor)
  - [Konstruktor Parameter](#konstruktor-parameter)
- [this Keyword](#this-keyword)
- [Javadoc Kommentare](#javadoc-kommentare)
- [Java Interfaces](#java-interfaces)
  - [Interface implementieren](#interface-implementieren)
  - [Warum und Wann?](#warum-und-wann)



# Java OOP
OOP = Object-Oriented Programming

Bei der objektorientierten Programmierung geht es darum, Objekte zu erstellen, die sowohl Daten als auch Methoden enthalten.

## Klassen vs. Objekte
**Class**: Fruit -> Bauplan
**objects**: Apple, Banana, Mango -> Instanzen

Eine Klasse ist eine Vorlage für Objekte und Objekte sind Instanzen einer Klasse.

Die einzelnen Objekte erben alle Variablen und Methoden der Klasse.

# Java Klassen und Objekte
Java ist eine objektorientierte Programmiersprache.

Alles in Java ist mit Klassen und Objekten verbunden.

---
## Aufbau von Klassen

**Syntax**
```java
class ClassName {
    // fields

    // constructor

    // methods

}
```

## Klasse erstellen

**Syntax**
```java
public class ClassName {
	//Attribute
	private int attr1;
	private String attr2;
	
}
```

**Beispiel**
```java
public class Main {
    int x = 5;
}
```

> [!NOTE]
> Klassennamen beginnen immer mit einem Grossbuchstaben und das `.java`-File muss den gleichen Namen haben.

---
### Mehrere Klassen
Ein Objekt kann in einer Klasse erstellt werden und in einer anderen Klasse darauf zugegriffen werden.

**Beispiel**
```java
// Main.java
public class Main {
  int x = 5;
}
```
```java
// Second.java
class Second {
  public static void main(String[] args) {
    Main myObj = new Main();
    System.out.println(myObj.x);
  }
}
```

---
## Objekt erstellen

**Beispiel**
```java
public class Main {
  int x = 5;

  public static void main(String[] args) {
    Main myObj = new Main();
    System.out.println(myObj.x);
  }
}
```
### Mehrere Objekte erstellen

**Beispiel**
```java
public class Main {
  int x = 5;

  public static void main(String[] args) {
    Main myObj1 = new Main();  // Object 1
    Main myObj2 = new Main();  // Object 2
    System.out.println(myObj1.x);
    System.out.println(myObj2.x);
  }
}
```

---
# Java Klassen Attribute

**Beispiel**
```java
public class Main {
  int x = 5; // Attribut 1
  int y = 3; // Attribut 2
}
```

---
# Java Konstruktor
Der Konstruktor ist eine spezielle Methode um Objekte zu erstellen.

Eine Klasse kann mehrere Konstruktoren haben, solange sie sich unterscheiden.

**Syntax**
```java
public ClassName() {
	String attr1 = value;
	int attr2 = value;
}
```
mit Parameter
```java
public ClassName(String param1, int param2) {
	this.attr1 = param1;
	this.attr2 = param2;
}
```

**Beispiel**
```java
// Create a Main class
public class Main {
  int x;  // Create a class attribute

  // Create a class constructor for the Main class
  public Main() {
    x = 5;  // Set the initial value for the class attribute x
  }

  public static void main(String[] args) {
    Main myObj = new Main(); // Create an object of class Main (This will call the constructor)
    System.out.println(myObj.x); // Print the value of x
  }
}

// Outputs 5
```

> [!NOTE]
> Der Konstruktorname muss gleich sein wie der Klassenname und hat **keinen** Rückgabewert.
>
> Alle Klassen haben standardmässig einen Konstruktor, auch wenn keiner erstellt wurde.

---
## Konstruktor Parameter
Constructors can also take parameters, which is used to initialize attributes.

The following example adds an int y parameter to the constructor. Inside the constructor we set x to y (x=y). When we call the constructor, we pass a parameter to the constructor (5), which will set the value of x to 5:

```java
public class Main {
  int x;

  public Main(int y) {
    x = y;
  }

  public static void main(String[] args) {
    Main myObj = new Main(5);
    System.out.println(myObj.x);
  }
}

// Outputs 5
```
Es sind beliebig viele Parameter möglich:

```java
public class Main {
  int modelYear;
  String modelName;

  public Main(int year, String name) {
    modelYear = year;
    modelName = name;
  }

  public static void main(String[] args) {
    Main myCar = new Main(1969, "Mustang");
    System.out.println(myCar.modelYear + " " + myCar.modelName);
  }
}

// Outputs 1969 Mustang
```

# this Keyword
Das Keyword `this` bezieht sich auf das aktuelle Objekt und wird verwendet um Verwechslungen zu vermeiden.

**Beispiel**
```java
public class Main {
  int x;  // Class variable x

  // Constructor with one parameter x
  public Main(int x) {
    this.x = x; // refers to the class variable x
  }

  public static void main(String[] args) {
    // Create an object of Main and pass the value 5 to the constructor
    Main myObj = new Main(5);
    System.out.println("Value of x = " + myObj.x);
  }
}
// Output: Value of x = 5
```

# Javadoc Kommentare

```java
/**
* Dies ist ein Javadoc Kommentar
*/
public class ClassName {
	/**
	* Javadoc wird verwendet, um automatisch HTML-Dokumentationen
	* aus speziellen Kommentaren im Quellcode zu generieren.
	* Die Kommentare beschreiben Klassen, Methoden, Felder 
	* und andere wichtige Elemente im Code.
	* @param: Parametername Beschreibung
	* @return: Beschreibung von Rückgabewert
	* @throws/@exception: dokumentiert Ausnahmen
	* @see: verweist auf verwandte Klassen oder Methoden
	* @since: Git Version seit der Verfügbarkeit einer Klasse an
	* @deprecated: Markiert eine Klasse oder
	*/
}
```

---
# Java Interfaces
Interfaces (Schnittstellen) sind vollständig abstrakte Klassen.

Sie dienen dazu, verwandte Methoden mit leerem "Body" zu gruppieren.

**Syntax**
```java
interface InterfaceName {
    public void method1();
    public void method2();
}
```

> [!NOTE]
> - Wie abstrakte Klassen können Interfaces **keine** Objekte erstellen
> - Interface Methoden haben **keinen** Body
> - Beim implementieren eines Interfaces müssen **alle** Methoden überschrieben werden
> - Interface Methoden sind standardmässig `public` und `abstract`
> - Interface Attribute sind standardmässig `public`, `static` und `final`
> - Ein Interface hat **keinen** Konstruktor

## Interface implementieren

**Syntax**
```java
interface InterfaceOne {
    public void method1();
}
interface InterfaceTwo {
    public void method2();
}
// Class
class ClassName implements InterfaceOne, InterfacheTwo {
    public void method1() {
        // code to execute
    }
    public void method2() {
        // code to execute
    }
}
// Main
class Main {
    public static void main(String[] args) {
        ClassName objectName = new ClassName();
        objectName.method1();
        objectName.method2();
    }
}
```

## Warum und Wann?
1. Um die Sicherheit zu gewährleisten, sollten bestimmte Details ausgeblendet und nur die wichtigen Details eines Interface angezeigt werden.
2. Java erlaubt keine Mehrfachvererbung (eine Klasse kann nur von einer Superklasse erben). Aber sie kann mehrere Interfaces implementieren.