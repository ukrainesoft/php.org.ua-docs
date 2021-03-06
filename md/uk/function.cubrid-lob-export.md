- [«cubrid_lob_close](function.cubrid-lob-close.md)
- [cubrid_lob_get »](function.cubrid-lob-get.md)

- [PHP Manual](index.md)
- [Функції CUBRID](ref.cubrid.md)
- Експортує дані BLOB/CLOB у файл

#cubrid_lob_export

(PECL CUBRID = 8.3.1)

cubrid_lob_export — Експортує дані BLOB/CLOB у файл

### Опис

**cubrid_lob_export**(resource `$conn_identifier`, resource
`$lob_identifier`, string `$path_name`): bool

**cubrid_lob_export()** використовується для отримання даних BLOB/CLOB з
бази даних CUBRID та збереження їх вмісту у файл. Щоб
використовувати цю функцію, необхідно спочатку використовувати
[cubrid_lob_get()](function.cubrid-lob-get.md), щоб отримати
інформацію BLOB/CLOB із CUBRID.

### Список параметрів

`conn_identifier`
Ідентифікатор підключення.

`lob_identifier`
Ідентифікатор LOB.

`path_name`
Ім'я шляху файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubrid_lob_export()****

`<?php$conn = cubrid_connect ("localhost", 33000, "demodb", "dba");cubrid_execute($conn,"DROP TABLE if exists doc");cubrid_execute($conn,"C , doc_content CLOB)");cubrid_execute($conn,"INSERT INTO doc VALUES (5,'hello,cubrid')");$lobs = cubrid_lob_get($conn, "SELECT doc_content FROM| "Розмір документа: ".cubrid_lob_size($lobs[0])." байтів";cubrid_lob_export($conn, $lobs[0], "doc_5.txt");cubrid_lob_close($lobs);$brid > `

### Дивіться також

- [cubrid_lob_get()](function.cubrid-lob-get.md) - Отримує дані
BLOB/CLOB
- [cubrid_lob_close()](function.cubrid-lob-close.md) - Закриває
дані BLOB/CLOB
- [cubrid_lob_size()](function.cubrid-lob-size.md) - Отримує розмір
даних BLOB/CLOB
- [cubrid_lob_send()](function.cubrid-lob-send.md) - Читає дані
BLOB/CLOB та відправляє їх прямо до браузера
