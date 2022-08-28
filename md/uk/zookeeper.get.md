Синхронно отримує дані, пов'язані з вузлом

-   [« Zookeeper::exists](zookeeper.exists.html)
    
-   [Zookeeper::getAcl »](zookeeper.getacl.html)
    
-   [PHP Manual](index.html)
    
-   [Zookeeper](class.zookeeper.html)
    
-   Синхронно отримує дані, пов'язані з вузлом
    

# Zookeeper::get

(PECL zookeeper >= 0.1.0)

Zookeeper::get — Синхронно отримує дані, пов'язані з вузлом

### Опис

```methodsynopsis
public
   Zookeeper::get(    string $path,    callable $watcher_cb = null,    array &$stat = null,    int $max_size = 0): string
```

### Список параметрів

`path`

Ім'я вузла. Виражається як ім'я файлу з косою межею, що розділяє предків вузла.

`watcher_cb`

Якщо ненульове значення на сервері буде встановлено спостереження, щоб повідомити клієнта про зміну вузла.

`stat`

Якщо не NULL, при поверненні буде збережено значення stat для шляху.

`max_size`

Максимальний обсяг даних. Якщо використовується 0, метод поверне всі дані.

### Значення, що повертаються

Повертає дані у разі успішного виконання та false у разі виникнення помилки.

### Помилки

Метод видає помилку/попередження PHP, коли кількість параметрів або типи неправильні або не вдається отримати значення від вузла.

**Застереження**

Починаючи з версії 0.3.0 метод викидає [ZookeeperException](class.zookeeperexception.html) та його похідні.

### Приклади

**Приклад #1 Приклад використання **Zookeeper::get()****

Набуття значення від вузла.

```php
<?php
$zookeeper = new Zookeeper('locahost:2181');
$path = '/path/to/node';
$value = 'nodevalue';
$zookeeper->set($path, $value);

$r = $zookeeper->get($path);
if ($r)
  echo $r;
else
  echo 'Ошибка';
?>
```

Результат виконання цього прикладу:

```
nodevalue
```

**Приклад #2 Приклад використання stat **Zookeeper::get()****

Отримання інформації про статистику сайту.

```php
<?php
$zookeeper = new Zookeeper('localhost:2181');
$path = '/path/to/node';
$stat = [];
$zookeeper->get($path, null, $stat);
var_dump($stat);
?>
```

Результат виконання цього прикладу:

```
array(11) {
  ["czxid"]=>
  float(0)
  ["mzxid"]=>
  float(0)
  ["ctime"]=>
  float(0)
  ["mtime"]=>
  float(0)
  ["version"]=>
  int(0)
  ["cversion"]=>
  int(-2)
  ["aversion"]=>
  int(0)
  ["ephemeralOwner"]=>
  float(0)
  ["dataLength"]=>
  int(0)
  ["numChildren"]=>
  int(2)
  ["pzxid"]=>
  float(0)
}
```

### Дивіться також

-   [Zookeeper::set()](zookeeper.set.html) - Встановлює дані, пов'язані з вузлом
-   [ZookeeperException](class.zookeeperexception.html)