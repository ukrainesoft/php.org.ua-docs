Установка обробника виходу межі простору імен

-   [« xml\_set\_element\_handler](function.xml-set-element-handler.html)
    
-   [xml\_set\_external\_entity\_ref\_handler »](function.xml-set-external-entity-ref-handler.html)
    
-   [PHP Manual](index.html)
    
-   [Функции парсера XML](ref.xml.html)
    
-   Установка обробника виходу межі простору імен
    

# xmlsetendnamespacedeclhandler

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

xmlsetendnamespacedeclhandler — Встановлення обробника виходу за межі простору імен

### Опис

```methodsynopsis
xml_set_end_namespace_decl_handler(XMLParser $parser, callable $handler): bool
```

Задає обробник, який викликається під час виходу межі оголошення простору імен. Цей обробник буде викликатись для кожного оголошення простору імен після того, як обробляє закінчення елемента, в якому цей простір імен було оголошено.

**Застереження**

Ця подія не підтримується LibXML, тому зареєстрований обробник не буде називатися.

### Список параметрів

`parser`

Посилання на аналізатор XML.

`handler`

`handler` - рядок, що містить ім'я функції, який повинен бути визначений на момент виклику функції [xml\_parse()](function.xml-parse.html) з аналізатора `parser`

Функція з ім'ям `handler` повинна приймати два аргументи та повертати цілий результат. Якщо обробник поверне **`false`** (як і нічого не поверне), XML аналізатор припинить роботу, а функція [xml\_get\_error\_code()](function.xml-get-error-code.html) повертатиме константу **`XML_ERROR_EXTERNAL_ENTITY_HANDLING`**

```methodsynopsis
handler(XMLParser $parser, string $prefix)
```

`parser`

Перший аргумент parser є посиланням на XML-аналізатор, що викликає обробник.

`prefix`

Префікс - рядок, що використовується як посилання на простір імен у межах об'єкта XML.

Якщо як обробник передано порожній рядок або **`false`**, цей обробник вимикається.

> **Зауваження**: Як аргумент замість імені функції може бути переданий масив, що містить посилання на об'єкт та ім'я методу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [xml\_set\_start\_namespace\_decl\_handler()](function.xml-set-start-namespace-decl-handler.html) - Встановлення обробника входу у межі простору імен