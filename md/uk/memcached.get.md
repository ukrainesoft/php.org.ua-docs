---
navigation:
  - memcached.flush.md: '« Memcached::flush'
  - memcached.getallkeys.md: 'Memcached::getAllKeys »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::get

(PECL memcached >= 0.1.0)

Memcached::get — Отримання запису

### Опис

```methodsynopsis
public Memcached::get(string $key, ?callable $cache_cb = null, int $get_flags = 0): mixed
```

**Memcached::get()** повертає запис, який раніше був збережений під ключом `key`. Якщо елемент не знайдено і для параметра `get_flags`задано\*\*`Memcached::GET_EXTENDED`\*\*, вона також поверне значення токена CAS для цього запису. Зверніться до документації щодо [Memcached::cas()](memcached.cas.md) для отримання інформації про використання CAS токена . [Читання за допомогою кешуючих callback-функцій](memcached.callbacks.md) може бути використано за допомогою параметра `cache_cb`

### Список параметрів

`key`

Ключ одержуваного запису.

`cache_cb`

Функція зворотного виклику для читання, що кешується, або **`null`**

`get_flags`

Прапори, що визначають результат, що повертається. Якщо задана константа **`Memcached::GET_EXTENDED`**, функція також поверне CAS токен.

### Значення, що повертаються

Возвращает значение хранимое в кеше или\*\*`false`\*\* в іншому випадку. Якщо в `get_flags`установлена константа,**`Memcached::GET_EXTENDED`**, повертається масив, що містить значення та токен CAS замість єдиного значення. Метод [Memcached::getResultCode()](memcached.getresultcode.md) повертає **`Memcached::RES_NOTFOUND`** якщо переданий ключ не існує.

### список змін

| Версия | Опис |
| --- | --- |
| PECL memcached 3.0.0 | Видалено параметр `&cas_token`. . Замість нього додано параметр `get_flags`, в який можна передати значення **`Memcached::GET_EXTENDED`** для того, щоб було повернуто токен CAS. |

### Приклади

**Пример #1 Пример использования**Memcached::get()\*\*\*\*

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->set('foo', 100);
var_dump($m->get('foo'));
?>
```

Результат виконання наведеного прикладу:

```
int(100)
```

**Пример #2 Пример использования**Memcached::get()\*\*\*\*

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

if (!($ip = $m->get('ip_block'))) {
    if ($m->getResultCode() == Memcached::RES_NOTFOUND) {
        $ip = array();
        $m->set('ip_block', $ip);
    } else {
        /* log error */
        /* ...       */
    }
}
?>
```

### Дивіться також

-   [Memcached::getByKey()](memcached.getbykey.md) \- Отримує запис із певного сервера
-   [Memcached::getMulti()](memcached.getmulti.md) \- Отримує кілька записів
-   [Memcached::getDelayed()](memcached.getdelayed.md) \- Запитує кілька записів
