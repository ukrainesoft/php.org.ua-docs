---
navigation:
  - xmlwriter.endelement.md: '« XMLWriter::endElement'
  - xmlwriter.flush.md: 'XMLWriter::flush »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::startPi()](xmlwriter.startpi.md) - Створити стартовий тег PI
-   [XMLWriter::writePi()](xmlwriter.writepi.md) - Записати інструкцію обробки (PI)
