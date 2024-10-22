---
order: 1
title: Admin
---

[html:iframe]

<table style="background-color: transparent; width: 100%; border-collapse: collapse;">
  <tr>
    <td style="border: 2px solid #ddd; padding: 8px;»><p style=«background-color: transparent; color: #333; padding: 3px 6px; border-radius: 3px; font-size: 16px; font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, Arial, sans-serif;">
      <dir style="background-color: transparent; color: #333; padding: 3px 6px; border-radius: 3px; font-size: 15px; font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, Arial, sans-serif;">Исключения ( <span style="background-color: #f4f4f4; padding: 4px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">Exceptions</span> ) позволяют программисту корректно реагировать на ошибки, предотвращая крах приложения.</dir>
    </td>
  </tr>
</table>

<dir style="background-color: transparent; color: #333; padding: 3px 6px; border-radius: 3px; font-size: 13px; font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, Arial, sans-serif;">Исключения ( <span style="background-color: #f4f4f4; padding: 3px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">Exceptions</span> ) позволяют программисту корректно реагировать на ошибки, предотвращая крах приложения.</dir>

<dir style="padding-left: 6px !important; font-family: Tahoma, sans-serif; font-size: 13px; color: #000; line-height: 1.5; letter-spacing: 0.5px;">Классы, методы, поля, конструкторы, помеченные модификатором <span style="background-color: #f4f4f4; padding: 3px 6px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">public</span> , <mark style="background-color: transparent; font-weight: normal; color: #AE4C00;"> доступны из любого места </mark>, так и из других классов и <strong> пакетов </strong>. 
</dir>

<h2 style="background-color: transparent; color: #171717; padding: 3px 6px; border-radius: 3px; font-size: 17px; font-family: -apple-system, BlinkMacSystemFont, Roboto, 'Helvetica Neue', Arial, sans-serif; font-weight: 450;">
  &nbsp;&nbsp;final: (final - значит неизменяемая)
</h2>
<h2 style="background-color: transparent; color: #171717; padding: 3px 6px; border-radius: 3px; font-size: 18px; font-family: font-family: 'Courier New', Courier, monospace; font-weight: 500;">
  &nbsp;&nbsp;final: (final - значит неизменяемая)
</h2>


[/html]

{% table %}

---

*  {% colwidth=[325] %}

   # `#`  Sasha

   ## `##`  Sasha

   ### `###`  Sasha

   #### `####`  Sasha

*  {% colwidth=[429] %}

   ```
   font-weight: bold;
   font-style: italic;
   font-size: 20px;
   border-radius: 5px; padding: 5px;
   text-shadow: 2px 2px 5px gray;
   font-family: 'Courier New', Courier, monospace;
   background-color: transparent;
   color: rgba(255, 165, 0, 0.2);
   ```

{% /table %}

{% table %}

---

*  {% colwidth=[324] %}

   [html:iframe]

   <pre style="background-color: transparent; padding: 10px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">
      `123` - code
      **Class Loader** - Жирный
      ```java
      < i > - курсив < /i >
      </pre>

   [/html]

*  {% colwidth=[2855] %}

   ```
   <pre style="background-color: transparent; padding: 10px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">
      `123` - code
      **Class Loader** - Жирный
      ```java
   </pre>
   ```

---

*  {% colwidth=[324] %}

   [html:iframe]

   <mark style="background-color: #f4f4f4; padding: 10px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">
      полупрозрачным оранжевым<strong> фоном </strong>
      </mark>

   [/html]

*  {% colwidth=[2855] %}

   ```
   <mark style=«background-color: #f4f4f4; padding: 10px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;»>
      полупрозрачным оранжевым<strong> фоном </strong> </mark>
   ```

---

*  {% colwidth=[324] %}

   [html:iframe]

   <p style="font-family: Tahoma, sans-serif; font-size: 15px; color: #000; line-height: 1.5; letter-spacing: 0.5px;">
         Текст с <mark style="background-color: rgba(255, 165, 0, 0.3); font-weight: normal; padding: 2px 6px; border: 1px solid #ccc;">полупрозрачным оранжевым фоном</mark> и строгим классическим <mark style="background-color: transparent; font-weight: normal; color: #AE4C00;"> фоном </mark>стилем шрифта <strong>Tahoma</strong>.
      </p>

   [/html]

