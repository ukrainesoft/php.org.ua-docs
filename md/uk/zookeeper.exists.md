---
navigation:
  - zookeeper.delete.md: '« Zookeeper::delete'
  - zookeeper.get.md: 'Zookeeper::get »'
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::exists'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Zookeeper::exists

(PECL zookeeper >= 0.1.0)

Zookeeper::exists — Синхронно перевіряє наявність вузла в zookeeper

### Опис

```methodsynopsis
public
   Zookeeper::exists(string $path, callable $watcher_cb = null): array
```

### Список параметрів

`path`

Назва вузла. Виражається як ім'я файлу з косою межею, що розділяє предків вузла.

`watcher_cb`

Якщо не нуль, на сервері буде встановлено спостереження, щоб повідомити клієнта, якщо вузол змінюється. Спостереження буде встановлено, навіть якщо вузол немає.

### Значення, що повертаються

Повертає значення stat для шляху, якщо даний вузол існує, інакше повертає false.

### Помилки

Метод видає PHP повідомлення про помилку/попередження, коли кількість параметрів або їх типи є неправильними або не вдалося перевірити наявність вузла.

**Застереження**

Починаючи з версії 0.3.0, метод викидає виняток [ZookeeperException](class.zookeeperexception.md) та його похідні.

### Приклади

**Приклад #1 Приклад використання** Zookeeper::exists()\*\*\*\*

Перевірте наявність вузла.

```php
<?php
$zookeeper = new Zookeeper('locahost:2181');
$path = '/path/to/node';
$r = $zookeeper->exists($path);
if ($r)
  echo 'Существет';
else
  echo 'Не определено или ошибка';
?>
```

Результат виконання наведеного прикладу:

```
Существет
```

### Дивіться також

-   [Zookeeper::get()](zookeeper.get.md) \- Синхронно отримує дані, пов'язані з вузлом
-   [ZookeeperException](class.zookeeperexception.md)
