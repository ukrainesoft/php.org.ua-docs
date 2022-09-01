---
navigation:
  - zookeeper.delete.html: '« Zookeeper::delete'
  - zookeeper.get.html: 'Zookeeper::get »'
  - index.html: PHP Manual
  - class.zookeeper.html: Zookeeper
title: 'Zookeeper::exists'
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

Починаючи з версії 0.3.0, метод викидає виняток [ZookeeperException](class.zookeeperexception.html) та його похідні.

### Приклади

**Приклад #1 Приклад використання **Zookeeper::exists()****

Перевірте наявність вузла.

```php
<?php
$zookeeper = new Zookeeper('locahost:2181');
$path = '/path/to/node';
$r = $zookeeper->exists($path);
if ($r)
  echo 'Существет';
else
  echo 'Не определено или ошибка';
?>
```

Результат виконання цього прикладу:

```
Существет
```

### Дивіться також

-   [Zookeeper::get()](zookeeper.get.html) - Синхронно отримує дані, пов'язані з вузлом
-   [ZookeeperException](class.zookeeperexception.html)
