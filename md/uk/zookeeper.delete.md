Видаляє синхронно вузол в zookeeper

-   [« Zookeeper::create](zookeeper.create.html)
    
-   [Zookeeper::exists »](zookeeper.exists.html)
    
-   [PHP Manual](index.html)
    
-   [Zookeeper](class.zookeeper.html)
    
-   Видаляє синхронно вузол в zookeeper
    

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

Починаючи з версії 0.3.0, метод викидає виняток [ZookeeperException](class.zookeeperexception.html) та його похідні.

### Приклади

**Приклад #1 Приклад використання **Zookeeper::delete()****

Видалення існуючого вузла.

```php
<?php
$zookeeper = new Zookeeper('locahost:2181');
$path = '/path/to/node';
$r = $zookeeper->delete($path);
if ($r)
  echo 'Успешное выполнение';
else
  echo 'Ошибка';
?>
```

Результат виконання цього прикладу:

```
Успешное выполнение
```

### Дивіться також

-   [Zookeeper::create()](zookeeper.create.html) - Створює синхронно вузол
-   [Zookeeper::getChildren()](zookeeper.getchildren.html) - Виводить список нащадків вузла синхронно
-   [ZookeeperException](class.zookeeperexception.html)