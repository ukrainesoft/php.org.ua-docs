Встановлення обробника входу в межі простору імен

-   [« xml\_set\_processing\_instruction\_handler](function.xml-set-processing-instruction-handler.html)
    
-   [xml\_set\_unparsed\_entity\_decl\_handler »](function.xml-set-unparsed-entity-decl-handler.html)
    
-   [PHP Manual](index.html)
    
-   [Функции парсера XML](ref.xml.html)
    
-   Встановлення обробника входу в межі простору імен
    

# xmlsetstartnamespacedeclhandler

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

xmlsetstartnamespacedeclhandler - Встановлення обробника входу в межі простору імен

### Опис

```methodsynopsis
xml_set_start_namespace_decl_handler(XMLParser $parser, callable $handler): bool
```

Задає обробник події входу до простору імен. Тобто обробник викликається аналізатор знаходить оголошення простору імен. Подібні оголошення знаходяться у елементах, що відкривають тегах. Цей оброблювач викликається до оброблювача початку тега.

### Список параметрів

`parser`

Посилання на аналізатор XML.

`handler`

`handler` - рядок, що містить ім'я функції, яка повинна бути визначена на момент виклику функції [xml\_parse()](function.xml-parse.html) з аналізатора `parser`

Функція з ім'ям `handler` повинна приймати три аргументи та повертати цілий результат. Якщо обробник поверне **`false`** (як і нічого не поверне), XML-аналізатор припинить роботу, а функція [xml\_get\_error\_code()](function.xml-get-error-code.html) повертатиме константу **`XML_ERROR_EXTERNAL_ENTITY_HANDLING`**

```methodsynopsis
handler(XMLParser $parser, string $prefix, string $uri)
```

`parser`

Перший аргумент parser є посиланням на XML-аналізатор, що викликає обробник.

`prefix`

Префікс - рядок, що використовується як посилання на простір імен у межах об'єкта XML.

`uri`

Універсальний ідентифікатор ресурсу (URI) простір імен.

Якщо як обробник передано порожній рядок або **`false`**, цей обробник вимикається.

> **Зауваження**: Як аргумент замість імені функції може бути переданий масив, що містить посилання на об'єкт та ім'я методу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                     |
|--------|--------------------------------------------------------------------------------------------------------------|
|        | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [xml\_set\_end\_namespace\_decl\_handler()](function.xml-set-end-namespace-decl-handler.html) - встановлення обробника виходу за межі простору імен