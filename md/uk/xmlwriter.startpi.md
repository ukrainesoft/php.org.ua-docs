---
navigation:
  - xmlwriter.startelementns.md: '« XMLWriter::startElementNs'
  - xmlwriter.text.md: 'XMLWriter::text »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startPi'
---
# XMLWriter::startPi

# xmlwriterstartпі

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startPi -- xmlwriterstartpi — Створити стартовий тег PI

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`target`

Ціль інструкції обробки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::endPi()](xmlwriter.endpi.md) - Закінчити поточну інструкцію обробки (PI)
-   [XMLWriter::writePi()](xmlwriter.writepi.md) - Записати інструкцію обробки (PI)
