---
navigation:
  - ocilob.erase.md: '« OCILob::erase'
  - ocilob.flush.md: 'OCILob::flush »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::export'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCILob::export

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCILob::export — Зберігає вміст об'єкта LOB у файл

### Опис

```methodsynopsis
public OCILob::export(string $filename, ?int $offset = null, ?int $length = null): bool
```

Зберігає вміст об'єкта LOB у файлі.

### Список параметрів

`filename`

Шлях до файлу.

`offset`

Початкова позиція експорту.

`length`

Довжина експортованої частини LOB.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | `offset`и`length` тепер допускають значення null. |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Lob**перейменований на[OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::import](ocilob.import.md)
