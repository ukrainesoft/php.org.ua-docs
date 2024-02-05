---
navigation:
  - class.zookeeper.md: « Zookeeper
  - zookeeper.close.md: 'Zookeeper::close »'
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::addAuth'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Zookeeper::addAuth

(PECL zookeeper >= 0.1.0)

Zookeeper::addAuth — Вказує облікові дані програми

### Опис

```methodsynopsis
public
   Zookeeper::addAuth(string $scheme, string $cert, callable $completion_cb = null): bool
```

Програма викликає цю функцію, щоб вказати свої облікові дані для цілей автентифікації. Сервер буде використовувати провайдера безпеки, вказаного в параметрі схеми, для автентифікації клієнтського з'єднання. Якщо запит про аутентифікацію не вдався: - з'єднання з сервером буде розірвано. - Спостерігач викликається зі значенням ZOO\_AUTH\_FAILED\_STATE як параметр стану.

### Список параметрів

`scheme`

Ідентифікатор схеми автентифікації. Вбудована підтримка: "digest" автентифікації на основі пароля

`cert`

Облікові дані програми. Фактичне значення залежить від схеми.

`completion_cb`

Підпрограма, щоб викликати, коли запит завершується. Один із наступних кодів результату може бути переданий в callback-функцію завершення: - Операція ZOK успішно завершена - ZAUTHFAILED автентифікація не вдалася

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Метод видає PHP-повідомлення про помилку/попередження, коли кількість параметрів чи типи неправильні або операція завершується невдало.

**Застереження**

Починаючи з версії 0.3.0, метод генерує виняток [ZookeeperException](class.zookeeperexception.md) та його похідні.

### Приклади

**Пример #1 Пример использования**Zookeeper::addAuth()\*\*\*\*

Додавання аутентифікації перед запитом вузла.

```php
<?php
$zookeeper = new Zookeeper('locahost:2181');
$path = '/path/to/node';
$value = 'nodevalue';
$zookeeper->set($path, $value);

$zookeeper->addAuth('digest', 'user0:passwd0');
$r = $zookeeper->get($path);
if ($r)
  echo $r;
else
  echo 'Ошибка';
?>
```

Результат виконання наведеного прикладу:

```
nodevalue
```

### Дивіться також

-   [Zookeeper::create()](zookeeper.create.md) \- Створює синхронно вузол
-   [Zookeeper::setAcl()](zookeeper.setacl.md) \- Встановлює ACL, пов'язаний із вузлом синхронно
-   [Zookeeper::getAcl()](zookeeper.getacl.md) \- Синхронно отримує ACL, пов'язаний із вузлом
-   [Стан ZooKeeper](class.zookeeper.md#zookeeper.class.constants.states)
-   [ZookeeperException](class.zookeeperexception.md)
