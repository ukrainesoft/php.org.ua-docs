---
navigation:
  - ocilob.erase.html: '« OCILob::erase'
  - ocilob.flush.html: 'OCILob::flush »'
  - index.html: PHP Manual
  - class.ocilob.html: OCILob
title: 'OCILob::export'
---
# OCILob::export

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | `offset` і `length` тепер допускають значення null. |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.html) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::import](ocilob.import.html)
