---
navigation:
  - function.wincache-ucache-exists.html: « wincacheucacheexists
  - function.wincache-ucache-inc.html: wincacheucacheinc »
  - index.md: PHP Manual
  - ref.wincache.md: Функции WinCache
title: wincacheucacheget
---
# wincacheucacheget

(PECL wincache >= 1.1.0)

wincacheucacheget — Отримує змінну, що зберігається в кеші користувача.

### Опис

```methodsynopsis
wincache_ucache_get(mixed $key, bool &$success = ?): mixed
```

Отримує змінну, що зберігається в кеші користувача.

### Список параметрів

`key`

Параметр `key`, який використовувався для зберігання змінної в кеші . `key` чутливий до регістру . `key` може бути масивом ключів. У цьому випадку значення, що повертається, буде масивом значень кожного елемента в масиві `key`. Якщо повертається об'єкт або масив, що містить об'єкти, об'єкти будуть десеріалізовані. Детальніше про десеріалізацію об'єктів дивіться [wakeup()](language.oop5.magic.html#object.wakeup)

`success`

Буде встановлено значення **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Значення, що повертаються

Якщо параметр `key` є рядком, функція повертає значення змінної, що зберігається із цим ключем. Для параметра `success` буде встановлено значення **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

Якщо параметр `key` - це масив, параметр `success` завжди матиме значення **`true`**. Повернутий масив (пари ім'я => значення) міститиме лише ті пари ім'я => значення, для яких операція отримання в кеші користувача була успішною. Якщо жоден з ключів у масиві ключів не знаходить збігу в кеші користувача, буде повернутий порожній масив.

### Приклади

**Приклад #1 **wincacheucacheget()** з `key` у вигляді рядка**

```php
<?php
wincache_ucache_add('color', 'blue');
var_dump(wincache_ucache_get('color', $success));
var_dump($success);
?>
```

Результат виконання цього прикладу:

```
string(4) "blue"
bool(true)
```

**Приклад #2 **wincacheucacheget()** з `key` у вигляді масиву**

```php
<?php
$array1 = array('green' => '5', 'Blue' => '6', 'yellow' => '7', 'cyan' => '8');
wincache_ucache_set($array1);
$array2 = array('green', 'Blue', 'yellow', 'cyan');
var_dump(wincache_ucache_get($array2, $success));
var_dump($success);
?>
```

Результат виконання цього прикладу:

```
array(4) { ["green"]=> string(1) "5"
           ["Blue"]=> string(1) "6"
           ["yellow"]=> string(1) "7"
           ["cyan"]=> string(1) "8" }
bool(true)
```

### Дивіться також

-   [wincacheucacheadd()](function.wincache-ucache-add.html) - Додає змінну в кеш користувача, тільки якщо змінна ще не існує в кеші
-   [wincacheucacheset()](function.wincache-ucache-set.html) - Додає змінну в кеш користувача і перезаписує змінну, якщо вона вже існує в кеші
-   [wincacheucachedelete()](function.wincache-ucache-delete.html) - Видаляє змінні з користувальницького кешу
-   [wincacheucacheclear()](function.wincache-ucache-clear.html) - Видаляє весь вміст кешу користувача.
-   [wincacheucacheexists()](function.wincache-ucache-exists.html) - Перевіряє, чи існує змінна в кеші користувача
-   [wincacheucachememinfo()](function.wincache-ucache-meminfo.html) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincacheucacheinfo()](function.wincache-ucache-info.html) - Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wakeup()](language.oop5.magic.html#object.wakeup)
