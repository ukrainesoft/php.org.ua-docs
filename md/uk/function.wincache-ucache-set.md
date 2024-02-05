---
navigation:
  - function.wincache-ucache-meminfo.md: « wincache\_ucache\_meminfo
  - function.wincache-unlock.md: wincache\_unlock »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_ucache\_set
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_ucache\_set

(PECL wincache >= 1.1.0)

wincache\_ucache\_set — Додає змінну в кеш користувача і перезаписує змінну, якщо вона вже існує в кеші

### Опис

```methodsynopsis
wincache_ucache_set(mixed $key, mixed $value, int $ttl = 0): bool
```

```methodsynopsis
wincache_ucache_set(array $values, mixed $unused = NULL, int $ttl = 0): bool
```

Додає змінну в кеш користувача. Замінює змінну, якщо вона вже існує у кеші. Додана або оновлена ​​змінна залишається в кеші користувача, поки не закінчиться термін її дії або вона не буде видалена за допомогою функцій [wincache\_ucache\_delete()](function.wincache-ucache-delete.md) або [wincache\_ucache\_clear()](function.wincache-ucache-clear.md)

### Список параметрів

`key`

Зберігає змінну з використанням цього імені `key`Если переменная с таким же`key` вже існує, функція перезапише попереднє значення новим . `key`чувствителен к регистру`key` також може приймати масив пар ім'я => значення, де імена будуть використовуватися як ключі. Це можна використовувати для додавання кількох значень до кешу за одну операцію, що дозволяє уникнути стану гонки.

`value`

Значення змінної, яку потрібно зберегти . `Value` підтримує всі типи даних, крім таких ресурсів, як дескриптори файлів. Параметр ігнорується, якщо першим аргументом масив. Загальне керівництво – передати **`null`** в якості `value`при использовании массива`key`. Якщо `value` є об'єктом або масивом, що містить об'єкти, об'єкти будуть серіалізовані. Докладніше про серіалізацію об'єктів дивіться в описі [\_\_sleep()](language.oop5.magic.md#object.sleep)

`values`

Асоціативний масив ключів та значень.

`ttl`

Час, протягом якого змінна знаходиться у кеші, за секунди. Після того, як значення, вказане в `ttl` буде передано, збережена змінна буде видалена з кеша. Параметр набуває значення за замовчуванням , что означает, что переменная останется в кеше, пока она не будет явно удалена с помощью функций[wincache\_ucache\_delete()](function.wincache-ucache-delete.md) або [wincache\_ucache\_clear()](function.wincache-ucache-clear.md)

### Значення, що повертаються

Якщо `key` є рядком, функція повертає **`true`** у разі успішного виконання та \*\*`false`\*\*в случае возникновения ошибки.

Якщо `key` є масивом, функція повертає:

-   Якщо всі пари ім'я => значення масиву можуть бути встановлені, функція повертає порожній масив;
-   Якщо всі пари ім'я => значення в масиві не можуть бути встановлені, функція повертає **`false`**
-   Якщо деякі з них можуть бути встановлені, а інші - ні, функція повертає масив з парами name => value, які не вдалося додати в кеш користувача.

### Приклади

**Приклад #1 Приклад використання** wincache\_ucache\_set()**с`key` у вигляді рядка**

```php
<?php
$bar = 'BAR';
var_dump(wincache_ucache_set('foo', $bar));
var_dump(wincache_ucache_get('foo'));
$bar1 = 'BAR1';
var_dump(wincache_ucache_set('foo', $bar1));
var_dump(wincache_ucache_get('foo'));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
string(3) "BAR"
bool(true)
string(3) "BAR1"
```

**Приклад #2 Приклад використання** wincache\_ucache\_set()**с`key` у вигляді масиву**

```php
<?php
$colors_array = array('green' => '5', 'Blue' => '6', 'yellow' => '7', 'cyan' => '8');
var_dump(wincache_ucache_set($colors_array));
var_dump(wincache_ucache_set($colors_array));
var_dump(wincache_ucache_get('Blue'));
?>
```

Результат виконання наведеного прикладу:

```
array(0) {}
array(0) {}
string(1) "6"
```

### Дивіться також

-   [wincache\_ucache\_add()](function.wincache-ucache-add.md) \- Додає змінну в кеш користувача, тільки якщо змінна ще не існує в кеші
-   [wincache\_ucache\_get()](function.wincache-ucache-get.md) \- Отримує змінну, що зберігається в користувальницькому кеші
-   [wincache\_ucache\_delete()](function.wincache-ucache-delete.md) \- Видаляє змінні з користувальницького кешу
-   [wincache\_ucache\_clear()](function.wincache-ucache-clear.md) \- Видаляє весь вміст користувальницького кешу
-   [wincache\_ucache\_exists()](function.wincache-ucache-exists.md) \- Перевіряє, чи існує змінна в кеші користувача
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.md) \- Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.md) \- Отримує інформацію про дані, що зберігаються в кеші користувача
-   [\_\_sleep()](language.oop5.magic.md#object.sleep)
