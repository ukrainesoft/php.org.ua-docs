---
navigation:
  - memcached.ispristine.md: '« Memcached::isPristine'
  - memcached.prependbykey.md: 'Memcached::prependByKey »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::prepend'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::prepend

(PECL memcached >= 0.1.0)

Memcached::prepend — Додає дані на початок існуючого запису

### Опис

```methodsynopsis
public Memcached::prepend(string $key, string $value): ?bool
```

\*\*Memcached::prepend()\*\*добавляет строку, переданную в параметре`value` на початок існуючого запису. Причина того, що `value` приводиться до рядкового типу у цьому, що додавання значення початку комплексних типів не визначено.

> **Зауваження** :
> 
> Если установлен параметр\*\*`Memcached::OPT_COMPRESSION`\*\*, то виконання даного методу завершиться невдачею і буде виведено попередження, тому що додавання стислих даних до значення, яке можливе вже стиснуте, неможливе.

### Список параметрів

`key`

Ключ запису до якого відбувається додавання на початок.

`value`

Доданий рядок.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Повертає **`null`**, якщо стиснення увімкнено.

### Помилки

Повертає **`null`** та видає помилку рівня **`E_WARNING`**, якщо стиснення увімкнено.

### Приклади

**Приклад #1 Приклад використання** Memcached::prepend()\*\*\*\*

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);
$m->setOption(Memcached::OPT_COMPRESSION, false);

$m->set('foo', 'abc');
$m->prepend('foo', 'def');
var_dump($m->get('foo'));
?>
```

Результат виконання наведеного прикладу:

```
string(6) "defabc"
```

### Дивіться також

-   [Memcached::prependByKey()](memcached.prependbykey.md) \- Додає дані на початок існуючого запису на вказаному сервері
-   [Memcached::append()](memcached.append.md) \- Додає дані до існуючого запису
