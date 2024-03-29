---
navigation:
  - dba.examples.md: « Приклади
  - ref.dba.md: Функції DBA »
  - index.md: PHP Manual
  - dba.examples.md: Приклади
title: Базове використання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Базове використання

**Приклад #1 DBA приклад**

```php
<?php

$id = dba_open("/tmp/test.db", "n", "db2");

if (!$id) {
    echo "dba_open failed\n";
    exit;
}

dba_replace("key", "This is an example!", $id);

if (dba_exists("key", $id)) {
    echo dba_fetch("key", $id);
    dba_delete("key", $id);
}

dba_close($id);
?>
```

DBA є бінарно безпечним і не має будь-яких довільних обмежень. Тим не менш, він успадковує всі обмеження, встановлені базовою реалізацією бази даних

Усі файлові бази даних повинні забезпечувати спосіб встановлення файлового режиму щойно створеної бази даних, якщо це взагалі можливо. Файловий режим зазвичай передається як четвертий аргумент у [dba\_open()](function.dba-open.md) або [dba\_popen()](function.dba-popen.md)

Ви можете отримати всі записи бази даних у процедурному стилі, використовуючи функції [dba\_firstkey()](function.dba-firstkey.md) і [dba\_nextkey()](function.dba-nextkey.md). Ви не можете змінити базу даних під час її обходу.

**Приклад #2 Обхід бази даних**

```php
<?php

// ...open database...

$key = dba_firstkey($id);

while ($key !== false) {
    if (true) {          // запоминаем ключ для выполнения некоторых действий далее
        $handle_later[] = $key;
    }
    $key = dba_nextkey($id);
}

foreach ($handle_later as $val) {
    dba_delete($val, $id);
}

?>
```
