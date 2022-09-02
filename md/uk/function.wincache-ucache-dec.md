---
navigation:
  - function.wincache-ucache-clear.md: « wincacheucacheclear
  - function.wincache-ucache-delete.md: wincacheucachedelete »
  - index.md: PHP Manual
  - ref.wincache.md: Функции WinCache
title: wincacheucachedec
---
# wincacheucachedec

(PECL wincache >= 1.1.0)

wincacheucachedec — Зменшує значення ключа.

### Опис

```methodsynopsis
wincache_ucache_dec(string $key, int $dec_by = 1, bool &$success = ?): mixed
```

Зменшує значення, пов'язане з `key` на 1 або як зазначено в `dec_by`

### Список параметрів

`key`

`key`, який використовувався для збереження змінної в кеш . `key` чутливий до регістру.

`dec_by`

Значення, на яке має бути зменшена змінна, пов'язана з `key`. Якщо аргумент є числом з плаваючою точкою, він буде усічений до найближчого цілого числа. Змінна, пов'язана з `key`, повинна мати тип `long`, інакше функція завершиться помилкою та поверне **`false`**

`success`

Буде встановлено значення **`true`** у разі успішного виконання та **`false`** у разі виникнення помилки.

### Значення, що повертаються

Повертає зменшене значення у разі успішного виконання та **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **wincacheucachedec()****

```php
<?php
wincache_ucache_set('counter', 1);
var_dump(wincache_ucache_dec('counter', 2923, $success));
var_dump($success);
?>
```

Результат виконання цього прикладу:

```
int(2922)
bool(true)
```

### Дивіться також

-   [wincacheucacheinc()](function.wincache-ucache-inc.md) - Збільшує значення, пов'язане з ключем
-   [wincacheucachecas()](function.wincache-ucache-cas.md) - Порівнює змінну зі старим значенням та надає їй нове значення
