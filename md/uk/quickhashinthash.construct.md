---
navigation:
  - quickhashinthash.add.md: '« QuickHashIntHash::add'
  - quickhashinthash.delete.md: 'QuickHashIntHash::delete »'
  - index.md: PHP Manual
  - class.quickhashinthash.md: QuickHashIntHash
title: 'QuickHashIntHash::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntHash::\_\_construct

(PECL quickhash >= Unknown)

QuickHashIntHash::\_\_construct — Створює об'єкт QuickHashIntHash

### Опис

```methodsynopsis
public QuickHashIntHash::__construct(int $size, int $options = ?)
```

Конструктор створює об'єкт [QuickHashIntHash](class.quickhashinthash.md). Розмір – це кількість списків, які потрібно створити. Чим більше списків, тим менше буде колізій. Також підтримуються налаштування.

### Список параметрів

`size`

Кількість списків, які потрібно налаштувати. Число, яке ви передасте, буде автоматично округлено до наступного ступеня 2. Воно також автоматично обмежується від `64`до`4194304`

`options`

Ви можете використовувати такі варіанти: \*\*`QuickHashIntHash::CHECK_FOR_DUPES`\*\*що гарантує, що в хеш не будуть додані дублюючі записи; **`QuickHashIntHash::DO_NOT_USE_ZEND_ALLOC`** щоб не використовувати внутрішній менеджер пам'яті PHP, а також одну з констант: **`QuickHashIntHash::HASHER_NO_HASH`** **`QuickHashIntHash::HASHER_JENKINS1`** або **`QuickHashIntHash::HASHER_JENKINS2`**. Останні три параметри визначають, який алгоритм хешування використати. Усі параметри можна поєднувати за допомогою побітових операторів.

### Значення, що повертаються

Повертає новий об'єкт [QuickHashIntHash](class.quickhashinthash.md)

### Приклади

**Приклад #1 Приклад використання** QuickHashIntHash::\_\_construct()\*\*\*\*

```php
<?php
var_dump( new QuickHashIntHash( 1024 ) );
var_dump( new QuickHashIntHash( 1024, QuickHashIntHash::CHECK_FOR_DUPES ) );
var_dump(
    new QuickHashIntHash(
        1024,
        QuickHashIntHash::DO_NOT_USE_ZEND_ALLOC | QuickHashIntHash::HASHER_JENKINS2
    )
);
?>
```
