---
order: 0.5
title: Основы java (Вводная)
---

### 0\. **Знакомства с java**

:::info:true Подробнее

### 1\. **Установка окружения**

1. **JDK (Java Development Kit)**: Пакет для разработки на Java. Он включает в себя компилятор `javac` и JVM (Java Virtual Machine).

   -  Скачать: <https://www.oracle.com/java/technologies/javase-downloads.html>

2. **IDE или текстовый редактор**: Можно использовать IntelliJ IDEA, Eclipse или Sublime Text (если вы предпочитаете лёгкий редактор).

3. **Maven** (опционально): Система управления зависимостями и сборкой для проектов на Java.

Проверка установки:

```bash
java -version
javac -version
```

---

### 2\. **Первая программа на Java**

Создадим простой класс с выводом «`Hello, World!`» на экран.

**Код:**

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

**Объяснение:**

-  **public**: Доступен всем.

-  **class**: Объявляет класс.

-  **main**: Это точка входа в программу. JVM ищет метод `main` для начала выполнения.

-  **String\[\] args**: Аргументы командной строки.

-  **System.out.println()**: Выводит текст в консоль.

**Компиляция и запуск:**

```bash
javac HelloWorld.java
java HelloWorld
```

---

### 3\. **Переменные и типы данных**

В Java необходимо объявлять тип переменной перед ее использованием.

**Пример:**

```java
int age = 25;              // Целое число
double price = 19.99;       // Число с плавающей точкой
char letter = 'A';          // Символ
boolean isJavaFun = true;   // Логический тип
String name = "Alice";      // Строка
```

#### Примитивные типы данных:

-  `byte`, `short`, `int`, `long` – целые числа.

-  `float`, `double` – числа с плавающей точкой.

-  `char` – символы.

-  `boolean` – логический тип (true/false).

---

### 4\. **Управляющие конструкции**

#### Условные операторы (`if`/`else`):

```java
int number = 10;
if (number > 0) {
    System.out.println("Положительное число");
} else {
    System.out.println("Отрицательное число");
}
```

#### Циклы:

1\. `for`:

```java
for (int i = 0; i < 5; i++) {
    System.out.println(i);
}
```

2\. `while`:

```java
int i = 0;
while (i < 5) {
    System.out.println(i);
    i++;
}
```

---

### 5\. **Методы**

Метод -- это блок кода, который выполняет определённую задачу.

#### Пример метода:

```java
public class Calculator {
    public static int add(int a, int b) {
        return a + b;
    }

    public static void main(String[] args) {
        int result = add(5, 3);
        System.out.println("Результат: " + result);
    }
}
```

#### Объяснение:

-  `int add(int a, int b)`: Метод принимает два параметра и возвращает сумму.

-  Вызов метода из `main`: `add(5, 3)`.

---

### 6\. **Классы и объекты**

Java поддерживает объектно-ориентированное программирование (ООП). Основные концепции:

-  **Класс** -- это шаблон для создания объектов.

-  **Объект** -- экземпляр класса.

#### Пример:

```java
public class Car {
    String model;
    int year;

    // Конструктор
    public Car(String model, int year) {
        this.model = model;
        this.year = year;
    }

    public void displayInfo() {
        System.out.println("Модель: " + model + ", Год: " + year);
    }

    public static void main(String[] args) {
        Car car1 = new Car("Toyota", 2020);
        car1.displayInfo();
    }
}
```

#### Объяснение:

-  Конструктор используется для инициализации объекта.

-  Метод `displayInfo()` выводит информацию о машине.

---

### 7\. **Коллекции и массивы**

#### Массив:

```java
int[] numbers = {1, 2, 3, 4, 5};
System.out.println(numbers[0]);  // Выводит 1
```

#### ArrayList:

```java
import java.util.ArrayList;

public class Example {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Java");
        list.add("Python");
        System.out.println(list);
    }
}
```

---

### 8\. **Исключения**

Исключения (exceptions) обрабатывают ошибки во время выполнения.

#### Пример обработки:

```java
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Ошибка: Деление на ноль!");
} finally {
    System.out.println("Блок finally выполняется всегда.");
}
```

---

### 9\. **Работа с Maven**

Если вы используете Maven, создайте проект и добавьте зависимости в файл `pom.xml`.

