---
navigation:
  - function.eio-close.md: « eio\_close
  - function.eio-dup2.md: eio\_dup2 »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_custom
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_custom

(PECL eio >= 0.0.1dev)

eio\_custom — Виконує запит користувача як будь-який інший *eio\_\** виклик

### Опис

```methodsynopsis
eio_custom(    callable $execute,    int $pri,    callable $callback,    mixed $data = NULL): resource
```

**eio\_custom()** виконує функцію користувача, визначену в параметрі `execute` як будь-який інший виклик запитів *eio\_\**

### Список параметрів

`execute`

Вказується функція, що відповідає нижченаведеному прототипу:

```
mixed execute(mixed data);
```

Параметр`callback` містить callback-функцію, що виконується після завершення виконання запиту. Функція повинна відповідати прототипу:

```
void callback(mixed data, mixed result);
```

`data` - дані, що передаються у функцію, зазначену в `execute`через аргумент`data`, без будь-яких змін . `result` - значення, яке повертається функцією у параметрі `execute`

`pri`

Пріоритет запитів: **`EIO_PRI_DEFAULT`** **`EIO_PRI_MIN`** **`EIO_PRI_MAX`**, или\*\*`null`**. Якщо передано **`null`**, то`pri`устанавливается в**`EIO_PRI_DEFAULT`\*\*

`callback`

Функция`callback` викликається після завершення запиту. Вона повинна задовольняти наступний прототип:

```php
void callback(mixed $data, int $result[, resource $req]);
```

`data`

є даними користувача, переданими в запиті.

`result`

містить результуюче значення, що залежить від запиту; зазвичай це значення, яке повертається відповідним системним викликом.

`req`

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eio\_get\_last\_error()](function.eio-get-last-error.md)

`data`

Произвольная переменная, передаваемая в`callback`\-функцію.

### Значення, що повертаються

**eio\_custom()** повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**eio\_custom()\*\*\*\*

```php
<?php
/* Пользовательская callback-функция */
function my_custom_callback($data, $result) {
    var_dump($data);
    var_dump(count($result));
    var_dump($result['data_modified']);
    var_dump($result['result']);
}

/* Пользовательский запрос */
function my_custom($data) {
    var_dump($data);

    $result  = array(
        'result'        => 1001,
        'data_modified' => "my custom data",
    );

    return $result;
}

$data = "my_custom_data";
$req = eio_custom("my_custom", EIO_PRI_DEFAULT, "my_custom_callback", $data);
var_dump($req);
eio_event_loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
resource(4) of type (EIO Request Descriptor)
string(14) "my_custom_data"
string(14) "my_custom_data"
int(2)
string(14) "my custom data"
int(1001)
```
