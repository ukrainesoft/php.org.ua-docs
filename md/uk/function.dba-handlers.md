---
navigation:
  - function.dba-firstkey.md: « dba\_firstkey
  - function.dba-insert.md: dba\_insert »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dba\_handlers
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dba\_handlers

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

dba\_handlers — Список доступних обробників

### Опис

```methodsynopsis
dba_handlers(bool $full_info = false): array
```

**dba\_handlers()** повертає список усіх доступних у цьому модулі обробників.

### Список параметрів

`full_info`

Включає або вимикає виведення повної інформації в результат.

### Значення, що повертаються

Повертає масив обробників баз даних. Якщо параметр `full_info`задан, как\*\*`true`\*\*, масив міститиме асоціативний масив, де ключами будуть імена обробників, а значенням інформація про версію. В іншому випадку, масив буде індексованим масивом і міститиме імена обробників як значення.

> **Зауваження** :
> 
> Якщо використовується вбудована база даних, ви побачите і `cdb`и`cdb_make`

### Приклади

**Приклад #1 Приклад використання** dba\_handlers()\*\*\*\*

```php
<?php

echo "Доступные обработчики DBA:\n";
foreach (dba_handlers(true) as $handler_name => $handler_version) {
  // Очищаем строки с версиями
  $handler_version = str_replace('$', '', $handler_version);
  echo " - $handler_name: $handler_version\n";
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
Доступные обработчики DBA:
 - cdb: 0.75, Revision: 1.3.2.3
 - cdb_make: 0.75, Revision: 1.2.2.4
 - db2: Sleepycat Software: Berkeley DB 2.7.7: (08/20/99)
 - inifile: 1.0, Revision: 1.6.2.3
 - flatfile: 1.0, Revision: 1.5.2.4
```