```xml
<dependencies>
    <dependency>
        <groupId>org.apache.commons</groupId>
        <artifactId>commons-lang3</artifactId>
        <version>3.12.0</version>
    </dependency>
</dependencies>
```

Для сборки проекта:

```bash
mvn compile
mvn exec:java -Dexec.mainClass="com.example.Main"
```

---

## 10\. **Заключение и дальнейшие шаги**

После освоения основ Java вы можете углубиться в следующие темы:

1. **ООП**: Наследование, полиморфизм, интерфейсы.

2. **Потоки (Threads)** и многопоточность.

3. **Работа с базами данных** (JDBC, Hibernate).

4. **Веб-приложения** (Spring, Java EE).

:::

### 1\. **Классы и объекты**

Java является объектно-ориентированным языком программирования, где основными строительными блоками являются **классы** и **объекты**.

-  **Класс** -- это шаблон или чертеж для создания объектов. Он описывает свойства ([comment:9olqM]поля[/comment]) и поведение (методы), которые будут у объектов.

-  **Объект** -- это экземпляр класса. Объект обладает конкретными значениями полей и может вызывать методы.

:::note:true Пример:

В этом примере создадим пользовательский класс `Car`, поля `model `и `year`, конструктор `public Car(String model, int year)` (*Класс получился без методов, хотя конечно в реальных программах, вся функциональность и все действия над данными, полями происходит в методах*). В вызывающем классе `Main`, в этой строке `Car car1 = new Car("Toyota", 2020);`, мы создали объект класса `Car` с помощью конструктора `new Car("Toyota", 2020);` и присвоили ссылку на созданный объект ссылочной переменной  `car1` типа `Car`. (В классе `Main` как раз содержится метод(статичный) `static void main(String[] args)` , данный метод в java программах является точкой входа, с него начинается вся программа)

```java
// Класс Car
public class Car {
    // Поля класса
    String model;
    int year;

    // Конструктор
    public Car(String model, int year) {
        this.model = model;
        this.year = year;
    }
}

// Использование класса и создание объекта
public class Main {
    public static void main(String[] args) {
        Car car1 = new Car("Toyota", 2020); // создали объект с помощью конструктора
		Car car2 = new Car("Volvo", 2024);  // создали еще один объект
    }
}
```

:::

**Объект это вполне конкретная сущность**, мы можем создать множество разных объектов, по определенному каркасу, в данном случае каркасом служит класс `Car` , а ссылкой на объект является переменная `car1`. Например два разных объекта  car1 и car2  по одному шаблону.

### 2\. **Переменные**

Java поддерживает несколько типов переменных:

-  **Члены класса или как их называют поля класса (атрибуты)** -- это переменные, объявленные в классе, которые хранят состояние объекта.

-  **Локальные переменные** -- объявлены внутри методов и существуют только в их пределах.

-  **Статические переменные** -- переменные, принадлежащие классу, а не конкретному объекту.

-  **Финальные переменные** -- означает, что переменная, помеченная как `final`, не может быть изменена после присвоения значения.

### 3\. **Типы данных**

Java -- это статически типизированный язык, что означает, что каждый объект и переменная должны иметь определенный тип данных. В Java существуют два основных типа данных:

#### Примитивные тип данных (базовый тип), всего их 8:

{% table %}

---

*  {% colwidth=[88] isHeader=true %}

   Тип

*  {% colwidth=[244] isHeader=true %}

   Размер

*  {% colwidth=[283] isHeader=true %}

   Диапазон

*  {% colwidth=[161] isHeader=true %}

   По умолчанию:

---

*  {% colwidth=[88] %}

   [comment:KxMVb]byte[/comment]

*  {% colwidth=[244] %}

   8 бит (1 байт)

*  {% colwidth=[283] %}

   от -128 до 127

*  {% colwidth=[161] %}

   0

---

*  {% colwidth=[88] %}

   [comment:av8Nj]short[/comment]

*  {% colwidth=[244] %}

   16 бит (2 байта)

*  {% colwidth=[283] %}

   от -32,768 до 32,767

*  {% colwidth=[161] %}

   0

---

*  {% colwidth=[88] %}

   [comment:AmVpf]int[/comment]

*  {% colwidth=[244] %}

   32 бита (4 байта)

*  {% colwidth=[283] %}

   [comment:tnIUN]от -2^31 до 2^31-1 [/comment]

*  {% colwidth=[161] %}

   0

