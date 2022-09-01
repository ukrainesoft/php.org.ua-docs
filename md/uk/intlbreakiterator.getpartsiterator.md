---
navigation:
  - intlbreakiterator.getlocale.html: '« IntlBreakIterator::getLocale'
  - intlbreakiterator.gettext.html: 'IntlBreakIterator::getText »'
  - index.html: PHP Manual
  - class.intlbreakiterator.html: IntlBreakIterator
title: 'IntlBreakIterator::getPartsIterator'
---
# IntlBreakIterator::getPartsIterator

(PHP 5> = 5.5.0, PHP 7, PHP 8)

IntlBreakIterator::getPartsIterator — Створює ітератор для переміщення фрагментів між кордонами

### Опис

```methodsynopsis
public IntlBreakIterator::getPartsIterator(string $type = IntlPartsIterator::KEY_SEQUENTIAL): IntlPartsIterator
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`type`

Необов'язковий тип ключа. Можливі значення:

-   **`IntlPartsIterator::KEY_SEQUENTIAL`** - Значення за замовчуванням. Послідовно збільшує цілі числа, які використовуються як ключ.
-   **`IntlPartsIterator::KEY_LEFT`** - Байтове зміщення зліва від поточної частини, що використовується як ключ.
-   **`IntlPartsIterator::KEY_RIGHT`** - Байтове зміщення праворуч від поточної частини, яка використовується як ключ.

### Значення, що повертаються
