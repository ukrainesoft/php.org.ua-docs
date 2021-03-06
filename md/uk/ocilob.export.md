- [« OCILob::erase](ocilob.erase.md)
- [OCILob::flush »](ocilob.flush.md)

- [PHP Manual](index.md)
- [OCILob](class.ocilob.md)
- Зберігає вміст об'єкта LOB у файл

# OCILob::export

(PHP 5, PHP 7, PHP 8, PECL OCI8 \>= 1.1.0)

OCILob::export — Зберігає вміст об'єкта LOB у файл

### Опис

public **OCILob::export**(string `$filename`, ?int `$offset` =
**`null`**, ?int `$length` = **`null`**): bool

Зберігає вміст об'єкта LOB у файлі.

### Список параметрів

`filename`
Шлях до файлу.

`offset`
Початкова позиція експорту.

`length`
Довжина експортованої частини LOB.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Список змін

| Версія                 | Опис                                                                                                  |
|------------------------|-------------------------------------------------------------------------------------------------------|
| 8.0.0, PECL OCI8 3.0.0 | offset та length тепер допускають значення null.                                                      |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

- [OCILob::import](ocilob.import.md)
