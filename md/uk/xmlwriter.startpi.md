---
navigation:
  - xmlwriter.startelementns.md: '« XMLWriter::startElementNs'
  - xmlwriter.text.md: 'XMLWriter::text »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startPi'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::startPi

# xmlwriter\_start\_pi

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startPi -- xmlwriter\_start\_pi — Створити стартовий тег PI

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startPi(string $target): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_pi(XMLWriter $writer, string $target): bool
```

Починає тег інструкції з обробки (PI).

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`target`

Ціль інструкції обробки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endPi()](xmlwriter.endpi.md) \- Закінчити поточну інструкцію обробки (PI)
-   [XMLWriter::writePi()](xmlwriter.writepi.md) \- Записати інструкцію обробки (PI)
