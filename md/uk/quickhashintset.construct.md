---
navigation:
  - quickhashintset.add.md: '« QuickHashIntSet::add'
  - quickhashintset.delete.md: 'QuickHashIntSet::delete »'
  - index.md: PHP Manual
  - class.quickhashintset.md: QuickHashIntSet
title: 'QuickHashIntSet::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntSet::\_\_construct

(PECL quickhash >= Unknown)

QuickHashIntSet::\_\_construct — Створює новий об'єкт QuickHashIntSet

### Опис

```methodsynopsis
public QuickHashIntSet::__construct(int $size, int $options = ?)
```

Конструктор створює новий об'єкт [QuickHashIntSet](class.quickhashintset.md). Розмір - це кількість списків, які потрібно створити. Чим більше списків, тим менше буде колізій. Також підтримуються налаштування.

### Список параметрів

`size`

Кількість списків, які потрібно налаштувати. Число, яке ви передасте, буде автоматично округлено до наступного ступеня 2. Воно також автоматично обмежується від `4`до`4194304`

`options`

Ви можете передати такі параметри: константу \*\*`QuickHashIntSet::CHECK_FOR_DUPES`\*\*яка гарантує, що до набору не будуть додані дублікати; Константу **`QuickHashIntSet::DO_NOT_USE_ZEND_ALLOC`**, щоб не використовувати внутрішній менеджер пам'яті PHP, а також одну з констант **`QuickHashIntSet::HASHER_NO_HASH`** **`QuickHashIntSet::HASHER_JENKINS1`** або **`QuickHashIntSet::HASHER_JENKINS2`**. Останні три параметри визначають, який алгоритм хешування використати. Усі параметри можна поєднувати за допомогою побітових операторів.

### Значення, що повертаються

Повертає новий об'єкт [QuickHashIntSet](class.quickhashintset.md)

### Приклади

**Приклад #1 Приклад використання** QuickHashIntSet::\_\_construct()\*\*\*\*

```php
<?php
var_dump( new QuickHashIntSet( 1024 ) );
var_dump( new QuickHashIntSet( 1024, QuickHashIntSet::CHECK_FOR_DUPES ) );
var_dump(
    new QuickHashIntSet(
        1024,
        QuickHashIntSet::DO_NOT_USE_ZEND_ALLOC | QuickHashIntSet::HASHER_JENKINS2
    )
);
?>
```
