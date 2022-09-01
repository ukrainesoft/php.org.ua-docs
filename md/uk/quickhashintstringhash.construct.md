---
navigation:
  - quickhashintstringhash.add.md: '« QuickHashIntStringHash::add'
  - quickhashintstringhash.delete.md: 'QuickHashIntStringHash::delete »'
  - index.md: PHP Manual
  - class.quickhashintstringhash.md: QuickHashIntStringHash
title: 'QuickHashIntStringHash::construct'
---
# QuickHashIntStringHash::construct

(PECL quickhash >= Unknown)

QuickHashIntStringHash::construct — Створює новий об'єкт QuickHashIntStringHash

### Опис

```methodsynopsis
public QuickHashIntStringHash::__construct(int $size, int $options = 0)
```

Конструктор створює новий об'єкт [QuickHashIntStringHash](class.quickhashintstringhash.md). Розмір – це кількість списків, які потрібно створити. Чим більше списків, тим менше буде колізій. Також підтримуються налаштування.

### Список параметрів

`size`

Кількість списків, які потрібно налаштувати. Число, яке ви передасте, буде автоматично округлено до наступного ступеня 2. Воно також автоматично обмежується від `64` до `4194304`

`options`

Ви можете використовувати такі варіанти: \*\*`QuickHashIntStringHash::CHECK_FOR_DUPES`\*\*що гарантує, що в хеш не будуть додані дублюючі записи; **`QuickHashIntStringHash::DO_NOT_USE_ZEND_ALLOC`** щоб не використовувати внутрішній менеджер пам'яті PHP, а також одну з констант: **`QuickHashIntStringHash::HASHER_NO_HASH`** **`QuickHashIntStringHash::HASHER_JENKINS1`** або **`QuickHashIntStringHash::HASHER_JENKINS2`**. Останні три параметри визначають, який алгоритм хешування використати. Усі параметри можна поєднувати за допомогою побітових операторів.

### Значення, що повертаються

Повертає новий об'єкт [QuickHashIntStringHash](class.quickhashintstringhash.md)

### Приклади

**Приклад #1 Приклад використання **QuickHashIntStringHash::construct()****

```php
<?php
var_dump( new QuickHashIntStringHash( 1024 ) );
var_dump( new QuickHashIntStringHash( 1024, QuickHashIntStringHash::CHECK_FOR_DUPES ) );
var_dump(
    new QuickHashIntStringHash(
        1024,
        QuickHashIntStringHash::DO_NOT_USE_ZEND_ALLOC | QuickHashIntStringHash::HASHER_JENKINS2
    )
);
?>
```
