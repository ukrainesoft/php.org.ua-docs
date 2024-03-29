---
navigation:
  - class.ocilob.md: « OCILob
  - ocilob.close.md: 'OCILob::close »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::append'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCILob::append

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCILob::append — Додає дані з об'єкта LOB до кінця іншого об'єкта

### Опис

```methodsynopsis
public OCILob::append(OCILob $from): bool
```

Додає до кінця об'єкта LOB дані з іншого об'єкта LOB.

Запис в LOB за допомогою цього методу викликає помилку, якщо об'єкт раніше був включений режим буферизації. Тому ви повинні вимкнути буферизацію перед її застосуванням. Перед вимкненням буферизації вам може знадобитися метод [OCILob::flush](ocilob.flush.md)для очистки буфера.

### Список параметрів

`from`

Копіюваний LOB.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Lob**перейменований на[OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::flush](ocilob.flush.md)
-   [OCILob::setBuffering](ocilob.setbuffering.md)
-   [OCILob::getBuffering](ocilob.getbuffering.md)
