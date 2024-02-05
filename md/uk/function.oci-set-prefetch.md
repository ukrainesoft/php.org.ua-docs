---
navigation:
  - function.oci-set-prefetch-lob.md: « oci\_set\_prefetch\_lob
  - function.oci-statement-type.md: oci\_statement\_type »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_set\_prefetch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_set\_prefetch

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_set\_prefetch — Встановлює кількість рядків, які будуть автоматично вибрані в буфер

### Опис

```methodsynopsis
oci_set_prefetch(resource $statement, int $rows): bool
```

Встановлює кількість рядків, які будуть вибрані в буфер клієнтськими бібліотеками Oracle відразу після успішного виклику [oci\_execute()](function.oci-execute.md) і кожного наступного внутрішнього запиту даних до базі. Продуктивність може бути значно збільшена для запитів, що повертають велику кількість рядків, за допомогою встановлення значення попередньої вибірки більше значення за замовчуванням [oci8.default\_prefetch](oci8.configuration.md#ini.oci8.default-prefetch)

Попередня вибірка - це ефективний механізм Oracle, що дозволяє повертати більше одного рядка результату бази даних за кожен мережевий запит. Це дає більш раціональне використання мережі та процесора. Буферизація рядків відбувається всередині OCI8, тому поведінка функцій вибірки OCI8 не залежить від розміру попередньої вибірки. Наприклад, [oci\_fetch\_row()](function.oci-fetch-row.md) завжди повертає один рядок. Буфер попередньої вибірки резервується окремо на кожен запит і не використовується вдруге у повторно запущених запитах або інших з'єднаннях.

Перед викликом [oci\_execute()](function.oci-execute.md) викличте **oci\_set\_prefetch()**

Сенс налаштування розміру попередньої вибірки полягає у підборі зручного значення передачі у мережі і обробки базі даних. Для запитів, що повертають дуже велику кількість рядків, загальна продуктивність системи може бути кращою, якщо рядки повертатимуться в кілька прийомів (тобто встановити розмір попередньої вибірки менше кількості рядків). Це дозволить базі даних обробляти запити інших користувачів протягом обробки PHP-скриптом поточного результату запиту.

Попередня вибірка запитів з'явилася у Oracle 8*i*. Попередня вибірка REF CURSOR з'явилася у Oracle 11*g*R2 і може бути застосована у випадку, якщо PHP злінковано з клієнтськими бібліотеками Oracle 11*g*R2 та старше. Попередня вибірка вкладених курсорів була додана до Oracle 11*g*R2 та вимагає наявності версії 11*g*R2 і старше як для клієнтських бібліотек Oracle, так і для бази даних, що використовується.

Попередня вибірка не підтримується якщо запити містять LONG або LOB стовпці. Значення попередньої вибірки ігнорується і, у всіх ситуаціях, що не підтримують попередню вибірку, буде використана рядкова вибірка.

При використанні Oracle Database 12*c*, попередня вибірка задана PHP може бути змінена конфігураційним файлом `oraaccess.xml` клієнта Oracle. Для отримання додаткових відомостей зверніться до документації Oracle.

### Список параметрів

`statement`

Коректний ідентифікатор виразу OCI8, отриманий з [oci\_parse()](function.oci-parse.md) та виконаний функцією [oci\_execute()](function.oci-execute.md), або ідентифікатор виразу `REF CURSOR`

`rows`

Кількість рядків попередньої вибірки >= 0

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Зміна попередньої вибірки за замовчуванням для запиту**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');

$stid = oci_parse($conn, 'SELECT * FROM myverybigtable');
oci_set_prefetch($stid, 300);  // Устанавливаем перед вызовом oci_execute()
oci_execute($stid);

echo "<table border='1'>\n";
while ($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS)) {
    echo "<tr>\n";
    foreach ($row as $item) {
        echo "    <td>".($item !== null ? htmlentities($item, ENT_QUOTES) : "")."</td>\n";
    }
    echo "</tr>\n";
}
echo "</table>\n";

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #2 Зміна значення попередньої вибірки за промовчанням для вибірки REF CURSOR**

```php
<?php
/*
  Создайте хранимую процедуру PL/SQL следующим образом:

  CREATE OR REPLACE PROCEDURE myproc(p1 OUT SYS_REFCURSOR) AS
  BEGIN
    OPEN p1 FOR SELECT * FROM all_objects WHERE ROWNUM < 5000;
  END;
*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');

$stid = oci_parse($conn, 'BEGIN myproc(:rc); END;');
$refcur = oci_new_cursor($conn);
oci_bind_by_name($stid, ':rc', $refcur, -1, OCI_B_CURSOR);
oci_execute($stid);

// Меняем размер предварительной выборки перед запуском курсора.
// Предварительная выборка REF CURSOR работает в случае линковки PHP
// с клиентскими библиотеками Oracle 11gR2 и старше
oci_set_prefetch($refcur, 200);
oci_execute($refcur);

echo "<table border='1'>\n";
while ($row = oci_fetch_array($refcur, OCI_ASSOC+OCI_RETURN_NULLS)) {
    echo "<tr>\n";
    foreach ($row as $item) {
        echo "    <td>".($item !== null ? htmlentities($item, ENT_QUOTES) : "")."</td>\n";
    }
    echo "</tr>\n";
}
echo "</table>\n";

oci_free_statement($refcur);
oci_free_statement($stid);
oci_close($conn);

?>
```

Якщо PHP OCI8 робить вибірку з REF CURSOR, а потім передає REF CURSOR назад в іншу PL/SQL-процедуру для подальшої обробки, необхідно встановити розмір попередньої вибірки REF CURSOR щоб уникнути "втрати" рядів з результату. Значення попередньої вибірки - це кількість "зайвих" рядів, отриманих кожним внутрішнім запитом OCI8 до бази даних, тому встановлення його в означає вибірку лише одного ряду за один раз.

**Приклад #3 Встановлення значення попередньої вибірки під час передачі REF CURSOR назад у Oracle**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/orcl');

// получение REF CURSOR
$stid = oci_parse($conn, 'BEGIN myproc(:rc_out); END;');
$refcur = oci_new_cursor($conn);
oci_bind_by_name($stid, ':rc_out', $refcur, -1, OCI_B_CURSOR);
oci_execute($stid);

// Отображаем два ряда, но больше не предвыбираем других рядов, иначе
// эти ряды не будут переданы обратно в  myproc_use_rc().
oci_set_prefetch($refcur, 0);
oci_execute($refcur);
$row = oci_fetch_array($refcur);
var_dump($row);
$row = oci_fetch_array($refcur);
var_dump($row);

// передаём REF CURSOR в myproc_use_rc() для дальнейшей обработки результата
$stid = oci_parse($conn, 'begin myproc_use_rc(:rc_in); end;');
oci_bind_by_name($stid, ':rc_in', $refcur, -1, OCI_B_CURSOR);
oci_execute($stid);

?>
```

### Дивіться також

-   Директива[oci8.default\_prefetch](oci8.configuration.md#ini.oci8.default-prefetch)
