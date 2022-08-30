Встановлення оброблювача нерозібраних оголошень сутностей

-   [« xmlsetstartnamespacedeclhandler](function.xml-set-start-namespace-decl-handler.html)
    
-   [XmlParser »](class.xmlparser.md)
    
-   [PHP Manual](index.md)
    
-   [Функции парсера XML](ref.xml.md)
    
-   Встановлення оброблювача нерозібраних оголошень сутностей
    

# xmlsetunparsedentitydeclhandler

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlsetunparsedentitydeclhandler — Встановлення оброблювача нерозібраних оголошень сутностей

### Опис

```methodsynopsis
xml_set_unparsed_entity_decl_handler(XMLParser $parser, callable $handler): bool
```

Задає функцію обробник нерозібраних оголошень для XML-аналізатора `parser`

Обробник `handler` буде викликано, якщо XML-аналізатор виявить NDATA-оголошення зовнішньої сутності вигляду:

name publicId systemId} NDATA notationName

Дивіться [» розділ 4.2.2 XML 1.0 специфікації](http://www.w3.org/TR/1998/REC-xml-19980210#sec-external-ent)щоб отримати точне визначення позначень зовнішніх сутностей.

### Список параметрів

`parser`

Посилання на XML-аналізатор, для якого задається обробник.

`handler`

`handler` - рядок, що містить ім'я функції, який повинен бути визначений на момент виклику функції [xmlparse()](function.xml-parse.html) з аналізатора `parser`

Функція з ім'ям `handler` має приймати шість аргументів:

```methodsynopsis
handler(    XMLParser $parser,    string $entity_name,    string $base,    string $system_id,    string $public_id,    string $notation_name)
```

`parser`

Перший аргумент parser є посиланням на XML-аналізатор, що викликає обробник.

`entity_name`

Ім'я сутності, яку потрібно дати визначення.

`base`

Це основа для дозволу системного ідентифікатора (`system_id`) Зовнішньої сутності. На даний момент як цей аргумент завжди передається порожній рядок.

`system_id`

Системний ідентифікатор зовнішньої сутності

`public_id`

Загальнодоступний ідентифікатор зовнішньої сутності.

`notation_name`

Ім'я позначення цієї сутності (дивіться [xmlsetnotationdeclhandler()](function.xml-set-notation-decl-handler.html)

Якщо як обробник передано порожній рядок або **`false`**, цей обробник вимикається.

> **Зауваження**: Як аргумент замість імені функції може бути переданий масив, що містить посилання на об'єкт та ім'я методу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікували ресурс (resource). |