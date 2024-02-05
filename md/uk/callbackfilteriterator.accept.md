---
navigation:
  - class.callbackfilteriterator.md: « CallbackFilterIterator
  - callbackfilteriterator.construct.md: 'CallbackFilterIterator::\_\_construct »'
  - index.md: PHP Manual
  - class.callbackfilteriterator.md: CallbackFilterIterator
title: 'CallbackFilterIterator::accept'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CallbackFilterIterator::accept

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

CallbackFilterIterator::accept — Викликає callback-функцію і передає їй як аргументи поточне значення, поточний ключ та внутрішній покажчик

### Опис

```methodsynopsis
public CallbackFilterIterator::accept(): bool
```

Викликає callback-функцію та передає їй як аргументи поточне значення, поточний ключ та внутрішній покажчик.

Callback-функція має повертати **`true`**, якщо поточний елемент пройшов фільтр, **`false`** в іншому випадку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо поточний елемент пройшов фільтр, **`false`** в іншому випадку.

### Дивіться також

-   [Приклади використання CallbackFilterIterator](class.callbackfilteriterator.md#callbackfilteriterator.examples)
-   [CallbackFilterIterator::\_\_construct()](callbackfilteriterator.construct.md) \- Створює фільтруючий ітератор на основі іншого ітератора
