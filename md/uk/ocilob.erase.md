---
navigation:
  - ocilob.eof.html: '« OCILob::eof'
  - ocilob.export.html: 'OCILob::export »'
  - index.html: PHP Manual
  - class.ocilob.html: OCILob
title: 'OCILob::erase'
---
# OCILob::erase

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCILob::erase — Очищає вказану частину об'єкта LOB

### Опис

```methodsynopsis
public OCILob::erase(?int $offset = null, ?int $length = null): int|false
```

Очищає конкретну частину об'єкта LOB, починаючи з позиції, визначеної у параметрі `offset`. За промовчанням LOB повністю очищається.

Для об'єктів типу BLOB очищення означає заповнення нульовими байтами. Об'єкти типу CLOB заповнюються пробілами.

### Список параметрів

`offset`

`length`

### Значення, що повертаються

Повертає кількість очищених символів/байт або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | `offset` і `length` тепер допускають значення null. |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.html) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::truncate](ocilob.truncate.html)
