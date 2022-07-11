- [« setcookie](function.setcookie.md)
- [socket_get_status »](function.socket-get-status.md)

- [PHP Manual](index.md)
- [Мережні функції](ref.network.md)
- Надсилає cookie без URL-кодування значення

# setrawcookie

(PHP 5, PHP 7, PHP 8)

setrawcookie — надсилає cookie без URL-кодування значення

### Опис

**setrawcookie**(
string `$name`,
string `$value` = ?,
int `$expires_or_options` = 0,
string `$path` = ?,
string `$domain` = ?,
bool `$secure` = **`false`**,
bool `$httponly` = **`false`**
): bool

Альтернативна сигнатура доступна з PHP 7.3.0 (іменовані параметри не
підтримуються):

**setrawcookie**(string `$name`, string `$value` = ?, array `$options` =
[]): bool

Функція **setrawcookie()** є повним аналогом функції
[setcookie()](function.setcookie.md), за винятком того, що
значення cookie не буде автоматично закодовано під час надсилання
браузеру.

### Список параметрів

Для отримання інформації про параметр, дивіться документацію по функції
[setcookie()](function.setcookie.md).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Список змін

| Версія | Опис                                                                                                                               |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------- |
| 7.3.0  | Доданий альтернативний підпис, що підтримує масив опцій options. Цей підпис також підтримує налаштування cookie-атрибута SameSite. |

### Дивіться також

- [setcookie()](function.setcookie.md) - Надсилає cookie
