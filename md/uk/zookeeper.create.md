---
navigation:
  - zookeeper.construct.md: '« Zookeeper::\_\_construct'
  - zookeeper.delete.md: 'Zookeeper::delete »'
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::create'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Zookeeper::create

(PECL zookeeper >= 0.1.0)

Zookeeper::create — Створює синхронно вузол.

### Опис

```methodsynopsis
public
   Zookeeper::create(    string $path,    string $value,    array $acls,    int $flags = null): string
```

Метод створить вузол у ZooKeeper. Вузол може бути створений тільки в тому випадку, якщо він ще не існує. Прапори створення впливають створення вузлів. Якщо встановлено прапор ZOO\_EPHEMERAL, вузол автоматично видаляється, якщо сеанс клієнта завершується. Якщо встановлено прапор ZOO\_SEQUENCE, до імені шляху додається унікальний порядковий номер, що монотонно збільшується.

### Список параметрів

`path`

Назва вузла. Виражається як ім'я файлу з косою межею, що розділяє предків вузла.

`value`

Дані для зберігання у вузлі.

`acls`

Початковий ACL вузла. ACL не може бути нульовим або порожнім.

`flags`

Може бути 0 для звичайного створення або із зазначенням прапорів створення.

### Значення, що повертаються

Повертає шлях нового вузла (він може відрізнятись від зазначеного шляху через прапор ZOO\_SEQUENCE) у разі успішного виконання та false у разі виникнення помилки.

### Помилки

Метод видає PHP повідомлення про помилку/попередження, коли кількість параметрів або їх типи неправильні або не вдалося створити вузол.

**Застереження**

Починаючи з версії 0.3.0, метод викидає виняток [ZookeeperException](class.zookeeperexception.md) та його похідні.

### Приклади

**Приклад #1 Приклад використання** Zookeeper::create()\*\*\*\*

Створення нового вузла.

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
$realPath = $zookeeper->create($path, null, $aclArray);
if ($realPath)
  echo $realPath;
else
  echo 'Ошибка';
?>
```

Результат виконання наведеного прикладу:

```
/path/to/newnode
```

### Дивіться також

-   [Zookeeper::delete()](zookeeper.delete.md) \- Видаляє синхронно вузол у zookeeper
-   [Zookeeper::getChildren()](zookeeper.getchildren.md) \- Виводить список нащадків вузла синхронно
-   [Дозволи ZooKeeper](class.zookeeper.md#zookeeper.class.constants.perms)
-   [ZookeeperException](class.zookeeperexception.md)
