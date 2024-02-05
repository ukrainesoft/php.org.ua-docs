---
navigation:
  - ocilob.truncate.md: '« OCILob::truncate'
  - ocilob.writetemporary.md: 'OCILob::writeTemporary »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::write'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCILob::write

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCILob::write — Записує дані в об'єкт LOB

### Опис

```methodsynopsis
public OCILob::write(string $data, ?int $length = null): int|false
```

Записує дані з параметра `data` у поточну позицію внутрішнього покажчика об'єкта.

### Список параметрів

`data`

Дані, що записуються в LOB.

`length`

Якщо параметр є числом, запис зупиниться після того, як `length` байт буде записано або закінчаться дані з параметра `data`

### Значення, що повертаються

Повертає кількість записаних байт або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | `length` тепер допускає значення null. |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Lob**перейменований на[OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::read](ocilob.read.md)
