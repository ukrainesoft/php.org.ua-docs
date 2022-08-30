Додає змінну в кеш користувача, тільки якщо змінна ще не існує в кеші

-   [« wincachescachememinfo](function.wincache-scache-meminfo.html)
    
-   [wincacheucachecas »](function.wincache-ucache-cas.html)
    
-   [PHP Manual](index.html)
    
-   [Функции WinCache](ref.wincache.html)
    
-   Додає змінну в кеш користувача, тільки якщо змінна ще не існує в кеші
    

# wincacheucacheadd

(PECL wincache >= 1.1.0)

wincacheucacheadd — Додає змінну в кеш користувача, тільки якщо змінна ще не існує в кеші

### Опис

```methodsynopsis
wincache_ucache_add(string $key, mixed $value, int $ttl = 0): bool
```

```methodsynopsis
wincache_ucache_add(array $values, mixed $unused = NULL, int $ttl = 0): bool
```

Додає змінну в кеш користувача, тільки якщо ця змінна ще не існує в кеші. Додана змінна залишається в кеші користувача, поки не закінчиться термін її дії або вона не буде видалена за допомогою функцій [wincacheucachedelete()](function.wincache-ucache-delete.html) або [wincacheucacheclear()](function.wincache-ucache-clear.html)

### Список параметрів

`key`

Зберігає змінну з використанням цього імені `key`. Якщо змінна з таким самим `key` вже існує, завершиться помилкою та поверне **`false`**. . `key` чутливий до регістру. Щоб перевизначити значення, навіть якщо `key` вже існує, використовуйте функцію [wincacheucacheset()](function.wincache-ucache-set.html). . `key` також може приймати масив пар ім'я => значення, де імена будуть використовуватися як ключі. Це можна використовувати для додавання кількох значень до кешу за одну операцію, що дозволяє уникнути стану гонки.

`value`

Значення змінної, яку потрібно зберегти . `Value` підтримує всі типи даних, крім таких ресурсів, як дескриптори файлів. Параметр ігнорується, якщо першим аргументом масив. Загальне керівництво – передати **`null`** в якості `value` при використанні масиву `key`. Якщо `value` є об'єктом або масивом, що містить об'єкти, об'єкти будуть серіалізовані. Докладніше про серіалізацію об'єктів дивіться в описі [sleep()](language.oop5.magic.html#object.sleep)

`values`

Асоціативний масив ключів та значень.

`ttl`

Час, протягом якого змінна знаходиться у кеші, за секунди. Після того, як значення, вказане в `ttl` буде передано, збережена змінна буде видалена з кеша. Параметр набуває значення за замовчуванням `0`, що означає, що змінна залишиться в кеші, доки вона не буде явно видалена за допомогою функцій [wincacheucachedelete()](function.wincache-ucache-delete.html) або [wincacheucacheclear()](function.wincache-ucache-clear.html)

### Значення, що повертаються

Якщо `key` є рядком, функція повертає **`true`** у разі успішного виконання та **`false`** у разі виникнення помилки.

Якщо `key` є масивом, функція повертає:

-   Якщо всі пари ім'я => значення масиву можуть бути встановлені, функція повертає порожній масив;
-   Якщо всі пари ім'я => значення в масиві не можуть бути встановлені, функція повертає **`false`**
-   Якщо деякі з них можуть бути встановлені, а інші - ні, функція повертає масив з парами name => value, які не вдалося додати в кеш користувача.

### Приклади

**Приклад #1 Приклад використання **wincacheucacheadd()** з `key` у вигляді рядка**

```php
<?php
$bar = 'BAR';
var_dump(wincache_ucache_add('foo', $bar));
var_dump(wincache_ucache_add('foo', $bar));
var_dump(wincache_ucache_get('foo'));
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
string(3) "BAR"
```

**Приклад #2 Приклад використання **wincacheucacheadd()** з `key` у вигляді масиву**

```php
<?php
$colors_array = array('green' => '5', 'Blue' => '6', 'yellow' => '7', 'cyan' => '8');
var_dump(wincache_ucache_add($colors_array));
var_dump(wincache_ucache_add($colors_array));
var_dump(wincache_ucache_get('Blue'));
?>
```

Результат виконання цього прикладу:

```
array(0) { }
array(4) {
  ["green"]=> int(-1)
  ["Blue"]=> int(-1)
  ["yellow"]=> int(-1)
  ["cyan"]=> int(-1)
}
string(1) "6"
```

### Дивіться також

-   [wincacheucacheset()](function.wincache-ucache-set.html) - Додає змінну в кеш користувача і перезаписує змінну, якщо вона вже існує в кеші
-   [wincacheucacheget()](function.wincache-ucache-get.html) - Отримує змінну, що зберігається в користувальницькому кеші
-   [wincacheucachedelete()](function.wincache-ucache-delete.html) - Видаляє змінні з користувальницького кешу
-   [wincacheucacheclear()](function.wincache-ucache-clear.html) - Видаляє весь вміст кешу користувача.
-   [wincacheucacheexists()](function.wincache-ucache-exists.html) - Перевіряє, чи існує змінна в кеші користувача
-   [wincacheucachememinfo()](function.wincache-ucache-meminfo.html) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincacheucacheinfo()](function.wincache-ucache-info.html) - Отримує інформацію про дані, що зберігаються в кеші користувача
-   [sleep()](language.oop5.magic.html#object.sleep)