---
navigation:
  - memcached.addservers.md: '« Memcached::addServers'
  - memcached.appendbykey.md: 'Memcached::appendByKey »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::append'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::append

(PECL memcached >= 0.1.0)

Memcached::append — Додає дані до існуючого запису

### Опис

```methodsynopsis
public Memcached::append(string $key, string $value): ?bool
```

\*\*Memcached::append()\*\*добавляет переданную в`value` рядок до існуючого запису. Причина того, що `value` приводиться до рядка у цьому, що додавання змішаних типів не визначено.

> **Зауваження** :
> 
> Якщо параметр **`Memcached::OPT_COMPRESSION`** встановлений, то операція буде завершена помилкою і буде виведено попередження, тому що додавання стислих даних до запису, який вже стислий, неможливо.

### Список параметрів

`key`

Ключ, під яким зберігається значення.

`value`

Рядок для додавання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Повертає **`null`**, якщо стиснення увімкнено.

### Помилки

Повертає **`null`** та видає помилку рівня **`E_WARNING`**, якщо стиснення увімкнено.

### Приклади

**Приклад #1 Приклад використання** Memcached::append()\*\*\*\*

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);
$m->setOption(Memcached::OPT_COMPRESSION, false);

$m->set('foo', 'abc');
$m->append('foo', 'def');
var_dump($m->get('foo'));
?>
```

Результат виконання наведеного прикладу:

```
string(6) "abcdef"
```

### Дивіться також

-   [Memcached::appendByKey()](memcached.appendbykey.md) \- Додає дані до наявного запису на заданому сервері
-   [Memcached::prepend()](memcached.prepend.md) \- Додає дані на початок існуючого запису
