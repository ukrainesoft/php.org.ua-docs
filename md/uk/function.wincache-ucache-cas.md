Порівнює змінну зі старим значенням і надає їй нове значення

-   [« wincacheucacheadd](function.wincache-ucache-add.html)
    
-   [wincacheucacheclear »](function.wincache-ucache-clear.html)
    
-   [PHP Manual](index.md)
    
-   [Функции WinCache](ref.wincache.md)
    
-   Порівнює змінну зі старим значенням і надає їй нове значення
    

# wincacheucachecas

(PECL wincache >= 1.1.0)

wincacheucachecas — Порівнює змінну зі старим значенням і надає їй нове значення

### Опис

```methodsynopsis
wincache_ucache_cas(string $key, int $old_value, int $new_value): bool
```

Порівнює змінну, пов'язану з `key` з `old_value` і, якщо вона збігається, надає їй `new_value`

### Список параметрів

`key`

`key`, який використовувався для збереження змінної в кеш . `key` чутливий до регістру.

`old_value`

Старе значення змінної, яку вказує `key` в кеші користувача. Значення має бути типу `long`, інакше функція поверне **`false`**

`new_value`

Нове значення, яке буде надано покажчику змінної `key`якщо знайдено збіг. Значення має бути типу `long`, інакше функція поверне **`false`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **wincacheucachecas()****

```php
<?php
wincache_ucache_set('counter', 2922);
var_dump(wincache_ucache_cas('counter', 2922, 1));
var_dump(wincache_ucache_get('counter'));
?>
```

Результат виконання цього прикладу:

```
bool(true)
int(1)
```

### Дивіться також

-   [wincacheucacheinc()](function.wincache-ucache-inc.html) - Збільшує значення, пов'язане з ключем
-   [wincacheucachedec()](function.wincache-ucache-dec.html) - Зменшує значення, пов'язане з ключем