---

*  {% colwidth=[88] %}

   [comment:8Vqnd]long[/comment]

*  {% colwidth=[244] %}

   64 бита (8 байт)

*  {% colwidth=[283] %}

   от -2^63 до 2^63-1

*  {% colwidth=[161] %}

   0[comment:eRgyi]L[/comment]

---

*  {% colwidth=[88] %}

   [comment:sX1hS]float[/comment]

*  {% colwidth=[244] %}

   32 бита (4 байта)

*  {% colwidth=[283] %}

   [comment:UGuOb]от \~1.4e−45 до \~3.4e+38[/comment]

*  {% colwidth=[161] %}

   0\.0f

---

*  {% colwidth=[88] %}

   [comment:o6vZm]double[/comment]

*  {% colwidth=[244] %}

   64 бита (8 байт)

*  {% colwidth=[283] %}

   [comment:KzT2U]от \~4.9e−324 до \~1.8e+308[/comment]

*  {% colwidth=[161] %}

   0\.0d

---

*  {% colwidth=[88] %}

   [comment:c94GX]boolean[/comment]

*  {% colwidth=[244] %}

   [comment:2IQZV]Выделяется минимум 1 байт[/comment]

*  {% colwidth=[283] %}

   `true` или `false`

*  {% colwidth=[161] %}

   `false`

---

*  {% colwidth=[88] %}

   [comment:5NsEE]char[/comment]

*  {% colwidth=[244] %}

   16 бит (2 байта)

*  {% colwidth=[283] %}

   от `\u0000` (0) до `\uffff` (65,535)

*  {% colwidth=[161] %}

   `\u0000` или 0

{% /table %}

**Примитивные типы** хранят простые значения и имеют фиксированный размер.

#### **Ссылочные типы (все остальные)**:

1. **Классы (**`class`**)**: такие как `String`, `ArrayList`, **пользовательские классы**. (*Размер: зависит от класса и его полей*)

2. **Массивы(**`[]`**)**: могут быть массивами примитивных или ссылочных типов. (*Размер: зависит от типа данных массива и его длины, используется для хранения множества значений одного типа данных*)

3. **Интерфейсы (**`interface`**)**: объявляют методы, которые должны быть реализованы классами.

4. **Перечисления (**`enum`**)**: набор фиксированных констант, которые могут использоваться для задания значений переменной.

:::note:true Пример:

```java
int num = 5;           // Примитивный тип
String text = "Hello"; // Ссылочный тип
```

или пользовательский класс `Car`:

```java
public class Car {
    String model;
    boolean available;

    public Car(String model) {
        this.model = model;
    }
}
```

В нем:

```java
String model;               // Объявили переменную Ссылочного тип (Строка), значение по умолчанию null
boolean available = true;   // Объявили и присвоили в одном выражении переменной available типа boolean значение true,
// по умолчанию все создаваемые объекты типа Car, будут иметь значение true в поле available, если оно не переназначено.
```

Теперь мы можем создать ссылку типа `Car`, например:

```java
class Main {
    public static void main(String[] args) {
        Car car;                // Объявили Переменную car типа Car 
        car = new Car("VOLVO"); // вызвали конструктор, тем самым создали объект, и присвоили ссылку в переменную car 
        car.available = false;  // по ссылке обращаемся к полю available(переменной), и меняем его на значение false
    }
}
```

:::

**Ссылочные типы** хранят ссылки на объекты, что делает их более гибкими для сложных структур данных и объектов.

### 4\. **Методы**

Метод -- это блок кода, который выполняет определенное действие. Методы могут принимать параметры и возвращать значения(`return`), а могут и не принимать или не возвращать значения(`void`):

:::note:true Синтаксис метода:

```java
возвращаемый_тип имя_метода(параметры) {
    // Тело метода
    return значение;
}
```

**Пример** метода, который принимает 2 параметра `(int a, int b)` , и возвращает значение `int`, для этого в методе указывается  `return` и все что после, например выражение, которое вычисляется, в значение которое имеет тип `int` возвращается данным методом.

```java
public int addNumbers(int a, int b) {
    return a + b; // возвращает значение int 
}
```

Теперь можно написать так (опустим пока что не статический метод вызывается у экземпляра класса):

```java
int a = addNumbers(12, 32); // a будет равно = 44
```

