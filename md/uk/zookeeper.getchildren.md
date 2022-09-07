---
navigation:
  - zookeeper.getacl.md: '« Zookeeper::getAcl'
  - zookeeper.getclientid.md: 'Zookeeper::getClientId »'
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::getChildren'
---
# Zookeeper::getChildren

(PECL zookeeper >= 0.1.0)

Zookeeper::getChildren - Виводить список нащадків вузла синхронно

### Опис

```methodsynopsis
public
   Zookeeper::getChildren(string $path, callable $watcher_cb = null): array
```

### Список параметрів

`path`

Ім'я вузла. Виражається як ім'я файлу з косою межею, що розділяє предків вузла.

`watcher_cb`

Якщо ненульове значення на сервері буде встановлено спостереження, щоб повідомити клієнта про зміну вузла.

### Значення, що повертаються

Повертає масив із дочірніми шляхами у разі успішного виконання та false у разі виникнення помилки.

### Помилки

Метод видає помилку/попередження PHP, коли кількість параметрів або типи неправильні або не вдається перерахувати дочірні елементи вузла.

**Застереження**

Починаючи з версії 0.3.0 метод викидає [ZookeeperException](class.zookeeperexception.md) та його похідні.

### Приклади

**Приклад #1 Приклад використання **Zookeeper::getChildren()****

Перелічує дочірні елементи сайту.

```php
<?php
$zookeeper = new Zookeeper('locahost:2181');
$path = '/zookeeper';
$r = $zookeeper->getchildren($path);
if ($r)
  var_dump($r);
else
  echo 'Ошибка';
?>
```

Результат виконання цього прикладу:

```
array(1) {
  [0]=>
  string(6) "config"
}
```

### Дивіться також

-   [Zookeeper::create()](zookeeper.create.md) - Створює синхронно вузол
-   [Zookeeper::delete()](zookeeper.delete.md) - Видаляє синхронно вузол у zookeeper
-   [ZookeeperException](class.zookeeperexception.md)
