- [« OCILob::export](ocilob.export.md)
- [OCILob::free »](ocilob.free.md)

- [PHP Manual](index.md)
- [OCILob](class.ocilob.md)
- Очищає та записує буфер об'єкта LOB на сервер

# OCILob::flush

(PHP 5, PHP 7, PHP 8, PECL OCI8 \>= 1.1.0)

OCILob::flush — Очищає та записує буфер об'єкта LOB на сервер

### Опис

public **OCILob::flush**(int `$flag` = 0): bool

**OCILob::flush()** безпосередньо записує дані на сервер.

### Список параметрів

`flag`
За замовчуванням ресурси не звільняються, але використовуючи прапор
**`OCI_LOB_BUFFER_FREE`** ви можете зробити це примусово. Проте,
ви повинні бути точно впевнені в тому, що ви робите, тому що наступне
читання з об'єкта буде більш ресурсоємним, ніж попередні через
необхідності звернення до сервера. Тому використати прапор
**`OCI_LOB_BUFFER_FREE`** рекомендується тільки після того, як робота з
об'єктом вже закінчено.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

Повертає **`false`** у разі виникнення помилки або якщо
буферизація об'єкта була включена.

### Список змін

| Версія                 | Опис                                                                                                  |
|------------------------|-------------------------------------------------------------------------------------------------------|
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

- [OCILob::getBuffering](ocilob.getbuffering.md)
- [OCILob::setBuffering](ocilob.setbuffering.md)
