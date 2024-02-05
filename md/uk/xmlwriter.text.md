---
navigation:
  - xmlwriter.startpi.md: '« XMLWriter::startPi'
  - xmlwriter.writeattribute.md: 'XMLWriter::writeAttribute »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::text'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::text

# xmlwriter\_text

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::text -- xmlwriter\_text — Записати текст

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::text(string $content): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_text(XMLWriter $writer, string $content): bool
```

Записує текст.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`content`

Вміст тексту. Символи `<` `>` `&`и`"` записуються як посилання на сутність (тобто . `&lt;` `&gt;` `&amp;`и`&quot;`відповідно). Всі інші символи у тому числі `'` записуються буквально. Щоб записувати спеціальні символи XML буквально або записувати буквальні посилання на сутності, необхідно використовувати [xmlwriter\_write\_raw()](xmlwriter.writeraw.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |
