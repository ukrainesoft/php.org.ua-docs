---
navigation:
  - memcached.fetchall.html: '« Memcached::fetchAll'
  - memcached.get.html: 'Memcached::get »'
  - index.html: PHP Manual
  - class.memcached.html: Memcached
title: 'Memcached::flush'
---
# Memcached::flush

(PECL memcached >= 0.1.0)

Memcached::flush - Анулює всі записи в кеші

### Опис

```methodsynopsis
public Memcached::flush(int $delay = 0): bool
```

**Memcached::flush()** анулює всі існуючі записи в кеші негайно (за замовчуванням) або після закінчення періоду часу, зазначеного в `delay`. Після інвалідності жодних записів не буде повернено у відповідь на запити команд отримання даних (якщо записи не були збережені під тими самими ключами після виклику) **Memcached::flush()**). Насправді, інвалідування кешу не звільняє всю пам'ять, яку займають записи; це відбувається поступово в міру заповнення новими записами.

### Список параметрів

`delay`

Величина затримки за секунди перед анулюванням записів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Використовуйте за необхідності [Memcached::getResultCode()](memcached.getresultcode.md)

### Приклади

**Приклад #1 Приклад використання **Memcached::flush()****

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

/* Очищает все записи через 10 секунд */
$m->flush(10);
?>
```
