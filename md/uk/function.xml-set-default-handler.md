---
navigation:
  - function.xml-set-character-data-handler.md: « xmlsetcharacterdatahandler
  - function.xml-set-element-handler.md: xmlsetelementhandler »
  - index.md: PHP Manual
  - ref.xml.md: Функции парсера XML
title: xmlsetdefaulthandler
---
# xmlsetdefaulthandler

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlsetdefaulthandler — Налаштування оброблювача за замовчуванням

### Опис

```methodsynopsis
xml_set_default_handler(XMLParser $parser, callable $handler): bool
```

Задає стандартний обробник для XML-аналізатора `parser`

### Список параметрів

`parser`

Посилання на аналізатор XML.

`handler`

`handler` - рядок, що містить ім'я функції, який повинен бути визначений на момент виклику функції [xmlparse()](function.xml-parse.md) з аналізатора `parser`

Функція з ім'ям `handler` має приймати два аргументи:

```methodsynopsis
handler(XmlParser $parser, string $data)
```

`parser`

Перший аргумент parser є посиланням на XML-аналізатор, що викликає обробник.

`data`

Другий аргумент `data`має містити символьні дані. Це може бути XML-оголошення, оголошення типу документа, сутності чи інші дані, котрим ще немає оброблювача.

Якщо як обробник передано порожній рядок або **`false`**, цей обробник вимикається.

> **Зауваження**: Як аргумент замість імені функції може бути переданий масив, що містить посилання на об'єкт та ім'я методу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікували ресурс (resource). |
