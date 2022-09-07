---
navigation:
  - memcache.examples.md: « Приклади
  - class.memcache.md: Memcache »
  - index.md: PHP Manual
  - memcache.examples.md: Приклади
title: Базове використання
---
## Базове використання

**Приклад #1 Приклад використання модуля memcache**

У цьому прикладі відбувається збереження об'єкта в кеші та його подальше читання. Об'єкти та інші нескалярні типи серіалізуються перед збереженням, що унеможливлює зберігання ресурсів (наприклад, ідентифікаторів підключень та ін.) у кеші.

```php
<?php

$memcache = new Memcache;
$memcache->connect('localhost', 11211) or die ("Не могу подключиться");

$version = $memcache->getVersion();
echo "Версия сервера: ".$version."<br/>\n";

$tmp_object = new stdClass;
$tmp_object->str_attr = 'test';
$tmp_object->int_attr = 123;

$memcache->set('key', $tmp_object, false, 10) or die ("Ошибка при сохранении данных на сервере");
echo "Данные сохранены в кеше. (время жизни данных 10 секунд)<br/>\n";

$get_result = $memcache->get('key');
echo "Данные из кеша:<br/>\n";

var_dump($get_result);

?>
```

**Приклад #2 Використання memcache як оброблювач сесій**

```php
<?php

$session_save_path = "tcp://$host:$port?persistent=1&weight=2&timeout=2&retry_interval=10,  ,tcp://$host:$port  ";
ini_set('session.save_handler', 'memcache');
ini_set('session.save_path', $session_save_path);

?>
```
