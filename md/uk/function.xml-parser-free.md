---
navigation:
  - function.xml-parser-create.md: « xmlparsercreate
  - function.xml-parser-get-option.md: xmlparsergetoption »
  - index.md: PHP Manual
  - ref.xml.md: Функции парсера XML
title: xmlparserfree
---
# xmlparserfree

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlparserfree — Звільнення XML-аналізатора

### Опис

```methodsynopsis
xml_parser_free(XMLParser $parser): bool
```

> **Зауваження**
> 
> Використання функції не має сенсу. До PHP 8.0.0 вона використовувалася для закриття ресурсу.

Звільняє пам'ять, зайняту XML-аналізатором `parser`

**Застереження**

До PHP 8.0.0, на додаток до виклику \*\*xmlparserfree()\*\*Після закінчення розбирання необхідно також явно видалити (unset) посилання на `parser` щоб уникнути витоку пам'яті, якщо ресурс парсеру посилається на об'єкт, а цей об'єкт посилається на ресурс парсера.

### Список параметрів

`parser`

Посилання на XML-аналізатор, що видаляється.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався ресурс (resource). |
