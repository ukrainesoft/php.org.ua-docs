---
navigation:
  - function.eio-mkdir.md: « eio\_mkdir
  - function.eio-nop.md: eio\_nop »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_mknod
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_mknod

(PECL eio >= 0.0.1dev)

eio\_mknod — Створює спеціальний або звичайний файл

### Опис

```methodsynopsis
eio_mknod(    string $path,    int $mode,    int $dev,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eio\_mknod()** створює звичайний чи спеціальний (що частіше) файл.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`path`

Шлях до нового файлу.

`mode`

Задає роздільну здатність файлу та його тип. Значенням аргументу є комбінація (використовуючи побітове АБО) однієї або декількох констант, що відповідають за тип файлу, та числа, що відповідає за дозволи для файлу (наприклад, 0640). Константи типів файлів: **`EIO_S_IFREG`**(звичайний файл), **`EIO_S_IFCHR`**(символьний файл), **`EIO_S_IFBLK`**(спеціальний блоковий файл), **`EIO_S_IFIFO`**(FIFO - іменований пайп) та **`EIO_S_IFSOCK`**(UNIX сокет домену). Для встановлення дозволів необхідно використовувати константи *EIO\_S\_I\**

`dev`

При создании файла типа\*\*`EIO_S_IFCHR`**или**`EIO_S_IFBLK`\*\*, параметр dev задає верхню та нижню межі нумерації спеціальних файлів пристроїв. При створенні інших типів файлів `dev` ігнорується. За додатковими поясненнями звертайтесь до *сторінці документації mknod(2)*

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

Дані, які потрібно передати в `callback`\-функцію.

### Значення, що повертаються

**eio\_mknod()** повертає ресурс запиту у разі успішного виконання операції або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**eio\_mknod()\*\*\*\*

```php
<?php
// имя FIFO
$temp_filename = "/tmp/eio-temp-fifo";

/* будет вызываться по завершении работы функции eio_mknod() */
function my_mknod_callback($data, $result) {
    $s = stat($data);
    var_dump($s);

    if ($result == 0) {
        echo "eio_mknod_ok";
    }

    @unlink($data);
}

eio_mknod($temp_filename, EIO_S_IFIFO, 0,
    EIO_PRI_DEFAULT, "my_mknod_callback", $temp_filename);
eio_event_loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(26) {
  [0]=>
  int(17)
  [1]=>
  int(2337608)
  [2]=>
  int(4096)
  [3]=>
  int(1)
  [4]=>
  int(1000)
  [5]=>
  int(100)
  [6]=>
  int(0)
  [7]=>
  int(0)
  [8]=>
  int(1318241261)
  [9]=>
  int(1318241261)
  [10]=>
  int(1318241261)
  [11]=>
  int(4096)
  [12]=>
  int(0)
  ["dev"]=>
  int(17)
  ["ino"]=>
  int(2337608)
  ["mode"]=>
  int(4096)
  ["nlink"]=>
  int(1)
  ["uid"]=>
  int(1000)
  ["gid"]=>
  int(100)
  ["rdev"]=>
  int(0)
  ["size"]=>
  int(0)
  ["atime"]=>
  int(1318241261)
  ["mtime"]=>
  int(1318241261)
  ["ctime"]=>
  int(1318241261)
  ["blksize"]=>
  int(4096)
  ["blocks"]=>
  int(0)
}
eio_mknod_ok
```

### Дивіться також

-   [eio\_open()](function.eio-open.md) \- Відкриває файл
