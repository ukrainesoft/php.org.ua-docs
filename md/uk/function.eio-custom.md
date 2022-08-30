Виконує запит користувача як будь-який інший eio виклик

-   [« eioclose](function.eio-close.html)
    
-   [eiodup2 »](function.eio-dup2.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
-   Виконує запит користувача як будь-який інший eio виклик
    

# eiocustom

(PECL eio >= 0.0.1dev)

eiocustom — Виконує запит користувача як будь-який інший *eio* виклик

### Опис

```methodsynopsis
eio_custom(    callable $execute,    int $pri,    callable $callback,    mixed $data = NULL): resource
```

**eiocustom()** виконує функцію користувача, визначену в параметрі `execute` як будь-який інший виклик запитів *eio*

### Список параметрів

`execute`

Вказується функція, що відповідає нижченаведеному прототипу:

```
mixed execute(mixed data);
```

Параметр `callback` містить callback-функцію, що виконується після завершення виконання запиту. Функція повинна відповідати прототипу:

```
void callback(mixed data, mixed result);
```

`data` - дані, що передаються у функцію, зазначену в `execute` через аргумент `data`, без будь-яких змін . `result` - значення, яке повертається функцією у параметрі `execute`

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

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eiogetlasterror()](function.eio-get-last-error.html)

`data`

Довільна змінна, що передається в `callback`функцію.

### Значення, що повертаються

**eiocustom()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **eiocustom()****

```php
<?php
/* Пользовательская callback-функция */
function my_custom_callback($data, $result) {
    var_dump($data);
    var_dump(count($result));
    var_dump($result['data_modified']);
    var_dump($result['result']);
}

/* Пользовательский запрос */
function my_custom($data) {
    var_dump($data);

    $result  = array(
        'result'        => 1001,
        'data_modified' => "my custom data",
    );

    return $result;
}

$data = "my_custom_data";
$req = eio_custom("my_custom", EIO_PRI_DEFAULT, "my_custom_callback", $data);
var_dump($req);
eio_event_loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
resource(4) of type (EIO Request Descriptor)
string(14) "my_custom_data"
string(14) "my_custom_data"
int(2)
string(14) "my custom data"
int(1001)
```