---
navigation:
  - function.wincache-ucache-get.md: « wincache\_ucache\_get
  - function.wincache-ucache-info.md: wincache\_ucache\_info »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_ucache\_inc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_ucache\_inc

(PECL wincache >= 1.1.0)

wincache\_ucache\_inc — Збільшує значення ключа

### Опис

```methodsynopsis
wincache_ucache_inc(string $key, int $inc_by = 1, bool &$success = ?): mixed
```

Збільшує значення, пов'язане з `key` на 1 або як зазначено в `inc_by`

### Список параметрів

`key`

`key`, який використовувався для збереження змінної в кеш . `key`чувствителен к регистру.

`inc_by`

Значення, на яке має бути збільшена змінна, пов'язана з `key`. Якщо аргумент є числом з точкою, що плаває, він буде усічений до найближчого цілого числа. Змінна, пов'язана з `key`, должна иметь тип`long`, інакше функція завершиться помилкою та поверне **`false`**

`success`

Будет установлено значение\*\*`true`\*\* у разі успішного виконання та \*\*`false`\*\*в случае возникновения ошибки.

### Значення, що повертаються

Повертає збільшене значення у разі успішного виконання та \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**wincache\_ucache\_inc()\*\*\*\*

```php
<?php
wincache_ucache_set('counter', 1);
var_dump(wincache_ucache_inc('counter', 2921, $success));
var_dump($success);
?>
```

Результат виконання наведеного прикладу:

```
int(2922)
bool(true)
```

### Дивіться також

-   [wincache\_ucache\_dec()](function.wincache-ucache-dec.md) \- Зменшує значення, пов'язане з ключем
-   [wincache\_ucache\_cas()](function.wincache-ucache-cas.md) \- Порівнює змінну зі старим значенням та надає їй нове значення