*  {% colwidth=[2855] %}

   ```
   <p style=«font-family: Tahoma, sans-serif; font-size: 15px; color: #000; line-height: 1.5; letter-spacing: 0.5px;»>
      Текст с <mark style=«background-color: rgba(255, 165, 0, 0.3); font-weight: normal; padding: 2px 6px; border: 1px solid #ccc;«>полупрозрачным оранжевым фоном</mark> и строгим классическим <mark style=»background-color: transparent; font-weight: normal; color: #AE4C00;»> фоном </mark>стилем шрифта <strong>Tahoma</strong>. 
   </p>
   ```

---

*  {% colwidth=[324] %}

   [html:iframe]

   <p style="font-family: Tahoma, sans-serif; font-size: 16px; color: #444; line-height: 1.6; letter-spacing: 0.5px;">
         Текст с <mark style="background-color: rgba(255, 165, 0, 0.2); font-weight: normal; padding: 3px 8px; border: 1px solid #ddd; border-radius: 3px;">мягким полупрозрачным оранжевым фоном</mark> и более плавным <mark style="background-color: transparent; font-weight: normal; color: #AE4C00;">fewfwewfwew <strong>fsf</strong></mark> оформлением.
      </p>

   [/html]

*  {% colwidth=[2855] %}

   ```
    <p style=«font-family: Tahoma, sans-serif; font-size: 16px; color: #444; line-height: 1.6; letter-spacing: 0.5px;»>
      Текст с <mark style=«background-color: rgba(255, 165, 0, 0.2); font-weight: normal; padding: 3px 8px; border: 1px solid #ddd; border-radius: 3px;«>мягким полупрозрачным оранжевым фоном</mark> и более плавным <mark style=»background-color: transparent; font-weight: normal; color: #AE4C00;»>fewfwewfwew <strong>fsf</strong></mark> оформлением. 
   </p>
   ```

---

*  {% colwidth=[324] %}

   [html:iframe]

   <mark style="background-color: transparent; color: #333; padding: 3px 6px; border-radius: 3px; font-size: 16px; font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, Arial, sans-serif;"> &nbsp&nbsp Один класс - один родитель.</mark>

   [/html]

*  {% colwidth=[2855] %}

   ```
      <mark style=«background-color: transparent; color: #333; padding: 3px 6px; border-radius: 3px; font-size: 16px; font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, Arial, sans-serif;»> &nbsp&nbsp Один класс - один родитель.</mark>
   ```

---

*  {% colwidth=[324] %}

   [html:iframe]

   <mark style="background-color: transparent; color: #2F1704; font-family: 'Courier New', Courier, monospace; font-weight: bold; font-size: 18px;">Один класс - один родитель.</mark>

   [/html]

*  {% colwidth=[2855] %}

   ```
      <mark style=«background-color: transparent; color: #2F1704; font-family: 'Courier New', Courier, monospace; font-weight: bold; font-size: 18px;»>Один класс - один родитель.</mark>
   ```

---

*  {% colwidth=[324] %}

   [html:iframe]

   <mark style="background-color: transparent; color: black; font-family: font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, sans-serif !important; font-size: 16px !important;">Один <strong>класс</strong> - один родитель.</mark>

   [/html]

*  {% colwidth=[2855] %}

   ```
      <mark style=«background-color: transparent; color: black; font-family: font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, sans-serif !important; font-size: 16px !important;»> &nbsp&nbsp Один <strong>класс</strong> - один родитель.</mark>
   ```

{% /table %}

```
{% table %}

---

*  {% colwidth=[375] isHeader=true %}

&nbsp;

*  {% colwidth=[398] isHeader=true %}

   

---

*  {% colwidth=[375] %}

	```java

	```

*  {% colwidth=[398] %}


{% /table %}
```

[html:iframe]

