Встановлює ACL, пов'язаний із вузлом синхронно

-   [« Zookeeper::set](zookeeper.set.html)
    
-   [Zookeeper::setDebugLevel »](zookeeper.setdebuglevel.html)
    
-   [PHP Manual](index.html)
    
-   [Zookeeper](class.zookeeper.html)
    
-   Встановлює ACL, пов'язаний із вузлом синхронно
    

# Zookeeper::setAcl

(PECL zookeeper >= 0.1.0)

Zookeeper::setAcl — Встановлює ACL, пов'язаний із вузлом синхронно

### Опис

```methodsynopsis
public
   Zookeeper::setAcl(string $path, int $version, array $acl): bool
```

### Список параметрів

`path`

Ім'я вузла. Виражається як ім'я файлу з косою межею, що розділяє предків вузла.

`version`

Очікувана версія шляху.

`acl`

ACL, який потрібно встановити.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Метод видає помилку/попередження PHP, коли кількість параметрів або типи неправильні або не вдається встановити ACL для вузла.

**Застереження**

Починаючи з версії 0.3.0 метод викидає [ZookeeperException](class.zookeeperexception.html) та його похідні.

### Приклади

**Приклад #1 Приклад використання **Zookeeper::setAcl()****

Встановіть ACL для вузла.

```php
<?php
$zookeeper = new Zookeeper('locahost:2181');
$aclArray = array(
  array(
    'perms'  => Zookeeper::PERM_ALL,
    'scheme' => 'world',
    'id'     => 'anyone',
  )
);
$path = '/path/to/newnode';
$zookeeper->setAcl($path, $aclArray);

$r = $zookeeper->getAcl($path);
if ($r)
  var_dump($r);
else
  echo 'Ошибка';
?>
```

Результат виконання цього прикладу:

```
array(1) {
  [0]=>
  array(3) {
    ["perms"]=>
    int(31)
    ["scheme"]=>
    string(5) "world"
    ["id"]=>
    string(6) "anyone"
  }
}
```

### Дивіться також

-   [Zookeeper::create()](zookeeper.create.html) - Створює синхронно вузол
-   [Zookeeper::getAcl()](zookeeper.getacl.html) - Синхронно отримує ACL, пов'язаний із вузлом
-   [Разрешения ZooKeeper](class.zookeeper.html#zookeeper.class.constants.perms)
-   [ZookeeperException](class.zookeeperexception.html)