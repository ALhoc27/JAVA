---
order: 5.8
title: "Инструменты "
---

#### Пример переопределения методов (Override)

Но подклассы могут и реализовывать свои методы, то есть **переопределять** методы базового класса для изменения их поведения.

```java
// Базовый класс (родительский класс)
class Animal {
    // Метод базового класса
    public void sound() {
        System.out.println("Animal makes a sound");
    }
}

// Подкласс (наследующий класс)
class Dog extends Animal {
    // Переопределение метода базового класса
    @Override
    public void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        // Создание объекта подкласса Dog
        Dog dog = new Dog();
        
        // Вызов переопределенного метода
        dog.sound();  // Выведет: Dog barks
    }
}
```

### Объяснение:

В классе `Dog` метод `sound()` из класса `Animal` был переопределен. Теперь при вызове метода `sound()` у объекта `Dog` будет выведено «Dog barks», а не «Animal makes a sound».

**Для переопределения** в дочернем классе(под классе) указывается метод, **c такой же сигнатурой**(именем и параметрами) **и с таким же возвращающимся типом**

[html:iframe]

<hr/>

[/html]