**Пример** метода, который  не принимает значения и не возвращает результат:

```java
public class Car {
    String model;
    boolean available = true;

	// метод не принимает параметров, и не возвращает значений, т.е. указан тип void 
    void trueOnFalse() { 
        available = false;
    }
}

class Main {
    public static void main(String[] args) {
        Car car1 = new Car("Audi"); 
		// выводим на экран значения поля available объекта car1, оно равно true 
		System.out.println(car1.available); 
		// вызвали метод, не принимает аргументов, и не чего не возвращает, но меняет состояние объекта 
        car.availableCar(); 
		// теперь значение поля available объекта car1, равно false
		System.out.println(car1.available); 
    }
}
```

:::

### 6\. **Конструкторы**

Конструктор -- это специальный метод, который вызывается при создании объекта. Конструктор используется для инициализации объекта. По умолчанию конструктор есть у каждого класса `Имя класса()` в данном случае `Car()`, но мы его переопределили(т.е. создали свой `public Car(String model, int year)`, который инициализирует поля класса, конструкторов бывает несколько, с разными аргументами (*перегрузка*))

:::note:true Пример конструктора:

```java
public class Car {
    String model;
    int year;
   
    public Car(String model, int year) {  // Конструктор
        this.model = model;
        this.year = year;
    }
}
```

:::

При наследовании, дочерний класс наследует, как будет ясно далее по лекциям, все поля и методы, включая конструкторы.

#### Правила вызова конструкторов при наследовании:

1. **Конструктор родительского класса всегда вызывается** при создании объекта дочернего класса. Если вы явно не вызываете его, Java автоматически добавляет вызов **конструктора без параметров (**`super()`).

2. **Если в родительском классе нет конструктора без параметров**, то в дочернем классе **обязательно** нужно явно вызвать один из конструкторов родителя с помощью ключевого слова `super(...)`.

:::note:true Подробнее

```java
class Parent {
    public Parent(String name) {
        System.out.println("Parent constr " + name);
    }
}

class Child extends Parent {
    public Child() {
        // Вызов конструктора родителя должен быть явным
        super("Java");
        System.out.println("Child constr");
    }
}

public class Main {
    public static void main(String[] args) {
        Child child = new Child();
    }
}
```

:::

### 7\. **Наследование**

Java поддерживает наследование, **это один из ключевых принципов объектно-ориентированного программирования (ООП)**, позволяющий одному классу использовать свойства и методы другого класса. В Java наследование достигается с помощью ключевого слова `extends`.

:::note:true Пример наследования:

```java
// Базовый класс (родительский класс)
class Animal {
    public void eat() { // Метод базового класса
        System.out.println("This animal is eating");
    }
}

class Dog extends Animal { // Подкласс (дочерний класс)
    // Метод подкласса
    public void bark() {
        System.out.println("Собака лает");
    }
}

public class Main {
    public static void main(String[] args) {  
        Dog dog = new Dog(); // Создание объекта подкласса Dog

        // Вызов метода базового класса, у экземпляра нет такого метода, он его унаследовал
        dog.eat();  // Выведет: This animal is eating

        // Вызов метода подкласса
        dog.bark(); // Выведет: Собака лает
    }
}
```

### Объяснение:

-  **Класс** `Animal` является базовым классом, содержащим метод `eat()`, который может быть вызван любым его подклассом.

-  **Класс** `Dog` является подклассом и наследует все методы и поля класса `Animal`. В данном примере он наследует метод `eat()`.

-  Подкласс `Dog` также может иметь свои собственные методы, такие как `bark()`.

:::

### 8\. **Полиморфизм**

Java поддерживает полиморфизм, это возможность одного метода работать с разными типами объектов. Он позволяет одному и тому же методу обрабатывать разные объекты по-разному, в зависимости от типа объекта, на котором он вызывается. Полиморфизм реализуется через наследование **и интерфейсы**.

:::note:true Пример полиморфизма:

В этом примере создадим базовый класс `Animal` и два подкласса -- `Dog` и `Cat`. Каждый из этих классов будет реализовывать метод `sound()` по-своему.

