---
navigation:
  - function.xml-parser-set-option.html: « xmlparsersetoption
  - function.xml-set-default-handler.html: xmlsetdefaulthandler »
  - index.html: PHP Manual
  - ref.xml.html: Функции парсера XML
title: xmlsetcharacterdatahandler
---
# xmlsetcharacterdatahandler

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlsetcharacterdatahandler — Встановлення обробника символьних даних

### Опис

```methodsynopsis
xml_set_character_data_handler(XMLParser $parser, callable $handler): bool
```

Встановлює обробник символьних даних для заданого XML-аналізатора `parser`

### Список параметрів

`parser`

Посилання на аналізатор XML.

`handler`

`handler` - рядок, що містить ім'я функції, який повинен бути визначений на момент виклику функції [xmlparse()](function.xml-parse.html) з аналізатора `parser`

Функція з ім'ям `handler` має приймати два аргументи:

```methodsynopsis
handler(XmlParser $parser, string $data)
```

`parser`

Перший аргумент parser є посиланням на XML-аналізатор, що викликає обробник.

`data`

Другий аргумент `data` повинен містити дані у вигляді текстового рядка.

Обробник символьних даних викликається кожного фрагмента тексту в XML-документі. Він також може викликатися кілька разів усередині кожного фрагмента (наприклад, для не ASCII-рядків).

Якщо як обробник передано порожній рядок або **`false`**, цей обробник вимикається.

> **Зауваження**: Як аргумент замість імені функції може бути переданий масив, що містить посилання на об'єкт та ім'я методу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.html); раніше очікували ресурс (resource). |
