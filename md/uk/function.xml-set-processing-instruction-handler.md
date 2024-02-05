---
navigation:
  - function.xml-set-object.md: « xml\_set\_object
  - function.xml-set-start-namespace-decl-handler.md: xml\_set\_start\_namespace\_decl\_handler »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_set\_processing\_instruction\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_set\_processing\_instruction\_handler

(PHP 4, PHP 5, PHP 7, PHP 8)

xml\_set\_processing\_instruction\_handler - Встановлення обробника інструкцій препроцесора (PI)

### Опис

```methodsynopsis
xml_set_processing_instruction_handler(XMLParser $parser, callable $handler): true
```

Задає обробник інструкцій препроцесора (PI) для XML-аналізатора . `parser`

Інструкції мають такий формат:

**Застереження**

PHP-код розмежовується інструкцією обробки `<?php`. Таким чином, у XML-документі можна розташовувати PHP-код. Однак кінцевий тег PI (`?>`) не повинен бути частиною даних. Якщо завершальний тег PI є частиною вбудованого PHP-коду, то решта PHP-коду та "справжній" тег PI end будуть розглядатися як символьні дані.

### Список параметрів

`parser`

Парсер XML.

`handler`

Якщо передається значення **`null`** або порожній рядок, обробник повертається в стан за замовчуванням.

Якщо параметр `handler` є типом [callable](language.types.callable.md), то як оброблювач встановлюється callable.

Якщо параметр `handler` є рядком (string), це може бути ім'я методу об'єкта, заданого за допомогою функції [xml\_set\_object()](function.xml-set-object.md)

Сигнатура оброблювача має бути:

```methodsynopsis
handler(XMLParser $parser, string $target, string $data): void
```

`parser`

XML-парсер, що викликає оброблювач.

`target`

Ціль застосування PI.

`data`

PI-дані.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався коректний `xml` ресурс (Resource). |
