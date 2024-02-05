---
navigation:
  - zookeeper.set.md: '« Zookeeper::set'
  - zookeeper.setdebuglevel.md: 'Zookeeper::setDebugLevel »'
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::setAcl'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Метод видає помилку/попередження PHP, коли кількість параметрів або типи неправильні або не вдається встановити ACL для вузла.

**Застереження**

Починаючи з версії 0.3.0 метод викидає [ZookeeperException](class.zookeeperexception.md) та його похідні.

### Приклади

**Приклад #1 Приклад використання** Zookeeper::setAcl()\*\*\*\*

Встановіть ACL для вузла.

```php
<?php
$zookeeper = new Zookeeper('locahost:2181');
$aclArray = array(
  array(
    'perms'  => Zookeeper::PERM_ALL,
    'scheme' => 'world',
    'id'     => 'anyone',
  )
);
$path = '/path/to/newnode';
$zookeeper->setAcl($path, $aclArray);

$r = $zookeeper->getAcl($path);
if ($r)
  var_dump($r);
else
  echo 'Ошибка';
?>
```

Результат виконання наведеного прикладу:

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

-   [Zookeeper::create()](zookeeper.create.md) \- Створює синхронно вузол
-   [Zookeeper::getAcl()](zookeeper.getacl.md) \- Синхронно отримує ACL, пов'язаний із вузлом
-   [Дозволи ZooKeeper](class.zookeeper.md#zookeeper.class.constants.perms)
-   [ZookeeperException](class.zookeeperexception.md)
