- [« XMLWriter::startDtd](xmlwriter.startdtd.md)
- [XMLWriter::startDtdElement »](xmlwriter.startdtdelement.md)

- [PHP Manual](index.md)
- [XMLWriter](class.xmlwriter.md)
- Створює стартовий перелік атрибутів DTD

# XMLWriter::startDtdAttlist

#xmlwriter_start_dtd_attlist

(PHP 5 = 5.1.2, PHP 7, PHP 8, PECL xmlwriter = 0.1.0)

XMLWriter::startDtdAttlist -- xmlwriter_start_dtd_attlist — Створює
стартовий список атрибутів DTD

### Опис

Об'єктно-орієнтований стиль

public **XMLWriter::startDtdAttlist**(string `$name`): bool

Процедурний стиль

**xmlwriter_start_dtd_attlist**([XMLWriter](class.xmlwriter.md)
`$writer`, string `$name`): bool

Починає перелік атрибутів DTD.

### Список параметрів

`writer`
Тільки для процедурних дзвінків. Змінний екземпляр
[XMLWriter](class.xmlwriter.md). Об'єкт повертається із виклику
[xmlwriter_open_uri()](xmlwriter.openuri.md) або
[xmlwriter_open_memory()](xmlwriter.openmemory.md).

`name`
Назва списку атрибутів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Список змін

| Версія | Опис                                                                                                               |
| ------ | ------------------------------------------------------------------------------------------------------------------ |
| 8.0.0  | У параметрі writer тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

- [XMLWriter::endDtdAttlist()](xmlwriter.enddtdattlist.md) -
Завершити поточний список атрибутів DTD
- [XMLWriter::writeDtdAttlist()](xmlwriter.writedtdattlist.md) -
Записати повний тег DTD AttList
