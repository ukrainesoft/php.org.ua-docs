---
navigation:
  - intlbreakiterator.getlocale.md: '« IntlBreakIterator::getLocale'
  - intlbreakiterator.gettext.md: 'IntlBreakIterator::getText »'
  - index.md: PHP Manual
  - class.intlbreakiterator.md: IntlBreakIterator
title: 'IntlBreakIterator::getPartsIterator'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlBreakIterator::getPartsIterator

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

IntlBreakIterator::getPartsIterator — Створює ітератор для переміщення фрагментів між кордонами

### Опис

```methodsynopsis
public IntlBreakIterator::getPartsIterator(string $type = IntlPartsIterator::KEY_SEQUENTIAL): IntlPartsIterator
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`type`

Необов'язковий тип ключа. Можливі значення:

-   \*\*`IntlPartsIterator::KEY_SEQUENTIAL`\*\*- Значення за замовчуванням. Послідовно збільшує цілі числа, які використовуються як ключ.
-   \*\*`IntlPartsIterator::KEY_LEFT`\*\*- Байтове зміщення зліва від поточної частини, що використовується як ключ.
-   \*\*`IntlPartsIterator::KEY_RIGHT`\*\*- Байтове зміщення праворуч від поточної частини, яка використовується як ключ.

### Значення, що повертаються
