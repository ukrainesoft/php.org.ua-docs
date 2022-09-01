---
navigation:
  - xmlwriter.endelement.html: '« XMLWriter::endElement'
  - xmlwriter.flush.html: 'XMLWriter::flush »'
  - index.html: PHP Manual
  - class.xmlwriter.html: XMLWriter
title: 'XMLWriter::endPi'
---
# XMLWriter::endPi

# xmlwriterendпі

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endPi -- xmlwriterendpi — Завершити поточну інструкцію обробки (PI)

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endPi(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_pi(XMLWriter $writer): bool
```

Завершує поточну інструкцію обробки.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::startPi()](xmlwriter.startpi.html) - Створити стартовий тег PI
-   [XMLWriter::writePi()](xmlwriter.writepi.html) - Записати інструкцію обробки (PI)