```java
// Базовый класс
class Animal {
    public void sound() {
        System.out.println("The animal makes a sound");
    }
}

// Подкласс Dog
class Dog extends Animal {
    @Override
    public void sound() {
        System.out.println("The dog barks");
    }
}

// Подкласс Cat
class Cat extends Animal {
    @Override
    public void sound() {
        System.out.println("The cat meows");
    }
}

public class Main {
    public static void main(String[] args) {
        // Полиморфизм через ссылки на базовый класс
        Animal myAnimal = new Animal(); // Базовый объект
        Animal myDog = new Dog();       // Ссылка типа Animal ссылается на объект типа Dog 
        Animal myCat = new Cat();       // Ссылка типа Animal ссылается на объект Cat

        // Вызов метода sound() для каждого объекта
        myAnimal.sound();  // Выведет: The animal makes a sound
        myDog.sound();     // Выведет: The dog barks
        myCat.sound();     // Выведет: The cat meows
    }
}
```

Сильно забегая вперед, переменная типа в данном случае ограничивает доступ.

`Animal myDog;` - данная ссылка `myDog` типа `Animal` не имеет доступа так как **не имеет адреса(объекта)**, переменная просто обьявленна (*Через нее можно ссылаться на статические поля или методы, это те, которые принадлежат классу, а не экземпляру класса, но у нас таких нет*)

`Animal myDog = new Animal();` - данная ссылка `myDog` типа `Animal` имеет доступа **ко всем (доступным) полям и методам** (со стороны клиента -  пользователя данного экземпляра класса) **класса** `Animal`

`Animal myDog123 = new Dog();` - данная ссылка `myDog123` типа `Animal` имеет доступа **ко всем (доступным) полям и методам** (со стороны клиента -  пользователя данного экземпляра класса) **класса** `Animal`, поля и методы класса `Dog`, будут недоступны, **РЕАЛИЗАЦИЯ ПЕРЕОПРЕДЕЛЕННЫХ МЕТОДОВ БУДЕТ КЛАССА** `Dog`

`Animal myDog123 = new Dog();`

То есть по ссылке `myDog123` мы сможем получиться доступ ко всем доступным полям класса `Animal`, к классу `Dog` доступа нет, но все методы которые переопределили в классе `Dog`, будут доступны с реализацией переопределенной в `Dog`

(конечно если все эти классы находятся в связи наследования)

:::

### 9\. **Абстракция**

**Абстракция** -- одна из ключевых концепций объектно-ориентированного программирования (ООП). Она заключается в создании простых интерфейсов для сложных систем, скрывая детали реализации. Абстракция позволяет определить общие характеристики объектов, при этом конкретная реализация этих характеристик остается скрытой.

Абстракция реализуется в java, через **абстрактные классы** и **интерфейсы**

{% table %}

---

*  {% colwidth=[391] isHeader=true %}

   Пример **абстрактного класса:**

*  {% colwidth=[382] isHeader=true %}

   Пример **интерфейса:**

---

*  {% colwidth=[391] %}

   ```java
   abstract class Animal {
       abstract void makeSound();
   }
   ```

*  {% colwidth=[382] %}

   ```java
    interface Drawable {
       void draw();
   }
   ```

---

*  {% colwidth=[391] %}

   **Абстрактный класс** используется, когда у объектов есть общие черты и поведение, и вы хотите предоставить частичную реализацию или хранить состояние (поля). Он подходит, если классы образуют иерархию и должны наследовать общий функционал.

*  {% colwidth=[382] %}

   **Интерфейс** используется, когда нужно задать контракт (набор методов), который классы должны реализовать, но с возможностью множественной реализации и гибкости. Интерфейсы применяются, если разные классы могут выполнять похожие действия, но не обязательно связаны иерархически.

{% /table %}

### 10\. **Циклы**

Java поддерживает стандартные циклы, такие как:

-  `for` / `for-each`: Используется для повторений с известным количеством итераций или для обхода массивов и коллекций.

:::note:true Подробнее

{% table %}

---

*  {% colwidth=[374] isHeader=true %}

   **for**

*  {% colwidth=[389] isHeader=true %}

   **for-each (упрощенная версия для обхода \[\])**

---

*  {% colwidth=[374] %}

   ```java
   for (int i = 0; i < 3; i++) {
       System.out.println(i);  //  0, 1, 2
   }
   ```

*  {% colwidth=[389] %}

   ```java
   int[] numbers = {1, 2, 3};
   for (int num : numbers) {
       System.out.println(num);  //  1, 2, 3
   }
   ```

{% /table %}

:::

