Збільшує значення, пов'язане з ключем

-   [« wincache\_ucache\_get](function.wincache-ucache-get.html)
    
-   [wincache\_ucache\_info »](function.wincache-ucache-info.html)
    
-   [PHP Manual](index.html)
    
-   [Функции WinCache](ref.wincache.html)
    
-   Збільшує значення, пов'язане з ключем
    

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

-   [wincache\_ucache\_dec()](function.wincache-ucache-dec.html) - Зменшує значення, пов'язане з ключем
-   [wincache\_ucache\_cas()](function.wincache-ucache-cas.html) - Порівнює змінну зі старим значенням та надає їй нове значення