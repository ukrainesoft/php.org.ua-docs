---
navigation:
  - function.wincache-ucache-exists.md: « wincache\_ucache\_exists
  - function.wincache-ucache-inc.md: wincache\_ucache\_inc »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_ucache\_get
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_ucache\_get

(PECL wincache >= 1.1.0)

wincache\_ucache\_get — Отримує змінну, що зберігається в кеші користувача.

### Опис

```methodsynopsis
wincache_ucache_get(mixed $key, bool &$success = ?): mixed
```

Отримує змінну, що зберігається в кеші користувача.

### Список параметрів

`key`

Параметр`key`, який використовувався для зберігання змінної в кеші . `key`чувствителен к регистру`key` може бути масивом ключів. У цьому випадку значення, що повертається, буде масивом значень кожного елемента в масиві `key`. Якщо повертається об'єкт або масив, що містить об'єкти, об'єкти будуть десеріалізовані. Детальніше про десеріалізацію об'єктів дивіться [\_\_wakeup()](language.oop5.magic.md#object.wakeup)

`success`

Будет установлено значение\*\*`true`\*\* у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Значення, що повертаються

Якщо параметр `key` є рядком, функція повертає значення змінної, що зберігається із цим ключем. Для параметра `success`будет установлено значение\*\*`true`\*\* у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

Якщо параметр `key` - це масив, параметр `success` завжди матиме значення **`true`**. . Повернутий масив (пари ім'я => значення) міститиме лише ті пари ім'я => значення, для яких операція отримання в кеші користувача була успішною. Якщо жоден з ключів у масиві ключів не знаходить збігу в кеші користувача, буде повернутий порожній масив.

### Приклади

**Пример #1**wincache\_ucache\_get()**с`key` у вигляді рядка**

```php
<?php
wincache_ucache_add('color', 'blue');
var_dump(wincache_ucache_get('color', $success));
var_dump($success);
?>
```

Результат виконання наведеного прикладу:

```
string(4) "blue"
bool(true)
```

**Пример #2**wincache\_ucache\_get()**с`key` у вигляді масиву**

```php
<?php
$array1 = array('green' => '5', 'Blue' => '6', 'yellow' => '7', 'cyan' => '8');
wincache_ucache_set($array1);
$array2 = array('green', 'Blue', 'yellow', 'cyan');
var_dump(wincache_ucache_get($array2, $success));
var_dump($success);
?>
```

Результат виконання наведеного прикладу:

```
array(4) { ["green"]=> string(1) "5"
           ["Blue"]=> string(1) "6"
           ["yellow"]=> string(1) "7"
           ["cyan"]=> string(1) "8" }
bool(true)
```

### Дивіться також

-   [wincache\_ucache\_add()](function.wincache-ucache-add.md) \- Додає змінну в кеш користувача, тільки якщо змінна ще не існує в кеші
-   [wincache\_ucache\_set()](function.wincache-ucache-set.md) \- Додає змінну в кеш користувача і перезаписує змінну, якщо вона вже існує в кеші
-   [wincache\_ucache\_delete()](function.wincache-ucache-delete.md) \- Видаляє змінні з користувальницького кешу
-   [wincache\_ucache\_clear()](function.wincache-ucache-clear.md) \- Видаляє весь вміст користувальницького кешу
-   [wincache\_ucache\_exists()](function.wincache-ucache-exists.md) \- Перевіряє, чи існує змінна в кеші користувача
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.md) \- Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.md) \- Отримує інформацію про дані, що зберігаються в кеші користувача
-   [\_\_wakeup()](language.oop5.magic.md#object.wakeup)