<table style="background-color: transparent; width: 100%; border-collapse: collapse;">
  <tr>
    <td style="border: 2px solid #ddd; padding: 8px;»><p style=«background-color: transparent; color: #333; padding: 3px 6px; border-radius: 3px; font-size: 16px; font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, Arial, sans-serif;">
      <dir style="background-color: transparent; color: #333; padding: 3px 6px; border-radius: 3px; font-size: 15px; font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, Arial, sans-serif;"> &nbsp&nbsp Один класс - один родитель.eveveerere &nbsp;&nbsp;<span style="background-color: #f4f4f4; padding: 4px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">полупрозрачным оранжевым<strong> фоном</strong></span> d33crccre erferfe</dir>
    </td>
  </tr>
</table>

[/html]

[html:iframe]

<table style="background-color: transparent; width: 100%; border-collapse: collapse;">
  <tr>
    <td style="border: 2px solid #ddd; padding: 8px;»><p style=«background-color: transparent; color: #333; padding: 3px 6px; border-radius: 3px; font-size: 16px; font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, Arial, sans-serif;">
      <dir style="background-color: transparent; color: #333; padding: 3px 6px; border-radius: 3px; font-size: 15px; font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, Arial, sans-serif;">Исключения ( <span style="background-color: #f4f4f4; padding: 4px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">Exceptions</span> ) позволяют программисту корректно реагировать на ошибки, предотвращая крах приложения.</dir>
    </td>
  </tr>
</table>

<dir style="background-color: transparent; color: #333; padding: 3px 6px; border-radius: 3px; font-size: 13px; font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, Arial, sans-serif;">Исключения ( <span style="background-color: #f4f4f4; padding: 3px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">Exceptions</span> ) позволяют программисту корректно реагировать на ошибки, предотвращая крах приложения.</dir>

<dir style="padding-left: 6px !important; font-family: Tahoma, sans-serif; font-size: 13px; color: #000; line-height: 1.5; letter-spacing: 0.5px;">Классы, методы, поля, конструкторы, помеченные модификатором <span style="background-color: #f4f4f4; padding: 3px 6px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">public</span> , <mark style="background-color: transparent; font-weight: normal; color: #AE4C00;"> доступны из любого места </mark>, так и из других классов и пакетов. 
</dir>

[/html]

[html:iframe]

<p>Исключения (Exceptions) позволяют программисту корректно реагировать на ошибки, предотвращая крах приложения.</p>

<dir style="background-color: transparent; color: #333; padding: 3px 6px; border-radius: 3px; font-size: 13px; font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, Arial, sans-serif;">Исключения ( <span style="background-color: #f4f4f4; padding: 3px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">Exceptions</span> ) позволяют программисту корректно реагировать на ошибки, предотвращая крах приложения.</dir>

<dir style="padding-left: 6px !important; font-family: Tahoma, sans-serif; font-size: 13px; color: #000; line-height: 1.5; letter-spacing: 0.5px;">Классы, методы, поля, конструкторы, помеченные модификатором <span style="background-color: #f4f4f4; padding: 3px 6px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">public</span> , <mark style="background-color: transparent; font-weight: normal; color: #AE4C00;"> доступны из любого места </mark>, так и из других классов и пакетов. 
</dir>



<dir style="background-color: transparent; color: #333; padding: 3px 6px; border-radius: 3px; font-size: 13px; font-family: -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, Arial, sans-serif;">Классы, методы, поля, конструкторы, помеченные модификатором  <span style="background-color: #f4f4f4; padding: 3px; border-radius: 3px; overflow: auto; font-family: 'Courier New', Courier, monospace;">public</span> , <strong> доступны из любого места </strong>, так и из других классов и пакетов.</dir>

<h2 style="background-color: transparent; color: #171717; padding: 3px 6px; border-radius: 3px; font-size: 17px; font-family: -apple-system, BlinkMacSystemFont, Roboto, 'Helvetica Neue', Arial, sans-serif; font-weight: 450;">
  &nbsp;&nbsp;final: (final - значит неизменяемая)
</h2>
<h2 style="background-color: transparent; color: #171717; padding: 3px 6px; border-radius: 3px; font-size: 18px; font-family: font-family: 'Courier New', Courier, monospace; font-weight: 500;">
  &nbsp;&nbsp;final: (final - значит неизменяемая)
</h2>

[/html]