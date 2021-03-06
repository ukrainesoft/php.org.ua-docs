- [«eio_chmod](function.eio-chmod.md)
- [eio_close »](function.eio-close.md)

- [PHP Manual](index.md)
- [Eio Функції](ref.eio.md)
- Змінює права доступу до файлу/директорії

#eio_chown

(PECL eio \>= 0.0.1dev)

eio_chown — Зміна прав доступу до файлу/директорії

### Опис

**eio_chown**(
string `$path`,
int `$uid`,
int `$gid` = -1,
int `$pri` = EIO_PRI_DEFAULT,
[callable](language.types.callable.md) `$callback` = NULL,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
$data = NULL
): resource

Змінює права доступу до файлу/директорії.

### Список параметрів

`path`
Шлях до файлу чи директорії.

**Увага**
Уникайте відносних шляхів

`uid`
Код користувача. Ігнорується при значенні, що дорівнює -1.

`gid`
Код групи. Ігнорується при значенні, що дорівнює -1.

`pri`
Пріоритет запитів: **`EIO_PRI_DEFAULT`**, **`EIO_PRI_MIN`**,
**`EIO_PRI_MAX`**, або **`null`**. Якщо переданий **`null`**, то `pri`
встановлюється у **`EIO_PRI_DEFAULT`**.

`callback`
Функція callback викликається при завершенні запиту. Вона повинна
задовольняти наступний прототип:

` void callback(mixed $data, int $result[, resource $req]);'

`data`
є даними користувача, переданими в запиті.

`result`
містить результуюче значення, що залежить від запиту; зазвичай це
значення, яке повертається відповідним системним викликом.

`req`
є опціональним запитуваним ресурсом, який може
використовуватися з такими функціями як
[eio_get_last_error()](function.eio-get-last-error.md)

`data`
Довільна змінна, що передається в `callback`-функцію.

### Значення, що повертаються

**eio_chown()** повертає вказівник на запит у разі успішного
виконання або **`false`** у разі виникнення помилки.

### Дивіться також

- [eio_chmod()](function.eio-chmod.md) - Змінює права доступу до
файлу/директорії
