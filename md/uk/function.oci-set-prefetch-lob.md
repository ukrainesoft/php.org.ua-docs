---
navigation:
  - function.oci-set-module-name.md: « oci\_set\_module\_name
  - function.oci-set-prefetch.md: oci\_set\_prefetch »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_set\_prefetch\_lob
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_set\_prefetch\_lob

(PHP 8.2, PECL OCI8 >= 3.2)

oci\_set\_prefetch\_lob — Встановлює обсяг даних, що попередньо вибираються для кожного CLOB або BLOB

### Опис

```methodsynopsis
oci_set_prefetch_lob(resource $statement, int $prefetch_lob_size): bool
```

Встановлює розмір внутрішнього буфера, який використовується для вибірки кожного значення CLOB або BLOB, коли реалізація отримує внутрішній локатор LOB Oracle з бази даних після успішного виклику запиту до функції [oci\_execute()](function.oci-execute.md) і кожного наступного внутрішнього запиту вибірки до бази даних. Збільшення цього значення може покращити продуктивність вибірки менших LOB за рахунок скорочення кругових обходів між PHP та базою даних. Використання пам'яті зміниться.

Значення впливає на великі об'єкти, що повертаються як екземпляри OCILob, а також на ті, що повертаються з використанням **`OCI_RETURN_LOBS`**

Функция**oci\_set\_prefetch\_lob()** викликається до виклику [oci\_execute()](function.oci-execute.md). Якщо функція не була викликана, використовується значення [oci8.prefetch\_lob\_size](oci8.configuration.md#ini.oci8.prefetch-lob-size)

Значення попередньої вибірки LOB слід встановлювати лише Oracle Database 12.2 або новіше.

### Список параметрів

`statement`

Коректний ідентифікатор виразу OCI8, отриманий з [oci\_parse()](function.oci-parse.md) та виконаний функцією [oci\_execute()](function.oci-execute.md), або ідентифікатор виразу `REF CURSOR`

`prefetch_lob_size`

Число байтів кожного LOB, яке потрібно заздалегідь вибрати, >= 0.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Змінення попередньої вибірки LOB для запиту**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');

$stid = oci_parse($conn, 'SELECT myclob FROM mytable');
oci_set_prefetch_lob($stid, 100000);  // Установка значения перед вызовом oci_execute()
oci_execute($stid);

echo "<table border='1'>\n";
while ($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS+OCI_RETURN_LOBS)) {
    echo "<tr>\n";
    foreach ($row as $item) {
        echo "    <td>".($item !== null ? htmlentities($item, ENT_QUOTES) : "&nbsp;")."</td>\n";
    }
    echo "</tr>\n";
}
echo "</table>\n";

oci_free_statement($stid);
oci_close($conn);

?>
```

### Дивіться також

-   INI-опція[oci8.prefetch\_lob\_size](oci8.configuration.md#ini.oci8.prefetch-lob-size)
