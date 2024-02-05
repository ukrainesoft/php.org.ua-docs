---
navigation:
  - function.oci-client-version.md: « oci\_client\_version
  - function.oci-commit.md: oci\_commit »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_close

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_close — Закриває з'єднання із сервером Oracle

### Опис

```methodsynopsis
oci_close(resource $connection): ?bool
```

Звільняє `connection`. Відповідне йому з'єднання з базою даних буде закрито за відсутності ресурсів, що його використовують, і якщо воно було отримано з функції [oci\_connect()](function.oci-connect.md) або [oci\_new\_connect()](function.oci-new-connect.md)

Рекомендується закривати більше не використовувані з'єднання, т.к. це звільняє ресурси бази даних іншим користувачам.

### Список параметрів

`connection`

Ідентифікатор з'єднання Oracle, отриманий із функцій [oci\_connect()](function.oci-connect.md) [oci\_pconnect()](function.oci-pconnect.md) або [oci\_new\_connect()](function.oci-new-connect.md)

### Значення, що повертаються

Повертає **`null`** якщо [oci8.old\_oci\_close\_semantics](oci8.configuration.md#ini.oci8.old-oci-close-semantics) включений або **`true`** в іншому випадку.

### Приклади

**Приклад #1 Закриття з'єднання**

Супутні з'єднання ресурси мають бути закриті для забезпечення коректного завершення з'єднання з базою даних та звільнення її ресурсів.

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT * FROM departments');
$r = oci_execute($stid);
oci_fetch_all($stid, $res);
var_dump($res);

// Освобождаем идентификатор выражения при закрытии соединения
oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #2 З'єднання бази даних не закривається доти, доки не будуть закриті всі посилання на нього**

Внутрішній лічильник посилань (refcount) ідентифікатора з'єднання повинен дорівнювати нулю перед безпосереднім закриттям з'єднання до бази даних.

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT * FROM departments');  // это увеличивает refcount на $conn
oci_execute($stid);
oci_fetch_all($stid, $res);
var_dump($res);

oci_close($conn);

// $conn больше не может использоваться в данном скрипте, но реальное
// соединение с базой данных будет открыто, пока не будет освобождена $stid.
var_dump($conn);  // выводит NULL

// Пока PHP спит, запрос к виду Oracle V$SESSION в окне терминала
// покажет, что пользователь базы данных всё ещё подключён.
sleep(10);

// Как только $stid освобождается, соединение к базе данных физически закрывается
oci_free_statement($stid);

// Пока PHP спит, запрос к виду Oracle V$SESSION в окне терминала
// покажет, что пользователь базы данных уже отключился.
sleep(10);

?>
```

**Приклад #3 Закриття з'єднання, відкритого кілька разів**

При повторному використанні облікових даних користувача обидві з'єднання повинні бути закриті перед безпосереднім закриттям з'єднання до бази даних.

```php
<?php

$conn1 = oci_connect('hr', 'welcome', 'localhost/XE');

// Использование тех же учётных данных повторно использует одно и то же
// соединение с базой данных. Любые незафиксированные изменения в
// $conn1 будут видны в $conn2
$conn2 = oci_connect('hr', 'welcome', 'localhost/XE');

// Пока PHP спит, запрос к виду Oracle V$SESSION в окне терминала
// покажет, что подключён только один пользователь базы данных.
sleep(10);

oci_close($conn1); // не закрывает реальное соединение с базой данных
var_dump($conn1);  // выводит NULL, т.к. $conn1 теперь бесполезна
var_dump($conn2);  // показывает, что $conn2 всё ещё является корректным ресурсом соединения

?>
```

**Приклад #4 З'єднання закривається при відході змінних в області видимості**

Коли всі змінні, що посилаються на з'єднання, йдуть з області видимості та звільняються PHP, відбувається відкат транзакції (якщо необхідно) і з'єднання з базою закривається.

```php
<?php

function myfunc() {
    $conn = oci_connect('hr', 'hrpwd', 'localhost/XE');
    if (!$conn) {
        $e = oci_error();
        trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
    }

    $stid = oci_parse($conn, 'UPDATE mytab SET id = 100');
    oci_execute($stid, OCI_NO_AUTO_COMMIT);
    return "Закончили!";
}

$r = myfunc();
// В этой точке происходит откат транзакции и закрывается соответствующее
// соединение с базой данных

print $r;  // отображает возвращённое функцией значение "Закончили!"

?>
```

### Примітки

> **Зауваження** :
> 
> Змінні, залежні від ідентифікатора з'єднань, такі як ідентифікатори виразів, отримані з [oci\_parse()](function.oci-parse.md), повинні бути звільнені до закриття з'єднання з базою даних.

> **Зауваження** :
> 
> Функция**oci\_close()** не закриває з'єднання з базою даних, створеними функцією [oci\_pconnect()](function.oci-pconnect.md)

### Дивіться також

-   [oci\_connect()](function.oci-connect.md) \- Встановлює з'єднання з базою даних Oracle
-   [oci\_free\_statement()](function.oci-free-statement.md) \- Звільняє ресурси, які займає курсор або SQL-вираз.
