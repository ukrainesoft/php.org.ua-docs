---
navigation:
  - collator.getlocale.md: '« Collator::getLocale'
  - collator.getstrength.md: 'Collator::getStrength »'
  - index.md: PHP Manual
  - class.collator.md: Collator
title: 'Collator::getSortKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collator::getSortKey

# collator\_get\_sort\_key

(PHP 5 >= 5.3.2, PHP 7, PHP 8, PECL intl >= 1.0.3)

Collator::getSortKey -- collator\_get\_sort\_key — Отримує ключ сортування рядка

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

Об'єкт [Collator](class.collator.md)

`string`

Рядок, з якого створюється ключ.

### Значення, що повертаються

Повертає ключ зіставлення для рядка або \*\*`false`\*\*в случае возникновения ошибки.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Приклади

**Приклад #1 Приклад використання** collator\_get\_sort\_key()\*\*\*\*

```php
<?php
$s1 = 'Hello';

$coll = collator_create('en_US');
$res  = collator_get_sort_key($coll, $s1);

echo bin2hex($res);
?>
```

Висновок наведеного прикладу буде схожим на:

3832404046010901dc08

### Дивіться також

-   [collator\_sort()](collator.sort.md) \- Сортує масив із використанням зазначеного засобу сортування
-   [collator\_sort\_with\_sort\_keys()](collator.sortwithsortkeys.md) \- Сортує масив з використанням зазначеного Collator та ключів сортування
