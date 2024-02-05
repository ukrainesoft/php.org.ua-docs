---
navigation:
  - ocilob.savefile.md: '« OCILob::saveFile'
  - ocilob.setbuffering.md: 'OCILob::setBuffering »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::seek'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCILob::seek

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCILob::seek — Встановлює позицію внутрішнього покажчика LOB

### Опис

```methodsynopsis
public OCILob::seek(int $offset, int $whence = OCI_SEEK_SET): bool
```

Встановлює позицію внутрішнього покажчика об'єкта LOB.

### Список параметрів

`offset`

Вказує кількість байтів, на які слід переміститися від позиції, яка визначається параметром `whence` :

`whence`

Може бути одним із значень:

-   \*\*`OCI_SEEK_SET`\*\*- встановити позицію, рівну`offset`
-   \*\*`OCI_SEEK_CUR`\*\*- додати до поточної позиції`offset`байт
-   \*\*`OCI_SEEK_END`\*\*- додати до кінця файлу`offset`байт (щоб перемістити покажчик на початок - вкажіть негативний`offset`) .

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Lob**перейменований на[OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::rewind](ocilob.rewind.md)
-   [OCILob::tell](ocilob.tell.md)
-   [OCILob::eof](ocilob.eof.md)
