Отримує ключ сортування рядка

-   [« Collator::getLocale](collator.getlocale.html)
    
-   [Collator::getStrength »](collator.getstrength.html)
    
-   [PHP Manual](index.html)
    
-   [Collator](class.collator.html)
    
-   Отримує ключ сортування рядка
    

# Collator::getSortKey

# collatorgetsortkey

(PHP 5 >= 5.3.2, PHP 7, PHP 8, PECL intl >= 1.0.3)

Collator::getSortKey -- collatorgetsortkey — Отримує ключ сортування рядка

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Collator::getSortKey(string $string): string|false
```

Процедурний стиль

```methodsynopsis
collator_get_sort_key(Collator $object, string $string): string|false
```

Повертає ключ зіставлення для рядка. Ключі зіставлення можна порівнювати безпосередньо, а не рядки, хоча вони залежать від реалізації і можуть змінюватись в залежності від версії бібліотеки ICU. Ключі сортування зазвичай корисні лише в базах даних або в інших випадках, коли виклики функцій надзвичайно дорогі.

### Список параметрів

`object`

Об'єкт [Collator](class.collator.html)

`string`

Рядок, з якого створюється ключ.

### Значення, що повертаються

Повертає ключ зіставлення для рядка або **`false`** у разі виникнення помилки.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.html). Використовуйте [оператор ===](language.operators.comparison.html) для перевірки значення, яке повертається цією функцією.

### Приклади

**Приклад #1 Приклад використання **collatorgetsortkey()****

```php
<?php
$s1 = 'Hello';

$coll = collator_create('en_US');
$res  = collator_get_sort_key($coll, $s1);

echo bin2hex($res);
?>
```

Результатом виконання цього прикладу буде щось подібне:

3832404046010901dc08

### Дивіться також

-   [collatorsort()](collator.sort.html) - Сортує масив із використанням зазначеного засобу сортування
-   [collatorsortwithsortkeys()](collator.sortwithsortkeys.html) - Сортує масив з використанням зазначеного Collator та ключів сортування