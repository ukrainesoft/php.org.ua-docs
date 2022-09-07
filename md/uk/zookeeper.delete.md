---
navigation:
  - zookeeper.create.md: '« Zookeeper::create'
  - zookeeper.exists.md: 'Zookeeper::exists »'
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::delete'
---
# Zookeeper::delete

(PECL zookeeper >= 0.2.0)

Zookeeper::delete — Видаляє синхронно вузол у zookeeper

### Опис

```methodsynopsis
public
   Zookeeper::delete(string $path, int $version = -1): bool
```

### Список параметрів

`path`

Назва вузла. Виражається як ім'я файлу з косою межею, що розділяє предків вузла.

`version`

Очікувана версія вузла. Функція завершиться помилкою, якщо фактична версія вузла не відповідає очікуваній версії. Якщо використовується -1, перевірка версії не виконуватиметься.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Метод видає PHP повідомлення про помилку/попередження, коли кількість параметрів або їх типи неправильні або видалити вузол.

**Застереження**

Починаючи з версії 0.3.0, метод викидає виняток [ZookeeperException](class.zookeeperexception.md) та його похідні.

### Приклади

**Приклад #1 Приклад використання **Zookeeper::delete()****

Видалення існуючого вузла.

```php
<?php
$zookeeper = new Zookeeper('locahost:2181');
$path = '/path/to/node';
$r = $zookeeper->delete($path);
if ($r)
  echo 'Успешное выполнение';
else
  echo 'Ошибка';
?>
```

Результат виконання цього прикладу:

```
Успешное выполнение
```

### Дивіться також

-   [Zookeeper::create()](zookeeper.create.md) - Створює синхронно вузол
-   [Zookeeper::getChildren()](zookeeper.getchildren.md) - Виводить список нащадків вузла синхронно
-   [ZookeeperException](class.zookeeperexception.md)
