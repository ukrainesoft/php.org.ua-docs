---
navigation:
  - function.wincache-ucache-get.md: « wincacheucacheget
  - function.wincache-ucache-info.md: wincacheucacheinfo »
  - index.md: PHP Manual
  - ref.wincache.md: Функции WinCache
title: wincacheucacheinc
---
# wincacheucacheinc

(PECL wincache >= 1.1.0)

wincacheucacheinc — Збільшує значення ключа

### Опис

```methodsynopsis
wincache_ucache_inc(string $key, int $inc_by = 1, bool &$success = ?): mixed
```

Збільшує значення, пов'язане з `key` на 1 або як зазначено в `inc_by`

### Список параметрів

`key`

`key`, який використовувався для збереження змінної в кеш . `key` чутливий до регістру.

`inc_by`

Значення, на яке має бути збільшена змінна, пов'язана з `key`. Якщо аргумент є числом з плаваючою точкою, він буде усічений до найближчого цілого числа. Змінна, пов'язана з `key`, повинна мати тип `long`, інакше функція завершиться помилкою та поверне **`false`**

`success`

Буде встановлено значення **`true`** у разі успішного виконання та **`false`** у разі виникнення помилки.

### Значення, що повертаються

Повертає збільшене значення у разі успішного виконання та **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **wincacheucacheinc()****

```php
<?php
wincache_ucache_set('counter', 1);
var_dump(wincache_ucache_inc('counter', 2921, $success));
var_dump($success);
?>
```

Результат виконання цього прикладу:

```
int(2922)
bool(true)
```

### Дивіться також

-   [wincacheucachedec()](function.wincache-ucache-dec.md) - Зменшує значення, пов'язане з ключем
-   [wincacheucachecas()](function.wincache-ucache-cas.md) - Порівнює змінну зі старим значенням та надає їй нове значення