-  `while`: Выполняет цикл, пока условие истинно. *(когда количество итераций заранее неизвестно, цикл работает, пока условие истинно*)

:::note:true Подробнее

```java
int i = 0;
while (i < 3) {
    System.out.println(i);  // Вывод: 0, 1, 2
    i++;
}
```

:::

-  `do-while`: Выполняет цикл хотя бы один раз, затем проверяет условие для продолжения.

:::note:true Подробнее

```java
int i = 0;
do {
    System.out.println(i);  // Вывод: 0, 1, 2
    i++;
} while (i < 3);
```

:::

#### Ключевые слова `break` и `continue`

1. `break`: немедленно завершает выполнение цикла.

2. `continue`: пропускает оставшуюся часть текущей итерации и переходит к следующей.

:::note:true Подробнее

{% table %}

---

*  {% colwidth=[362] isHeader=true %}

   Пример с `break`:

*  {% colwidth=[406] isHeader=true %}

   Пример с `continue`:

---

*  {% colwidth=[362] %}

   ```java
   for (int i = 0; i < 10; i++) {
      if (i == 5) {
      // Прерывает цикл, если i равно 5
         break;  
      }
      System.out.println(i);
   }
   ```

*  {% colwidth=[406] %}

   ```java
   for (int i = 0; i < 5; i++) {
      if (i == 2) {
      // Пропускает итерацию, когда i равно 2
         continue;
      }
      System.out.println(i);
   }
   ```

{% /table %}

:::

### 11\. **Условные операторы**

Java предоставляет стандартные условные операторы:

-  `if`, `else if`, `else`, тернарный оператор ( `Результат = (Выражение) ? true : false`),  `switch`

   Используется для выполнения блока кода в зависимости от условия. Лучше подходит для более [comment:gQHFR]**сложных условий**[/comment] и проверок диапазонов.

:::note:true Синтаксис и пример:

```java
if (условие) {
    // код, если условие истинно
} else {
    // код, если условие ложно
}
```

Пример:

```java
int x = 10;
if (x > 5) {
    System.out.println("x больше 5");
} if else (x = 5) {
    System.out.println("x равно 5");
} else {
System.out.println("x меньше 5");
}
```

Можно так же использовать просто `if`

```java
if (x = 5) System.out.println("x равно 5");
```

:::

-  **Тернарный оператор** (`? :`)  - краткая форма условного оператора `if-else`

```java
переменная = (условие) ? значение1 : значение2;
```

`значение1` - вызывается если **условие** верно, `значение2` - если ложно

Пример:

```java
int x = 10;
String result = (x > 5) ? "Больше 5" : "Меньше или равно 5";
System.out.println(result);
```

-  `switch` (В некоторых случаях компилятор может оптимизировать switch *быстрее, чем множество* `if-else` (особенно для большого количества веток))

Используется для выбора одного из множества возможных вариантов на основе значения переменной.

:::quote 

Лучше подходит `switch` , если нужно проверять **одно значение** с множеством вариантов (конкретные константы).

:::

:::note:true Синтаксис:

```java
switch (переменная) {
    case значение1:
        // код, если переменная равна значение1
        break;
    case значение2:
        // код, если переменная равна значение2
        break;
    default:
        // код, если ни одно значение не совпадает
}
```

{% table %}

---

*  {% colwidth=[435] isHeader=true %}

   Пример старого `switch`

*  {% colwidth=[395] isHeader=true %}

   Новый синтаксис `switch`

---

*  {% colwidth=[435] %}

   ```java
   int day = 2;
   switch (day) {
       case 1:
           System.out.println("Понедельник");
           break;
       case 2:
           System.out.println("Вторник");
           break;
       case 3:
           System.out.println("Среда");
           break;
       case 4, 5:
           System.out.println("Четверг, Пятница");
           break;
       default:
           System.out.println("Неизвестный день");
   }
   ```

*  {% colwidth=[395] %}

   ```java
   int day = 2;
   String dayName = switch (day) {
    case 1, 2, 3 -> "Понедельник - Среда";
    case 4 -> "Четверг";
    case 5 -> "Пятница";
    default -> {
    	System.out.println("Не рабочий день");
        yield "Выходной";  // возвращаемое значение
    }
   "Неизвестный день";
   };
   System.out.println(dayName);  // Вывод: Понедельник - Среда
   ```

{% /table %}

:::