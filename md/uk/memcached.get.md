---
navigation:
  - memcached.flush.html: '« Memcached::flush'
  - memcached.getallkeys.html: 'Memcached::getAllKeys »'
  - index.html: PHP Manual
  - class.memcached.html: Memcached
title: 'Memcached::get'
---
# Memcached::get

(PECL memcached >= 0.1.0)

Memcached::get — Отримання запису

### Опис

```methodsynopsis
public Memcached::get(string $key, callable $cache_cb = ?, int $flags = ?): mixed
```

**Memcached::get()** повертає запис, який раніше був збережений під ключом `key`. Якщо елемент не знайдено і для параметра `flags` поставлено **`Memcached::GET_EXTENDED`**, вона також поверне значення токена CAS для цього запису. Зверніться до документації щодо [Memcached::cas()](memcached.cas.html) для отримання інформації про використання CAS токена . [Чтение при помощи кеширующих callback-функций](memcached.callbacks.html) може бути використано за допомогою параметра `cache_cb`

### Список параметрів

`key`

Ключ одержуваного запису.

`cache_cb`

Функція зворотного виклику для читання, що кешується, або **`null`**

`flags`

Прапори, що визначають результат, що повертається. Якщо задана константа **`Memcached::GET_EXTENDED`**, функція також поверне CAS токен.

### Значення, що повертаються

Повертає значення, що зберігається в кеші або **`false`** в іншому випадку. Якщо в `flags` встановлена ​​константа, **`Memcached::GET_EXTENDED`**, повертається масив, що містить значення та токен CAS замість єдиного значення. Метод [Memcached::getResultCode()](memcached.getresultcode.html) повертає **`Memcached::RES_NOTFOUND`** якщо переданий ключ не існує.

### список змін

| Версия | Описание |
| --- | --- |
| PECL memcached 3.0.0 | Видалено параметр `&cas_token`. Замість нього додано параметр `flags`, в який можна передати значення **`Memcached::GET_EXTENDED`** для того, щоб було повернуто токен CAS. |

### Приклади

**Приклад #1 Приклад використання **Memcached::get()****

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->set('foo', 100);
var_dump($m->get('foo'));
?>
```

Результат виконання цього прикладу:

```
int(100)
```

**Приклад #2 Приклад використання **Memcached::get()****

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

if (!($ip = $m->get('ip_block'))) {
    if ($m->getResultCode() == Memcached::RES_NOTFOUND) {
        $ip = array();
        $m->set('ip_block', $ip);
    } else {
        /* log error */
        /* ...       */
    }
}
?>
```

### Дивіться також

-   [Memcached::getByKey()](memcached.getbykey.html) - Отримує запис із певного сервера
-   [Memcached::getMulti()](memcached.getmulti.html) - Отримує кілька записів
-   [Memcached::getDelayed()](memcached.getdelayed.html) - Запитує кілька записів
