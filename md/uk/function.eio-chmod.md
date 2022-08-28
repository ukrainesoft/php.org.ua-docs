Змінює права доступу до файлу/директорії

-   [« eio\_cancel](function.eio-cancel.html)
    
-   [eio\_chown »](function.eio-chown.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
-   Змінює права доступу до файлу/директорії
    

# eiochmod

(PECL eio >= 0.0.1dev)

eiochmod — Змінює права доступу до файлу/директорії

### Опис

```methodsynopsis
eio_chmod(    string $path,    int $mode,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eiochmod()** змінює права доступу до файлу/директорії. Нові права доступу вказуються у параметрі `mode`

### Список параметрів

`path`

Шлях до файлу чи директорії

**Увага**

Уникайте відносних шляхів

`mode`

Нові права доступу Наприклад, **`0644`**

`pri`

Пріоритет запитів: **`EIO_PRI_DEFAULT`** **`EIO_PRI_MIN`** **`EIO_PRI_MAX`**, або **`null`**. Якщо передано **`null`**, то `pri` встановлюється в **`EIO_PRI_DEFAULT`**

`callback`

Функція `callback` викликається після завершення запиту. Вона повинна задовольняти наступний прототип:

```php
void callback(mixed $data, int $result[, resource $req]);
```

`data`

є даними користувача, переданими в запиті.

`result`

містить результуюче значення, що залежить від запиту; зазвичай це значення, яке повертається відповідним системним викликом.

`req`

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eio\_get\_last\_error()](function.eio-get-last-error.html)

`data`

Довільна змінна, що передається в `callback`функцію.

### Значення, що повертаються

**eiochmod()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [eio\_chown()](function.eio-chown.html) - Змінює права доступу до файлу/директорії