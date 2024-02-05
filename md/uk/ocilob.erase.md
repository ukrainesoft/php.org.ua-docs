---
navigation:
  - ocilob.eof.md: '« OCILob::eof'
  - ocilob.export.md: 'OCILob::export »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::erase'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCILob::erase

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCILob::erase — Очищає вказану частину об'єкта LOB

### Опис

```methodsynopsis
public OCILob::erase(?int $offset = null, ?int $length = null): int|false
```

Очищає конкретну частину об'єкта LOB, починаючи з позиції, визначеної у параметрі `offset`По умолчанию LOB очищается полностью.

Для об'єктів типу BLOB очищення означає заповнення нульовими байтами. Об'єкти типу CLOB заповнюються пробілами.

### Список параметрів

`offset`

`length`

### Значення, що повертаються

Повертає кількість очищених символів/байт або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | `offset`и`length` тепер допускають значення null. |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Lob**перейменований на[OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::truncate](ocilob.truncate.md)
