---
navigation:
  - xmlwriter.writeelementns.md: '« XMLWriter::writeElementNs'
  - xmlwriter.writeraw.md: 'XMLWriter::writeRaw »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::writePi'
---
# XMLWriter::writePi

# xmlwriterwriteпі

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writePi -- xmlwriterwritepi — Записати інструкцію обробки (PI)

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writePi(string $target, string $content): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_pi(XMLWriter $writer, string $target, string $content): bool
```

Записує інструкцію обробки.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`target`

Ціль інструкції обробки.

`content`

Вміст інструкції обробки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::startPi()](xmlwriter.startpi.md) - Створити стартовий тег PI
-   [XMLWriter::endPi()](xmlwriter.endpi.md) - Закінчити поточну інструкцію обробки (PI)
