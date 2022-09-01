---
navigation:
  - function.oci-set-module-name.html: « ocisetmodulename
  - function.oci-set-prefetch.html: ocisetprefetch »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ocisetprefetchлоб
---
# ocisetprefetchлоб

(PHP 8.2, PECL OCI8> = 3.2)

ocisetprefetchlob — Встановлює обсяг даних, що попередньо вибираються для кожного CLOB або BLOB

### Опис

```methodsynopsis
oci_set_prefetch_lob(resource $statement, int $prefetch_lob_size): bool
```

Встановлює розмір внутрішнього буфера, який використовується для вибірки кожного значення CLOB або BLOB, коли реалізація отримує внутрішній локатор LOB Oracle з бази даних після успішного виклику запиту до функції [ociexecute()](function.oci-execute.md) і кожного наступного внутрішнього запиту вибірки до бази даних. Збільшення цього значення може покращити продуктивність вибірки менших LOB за рахунок скорочення кругових обходів між PHP та базою даних. Використання пам'яті зміниться.

Значення впливає на великі об'єкти, що повертаються як екземпляри OCILob, а також на ті, що повертаються з використанням **`OCI_RETURN_LOBS`**

Функція **ocisetprefetchлоб()** викликається до виклику [ociexecute()](function.oci-execute.md). Якщо функція не була викликана, використовується значення [oci8.prefetchlobsize](oci8.configuration.html#ini.oci8.prefetch-lob-size)

Значення попередньої вибірки LOB слід встановлювати лише Oracle Database 12.2 або новіше.

### Список параметрів

`statement`

Коректний ідентифікатор виразу OCI8, отриманий з [ociparse()](function.oci-parse.html) та виконаний функцією [ociexecute()](function.oci-execute.md), або ідентифікатор виразу `REF CURSOR`

`prefetch_lob_size`

Число байтів кожного LOB, яке потрібно заздалегідь вибрати, >= 0.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Зміна попередньої вибірки LOB для запиту**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');

$stid = oci_parse($conn, 'SELECT myclob FROM mytable');
oci_set_prefetch_lob($stid, 100000);  // Установка значения перед вызовом oci_execute()
oci_execute($stid);

echo "<table border='1'>\n";
while ($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS+OCI_RETURN_LOBS)) {
    echo "<tr>\n";
    foreach ($row as $item) {
        echo "    <td>".($item !== null ? htmlentities($item, ENT_QUOTES) : "&nbsp;")."</td>\n";
    }
    echo "</tr>\n";
}
echo "</table>\n";

oci_free_statement($stid);
oci_close($conn);

?>
```

### Дивіться також

-   INI-опція [oci8.prefetchlobsize](oci8.configuration.html#ini.oci8.prefetch-lob-size)
