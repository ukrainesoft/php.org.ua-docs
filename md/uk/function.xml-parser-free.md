---
navigation:
  - function.xml-parser-create.md: « xml\_parser\_create
  - function.xml-parser-get-option.md: xml\_parser\_get\_option »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_parser\_free
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_parser\_free

(PHP 4, PHP 5, PHP 7, PHP 8)

xml\_parser\_free — Звільнення XML-аналізатора

### Опис

```methodsynopsis
xml_parser_free(XMLParser $parser): bool
```

> **Зауваження** :
> 
> Використання функції не має сенсу. До PHP 8.0.0 вона використовувалася для закриття ресурсу.

Звільняє пам'ять, зайняту XML-аналізатором `parser`

**Застереження**

До PHP 8.0.0, на додаток до виклику \*\*xml\_parser\_free()\*\*Після закінчення розбирання необхідно також явно видалити (unset) посилання на `parser` щоб уникнути витоку пам'яті, якщо ресурс парсеру посилається на об'єкт, а цей об'єкт посилається на ресурс парсера.

### Список параметрів

`parser`

Посилання на XML-аналізатор, що видаляється.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався коректний `xml` ресурс (Resource). |
