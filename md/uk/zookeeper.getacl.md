---
navigation:
  - zookeeper.get.md: '« Zookeeper::get'
  - zookeeper.getchildren.md: 'Zookeeper::getChildren »'
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::getAcl'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Zookeeper::getAcl

(PECL zookeeper >= 0.1.0)

Zookeeper::getAcl — Синхронно отримує ACL, пов'язаний із вузлом

### Опис

```methodsynopsis
public
   Zookeeper::getAcl(string $path): array
```

### Список параметрів

`path`

Ім'я вузла. Виражається як ім'я файлу з косою межею, що розділяє предків вузла.

### Значення, що повертаються

Повертає масив acl у разі успішного виконання та false у разі виникнення помилки.

### Помилки

Метод видає помилку/попередження PHP, коли кількість параметрів або типи неправильні або не вдається отримати ACL вузла.

**Застереження**

Починаючи з версії 0.3.0 метод викидає [ZookeeperException](class.zookeeperexception.md) та його похідні.

### Приклади

**Пример #1 Пример использования**Zookeeper::getAcl()\*\*\*\*

Отримання ACL вузла.

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
-   [Zookeeper::setAcl()](zookeeper.setacl.md) \- Встановлює ACL, пов'язаний із вузлом синхронно
-   [Дозволи ZooKeeper](class.zookeeper.md#zookeeper.class.constants.perms)
-   [ZookeeperException](class.zookeeperexception.md)
