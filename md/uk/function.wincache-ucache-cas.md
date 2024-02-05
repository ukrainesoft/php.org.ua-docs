---
navigation:
  - function.wincache-ucache-add.md: « wincache\_ucache\_add
  - function.wincache-ucache-clear.md: wincache\_ucache\_clear »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_ucache\_cas
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_ucache\_cas

(PECL wincache >= 1.1.0)

wincache\_ucache\_cas — Порівнює змінну зі старим значенням і надає їй нове значення

### Опис

```methodsynopsis
wincache_ucache_cas(string $key, int $old_value, int $new_value): bool
```

Сравнивает переменную, связанную с`key`с`old_value` і, якщо вона збігається, надає їй `new_value`

### Список параметрів

`key`

`key`, який використовувався для збереження змінної в кеш . `key`чувствителен к регистру.

`old_value`

Старе значення змінної, яку вказує `key` в кеші користувача. Значення має бути типу `long`, інакше функція поверне **`false`**

`new_value`

Нове значення, яке буде надано покажчику змінної `key`якщо знайдено збіг. Значення має бути типу `long`, інакше функція поверне **`false`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**wincache\_ucache\_cas()\*\*\*\*

```php
<?php
wincache_ucache_set('counter', 2922);
var_dump(wincache_ucache_cas('counter', 2922, 1));
var_dump(wincache_ucache_get('counter'));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
int(1)
```

### Дивіться також

-   [wincache\_ucache\_inc()](function.wincache-ucache-inc.md) \- Збільшує значення, пов'язане з ключем
-   [wincache\_ucache\_dec()](function.wincache-ucache-dec.md) \- Зменшує значення, пов'язане з ключем
