---
navigation:
  - collator.setattribute.md: '« Collator::setAttribute'
  - collator.sortwithsortkeys.md: 'Collator::sortWithSortKeys »'
  - index.md: PHP Manual
  - class.collator.md: Collator
title: 'Collator::setStrength'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collator::setStrength

# collator\_set\_strength

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::setStrength -- collator\_set\_strength - Встановлює силу зіставлення

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Collator::setStrength(int $strength): bool
```

Процедурний стиль

```methodsynopsis
collator_set_strength(Collator $object, int $strength): bool
```

Служба сопоставления[» ICU](https://icu.unicode.org/) підтримує безліч рівнів порівняння (званих "Рівні", але також відомих як "Сила порівняння"). Наявність цих категорій дозволяє ICU сортувати рядки точно відповідно до місцевих угод. Однак, дозволяючи вибірково використовувати рівні, пошук рядка в тексті може виконуватися з різними умовами зіставлення.

1.  *Первинний рівень*: Зазвичай використовується для позначення відмінностей між основними символами (наприклад, "a" < "b"). Це найбільша різниця. Наприклад, словники розбиті на різні розділи за основним символом. Також називається силою `level 1`
    
2.  *Вторинний рівень*: Акценти в символах вважаються вторинними відмінностями (наприклад, as < as < at). Інші відмінності між літерами можна вважати вторинними, залежно від мови. Вторинна відмінність ігнорується, якщо є первинна відмінність десь у рядках. Також називається силою `level 2`
    
    > **Зауваження** :
    > 
    > Примітка: У деяких мовах (наприклад, датському) певні літери з діакритичними знаками є окремими базовими символами. Однак, у більшості мов, літера з наголосом має лише другорядну відмінність від версії цієї літери без наголосу.
    
3.  *Третічний рівень*: Відмінності у верхньому та нижньому регістрі символів розрізняються на третинному рівні (наприклад, «ao» < «Ao» < «aò»). Крім того, варіант літери відрізняється від базової форми на третинному рівні (наприклад, «a» та «𝒶»). Інший приклад - різниця між великою та маленькою Кана. Третинна відмінність ігнорується, якщо десь у рядках є первинна або вторинне відмінність. Також називається силою `level 3`
    
4.  *Четвертичний рівень*: Коли пунктуація ігнорується (див. Ігнорування розділових знаків) на рівнях 1-3, можна використовувати додатковий рівень для розрізнення слів з пунктуацією і без неї (наприклад, «ab» < «a-b» < «aB»). Ця різниця ігнорується, якщо є первинна, вторинна чи третинна різниця. Також називається силою `level 4`. Четвертинний рівень слід використовувати тільки в тому випадку, якщо потрібне ігнорування розділових знаків або при обробці японського тексту (дивіться Обробка хірагани).
    
5.  *Ідентичний рівень*: Коли всі рівні рівні рівні, ідентичний рівень використовується як тай-брейк. Значення кодових точок Unicode форми NFD кожного рядка порівнюються цьому рівні, про всяк випадок, якщо немає різниці рівнях 1-4. Наприклад, кантиляційні знаки івриту різняться лише цьому рівні. Цей рівень слід використовувати з обережністю, оскільки різниця лише у значеннях кодових точок між двома рядками є вкрай рідкісним явищем. Використання цього рівня істотно знижує продуктивність як інкрементного порівняння, так і для генерації ключа сортування (а також збільшує довжину ключа сортування). Також називається силою`level 5`
    

Наприклад, люди можуть ігнорувати акценти або ігнорувати акценти та регістр під час пошуку тексту. Майже всі символи розрізняються за першими трьома рівнями, тому в більшості мов значення за замовчуванням - третинний. Однак, якщо для параметра «Альтернативний» встановлено значення «Shifted», то четвертинну силу можна використовувати для розриву зв'язків між пробілами, пунктуацією та символами, які інакше були б проігноровані. Якщо потрібні дуже тонкі відмінності між символами, тоді можна використовувати Ідентичний рівень (наприклад, Ідентичний рівень розрізняє Mathematical Bold Small A та Mathematical Italic Small A.). Однак використання рівнів вище, ніж третинний, ідентична сила призводить до значно довших ключів сортування та зниження продуктивності порівняння рядків для рівних рядків.

### Список параметрів

`object`

Об'єкт [Collator](class.collator.md)

`strength`

Strength to set.

Допустимі значення:

-   **`Collator::PRIMARY`**
    
-   **`Collator::SECONDARY`**
    
-   **`Collator::TERTIARY`**
    
-   **`Collator::QUATERNARY`**
    
-   **`Collator::IDENTICAL`**
    
-   **`Collator::DEFAULT_STRENGTH`**
    

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** collator\_set\_strength()\*\*\*\*

```php
<?php
$arr  = array( 'aò', 'Ao', 'ao' );
$coll = collator_create( 'en_US' );

// Сортировка массива с использованием силы по умолчанию.
collator_sort( $coll, $arr );
var_export( $arr );

// Сортировка массива с использованием первичной силы.
collator_set_strength( $coll, Collator::PRIMARY );
collator_sort( $coll, $arr );
var_export( $arr );
?>
```

Результат виконання наведеного прикладу:

```
array (
  0 => 'ao',
  1 => 'Ao',
  2 => 'aò',
)
array (
  0 => 'aò',
  1 => 'Ao',
  2 => 'ao',
)
```

### Дивіться також

-   [Константи](class.collator.md#intl.collator-constants) [Collator](class.collator.md)
-   [collator\_get\_strength()](collator.getstrength.md) \- набуває поточної сили зіставлення
