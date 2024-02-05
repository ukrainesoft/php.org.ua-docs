---
navigation:
  - quickhashstringinthash.add.md: '« QuickHashStringIntHash::add'
  - quickhashstringinthash.delete.md: 'QuickHashStringIntHash::delete »'
  - index.md: PHP Manual
  - class.quickhashstringinthash.md: QuickHashStringIntHash
title: 'QuickHashStringIntHash::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashStringIntHash::\_\_construct

(No version information available, might only be in Git)

QuickHashStringIntHash::\_\_construct — Створює новий об'єкт QuickHashStringIntHash

### Опис

```methodsynopsis
public QuickHashStringIntHash::__construct(int $size, int $options = 0)
```

Конструктор створює новий об'єкт [QuickHashStringIntHash](class.quickhashstringinthash.md). Розмір - це кількість списків, які потрібно створити. Чим більше списків, тим менше буде колізій. Також підтримуються налаштування.

### Список параметрів

`size`

Кількість списків, які потрібно налаштувати. Число, яке ви передасте, буде автоматично округлено до наступного ступеня 2. Воно також автоматично обмежується від `64`до`4194304`

`options`

Ви можете передати такі параметри: константу **`QuickHashStringIntHash::CHECK_FOR_DUPES`**, яка гарантує, що в хеш не будуть додані дублікати та константу **`QuickHashStringIntHash::DO_NOT_USE_ZEND_ALLOC`**, щоб не використовувати внутрішній менеджер PHP.

### Значення, що повертаються

Повертає новий об'єкт [QuickHashStringIntHash](class.quickhashstringinthash.md)

### Приклади

**Приклад #1 Приклад використання** QuickHashStringIntHash::\_\_construct()\*\*\*\*

```php
<?php
var_dump( new QuickHashStringIntHash( 1024 ) );
var_dump( new QuickHashStringIntHash( 1024, QuickHashStringIntHash::CHECK_FOR_DUPES ) );
?>
```
