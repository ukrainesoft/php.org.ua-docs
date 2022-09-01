---
navigation:
  - zookeeper.isrecoverable.md: '« Zookeeper::isRecoverable'
  - zookeeper.setacl.md: 'Zookeeper::setAcl »'
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::set'
---
# Zookeeper::set

(PECL zookeeper >= 0.1.0)

Zookeeper::set — Встановлює дані, пов'язані з вузлом

### Опис

```methodsynopsis
public
   Zookeeper::set(    string $path,    string $value,    int $version = -1,    array &$stat = null): bool
```

### Список параметрів

`path`

Ім'я вузла. Виражається як ім'я файлу з косою межею, що розділяє предків вузла.

`value`

Дані, які зберігатимуться у вузлі.

`version`

Очікувана версія вузла. Функція завершиться помилкою, якщо фактична версія вузла відповідає очікуваної. Якщо використовується -1, перевірка версії не виконуватиметься.

`stat`

Якщо не NULL, при поверненні буде збережено значення stat для шляху.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Метод видає помилку/попередження PHP, коли кількість параметрів або типи неправильні або не вдається зберегти значення у вузлі.

**Застереження**

Починаючи з версії 0.3.0 метод викидає [ZookeeperException](class.zookeeperexception.md) та його похідні.

### Приклади

**Приклад #1 Приклад використання **Zookeeper::set()****

Збереження значення у вузол.

```php
<?php
$zookeeper = new Zookeeper('locahost:2181');
$path = '/path/to/node';
$value = 'nodevalue';
$r = $zookeeper->set($path, $value);
if ($r)
  echo 'Значение сохранено';
else
  echo 'Ошибкак';
?>
```

Результат виконання цього прикладу:

```
SUCCESS
```

### Дивіться також

-   [Zookeeper::create()](zookeeper.create.md) - Створює синхронно вузол
-   [Zookeeper::get()](zookeeper.get.md) - Синхронно отримує дані, пов'язані з вузлом
-   [ZookeeperException](class.zookeeperexception.md)
