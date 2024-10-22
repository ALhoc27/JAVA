---
order: 0.8
title: 2. Модификаторы доступа
---

В **Java** существует четыре модификатора доступа: `public`, `protected`, `default` (пакетный уровень) и `private`. Каждый из них определяет, в каких пределах доступен класс, метод или поле. Давайте подробно рассмотрим каждый модификатор, его особенности, области видимости и примеры.

:::note 

**Модификаторы доступа - \[**`public|protected|private`**\]**

:::

**Это модификаторы доступа:**

**−** `public` **(публичный):**

[html:iframe]

<dir style="background-color: transparent; color: #333; padding: 3px 6px; border-radius: 3px; font-size: 13px; font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, Arial, sans-serif;">Классы, методы, поля, конструкторы, помеченные модификатором  <span style="background-color: #f4f4f4; padding: 3px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">public</span> , <strong> доступны из любого места </strong>, так и из других классов и пакетов.</dir>

[/html]

**−** `private` **(приватный):**

[html:iframe]

<dir style="background-color: transparent; color: #333; padding: 3px 6px; border-radius: 3px; font-size: 13px; font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, Arial, sans-serif;">Члены класса, помеченные модификатором  <span style="background-color: #f4f4f4; padding: 3px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">private</span> , <strong> видны только внутри того же класса </strong>. Они не доступны извне класса, включая подклассы.</dir>

[/html]

**−** `protected` **(защищенный):**

[html:iframe]

<dir style="background-color: transparent; color: #333; padding: 3px 6px; border-radius: 3px; font-size: 13px; font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, Arial, sans-serif;"><span style="background-color: #f4f4f4; padding: 3px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">protected</span> - это также модификатор доступа, что и <span style="background-color: #f4f4f4; padding: 3px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">default</span>, но с более широким уровень доступа.<br/>Члены класса, помеченные модификатором <span style="background-color: #f4f4f4; padding: 3px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">protected</span> , <strong> видны классе, в внутри пакета, а также в подклассах </strong>(даже если они находятся в другом пакете)</dir>

[/html]

**−** `default` **(по умолчанию, package-private)**

[html:iframe]

<dir style="background-color: transparent; color: #333; padding: 3px 6px; border-radius: 3px; font-size: 13px; font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, Arial, sans-serif;">Если член класса не имеет явного модификатора доступа (т.е., не помечен как  <span style="background-color: #f4f4f4; padding: 3px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">public</span> , <span style="background-color: #f4f4f4; padding: 3px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">private</span> или <span style="background-color: #f4f4f4; padding: 3px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">protected</span>, то он <strong> считается доступным только внутри своего собственного пакета.</strong></dir>

[/html]

![](./obektno-orientirovannoe-programmirovani.png)

### Рекомендации:

-  **Используйте** `private` для полей и методов, чтобы скрыть детали реализации.

-  **Используйте** `protected` для того, чтобы дать доступ потомкам в иерархии классов.

-  **Используйте** `default`, если класс или метод предназначен для использования только внутри пакета.

-  **Используйте** `public`, если метод или класс должен быть доступен повсюду.

### Мы применяем только два модификатора **public** и **private**. 

**\- Почему так?**

Модификаторы **default** и **protected** связаны с тонкостями проектирования. В большинстве случаев программист ошибается с выбором этих модификаторов и в дальнейшем изменяет существующий код. Так же модификаторы **default** и **protected** соблазняют программиста делать расширение кода за счет наследования (лучше избегать). Этот механизм жестко связывает элементы. Далее в курсе мы увидим возникающую из этого проблему.

Поэтому общее правило в курсе.

1\. Для всех полей используем только модификатор **private**.

2\. Для классов и методов - **public**/**private**.