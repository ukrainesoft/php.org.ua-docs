---
navigation:
  - ocilob.seek.md: '« OCILob::seek'
  - ocilob.size.md: 'OCILob::size »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::setBuffering'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCILob::setBuffering

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCILob::setBuffering — Змінює поточний стан буферизації великого об'єкта (LOB)

### Опис

```methodsynopsis
public OCILob::setBuffering(bool $mode): bool
```

Встановлює буферизацію для великого об'єкта, виходячи зі значення параметра `mode`

Використання цієї функції може призвести до покращення продуктивності шляхом буферизації дрібних операцій читання та запису в LOB за рахунок зменшення кількості мережевих звернень та версій LOB. Необхідно обов'язково використовувати [OCILob::flush()](ocilob.flush.md)после завершения всех работ с LOB.

### Список параметрів

`mode`

\*\*`true`**для включения и**`false`\*\*для отключения.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Повторні виклики цього методу з тим самим прапором буде повертати **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Lob**перейменований на[OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::getBuffering](ocilob.getbuffering.md)
