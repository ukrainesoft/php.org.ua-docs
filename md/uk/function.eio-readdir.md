---
navigation:
  - function.eio-readahead.md: « eio\_readahead
  - function.eio-readlink.md: eio\_readlink »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_readdir
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_readdir

(PECL eio >= 0.0.1dev)

eio\_readdir - Читає вміст директорії

### Опис

```methodsynopsis
eio_readdir(    string $path,    int $flags,    int $pri,    callable $callback,    string $data = NULL): resource
```

Читає вміст директорії (за допомогою системних викликів `opendir` `readdir`и`closedir`) і або повертає імена файлів, або передає масив як аргумент `result` у функцію `callback`Поведение метода зависит от значения параметра`flags`

### Список параметрів

`path`

Шлях до директорії.

`flags`

Комбінація констант *EIO\_READDIR\_\**

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

Дані, які потрібно передати функції `callback`

### Значення, що повертаються

**eio\_readdir()** повертає ресурс запиту у разі успішного виконання або **`false`** у разі виникнення помилки. Також може ставити значення аргументу `result` функції `callback`в зависимости от значения параметра`flags` :

**`EIO_READDIR_DENTS`**(int)

Флаг**eio\_readdir()**. Якщо заданий, як аргумент callback-функції передаватиметься масив з такими ключами: `'names'` - масив імен директорії `'dents'` - масив структур типу `struct eio_dirent`, кожна з яких є масивом з ключами: `'name'` - Ім'я директорії; `'type'`\- одна из констант*EIO\_DT\_\** `'inode'`\- номер узла inode, если доступен, либо пустое значение;

**`EIO_READDIR_DIRS_FIRST`**(int)

Якщо цей прапор задано, першими повертатимуться імена директорій, потім імена файлів. Порядок проходження імен у кожній групі буде оптимальним для застосування функції stat.

**`EIO_READDIR_STAT_ORDER`**(int)

Якщо цей прапор задано, імена файлів та директорій повертатимуться в порядку, зручному для збору статистики (`stat`) кожного з об'єктів. Якщо отриманий список імен передбачається передавати у функцію [stat()](function.stat.md), порядок проходження імен забезпечить найшвидшу роботу функції.

**`EIO_READDIR_FOUND_UNKNOWN`**(int)

Типи вузлів:

**`EIO_DT_UNKNOWN`**(int)

Невідомий тип вузла (дуже часто). Необхідна обробка функцією [stat()](function.stat.md)

**`EIO_DT_FIFO`**(int)

Тип вузла - FIFO

**`EIO_DT_CHR`**(int)

Тип вузла

**`EIO_DT_MPC`**(int)

Тип вузла - складовий символьний пристрій (v7+coherent)

**`EIO_DT_DIR`**(int)

Тип вузла - директорія

**`EIO_DT_NAM`**(int)

Тип вузла - файл зі спеціальним Xenix найменуванням

**`EIO_DT_BLK`**(int)

Тип вузла

**`EIO_DT_MPB`**(int)

Складовий блоковий пристрій (v7+coherent)

**`EIO_DT_REG`**(int)

Тип вузла

**`EIO_DT_NWK`**(int)

**`EIO_DT_CMP`**(int)

Спеціальний тип вузла для мереж HP-UX

**`EIO_DT_LNK`**(int)

Тип вузла - посилання

**`EIO_DT_SOCK`**(int)

Тип вузла - сокет

**`EIO_DT_DOOR`**(int)

Тип вузла - Solaris door

**`EIO_DT_WHT`**(int)

Тип вузла

**`EIO_DT_MAX`**(int)

Максимальне значення типу вузла

### Приклади

**Пример #1 Пример использования**eio\_readdir()\*\*\*\*

```php
<?php
/* Вызывается, когда отработает eio_readdir() */
function my_readdir_callback($data, $result) {
    echo "Вызвана функция ", __FUNCTION__, "\n";
    echo "данные: "; var_dump($data);
    echo "результат: "; var_dump($result);
    echo "\n";
}

eio_readdir("/var/spool/news", EIO_READDIR_STAT_ORDER | EIO_READDIR_DIRS_FIRST,
  EIO_PRI_DEFAULT, "my_readdir_callback");
eio_event_loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
Вызвана функция my_readdir_callback
данные: NULL
результат: array(2) {
 ["names"]=>
  array(7) {
   [0]=>
    string(7) "archive"
    [1]=>
    string(8) "articles"
    [2]=>
    string(8) "incoming"
    [3]=>
    string(7) "innfeed"
    [4]=>
    string(8) "outgoing"
    [5]=>
    string(8) "overview"
    [6]=>
    string(3) "tmp"
  }
 ["dents"]=>
  array(7) {
   [0]=>
    array(3)
    {
     ["name"]=>
      string(7)
      "archive"
      ["type"]=>
      int(4)
      ["inode"]=>
      int(393265)
    }
   [1]=>
    array(3)
    {
     ["name"]=>
      string(8)
      "articles"
      ["type"]=>
      int(4)
      ["inode"]=>
      int(393266)
    }
   [2]=>
    array(3)
    {
     ["name"]=>
      string(8)
      "incoming"
      ["type"]=>
      int(4)
      ["inode"]=>
      int(393267)
    }
   [3]=>
    array(3)
    {
     ["name"]=>
      string(7)
      "innfeed"
      ["type"]=>
      int(4)
      ["inode"]=>
      int(393269)
    }
   [4]=>
    array(3)
    {
     ["name"]=>
      string(8)
      "outgoing"
      ["type"]=>
      int(4)
      ["inode"]=>
      int(393270)
    }
   [5]=>
    array(3)
    {
     ["name"]=>
      string(8)
      "overview"
      ["type"]=>
      int(4)
      ["inode"]=>
      int(393271)
    }
   [6]=>
    array(3)
    {
     ["name"]=>
      string(3)
      "tmp"
      ["type"]=>
      int(4)
      ["inode"]=>
      int(393272)
    }
  }
}
```
