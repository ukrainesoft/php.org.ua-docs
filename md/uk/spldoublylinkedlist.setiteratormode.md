---
navigation:
  - spldoublylinkedlist.serialize.md: '« SplDoublyLinkedList::serialize'
  - spldoublylinkedlist.shift.md: 'SplDoublyLinkedList::shift »'
  - index.md: PHP Manual
  - class.spldoublylinkedlist.md: SplDoublyLinkedList
title: 'SplDoublyLinkedList::setIteratorMode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplDoublyLinkedList::setIteratorMode

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplDoublyLinkedList::setIteratorMode — Встановлює режим ітерації

### Опис

```methodsynopsis
public SplDoublyLinkedList::setIteratorMode(int $mode): int
```

### Список параметрів

`mode`

Існують два ортогональні набори режимів, які можуть бути встановлені:

-   Напрямок ітерації (одне з двох):
    -   **`SplDoublyLinkedList::IT_MODE_LIFO`**(Стек)
    -   **`SplDoublyLinkedList::IT_MODE_FIFO`**(Черга)
-   Поведінка ітератора (одне із двох):
    -   **`SplDoublyLinkedList::IT_MODE_DELETE`**(Елементи видаляються ітератором)
    -   **`SplDoublyLinkedList::IT_MODE_KEEP`**(Ітератор обходить елементи, не видаляючи їх)

По умолчанию используется режим:**`SplDoublyLinkedList::IT_MODE_FIFO`** **`SplDoublyLinkedList::IT_MODE_KEEP`**

**Увага**

Направление итерации нельзя изменить для классов[SplStack](class.splstack.md) і [SplQueue](class.splqueue.md), воно завжди **`SplDoublyLinkedList::IT_MODE_FIFO`**. Спроба змінити його призведе до викидання винятків [RuntimeException](class.runtimeexception.md)

### Значення, що повертаються

Повертає різні режими та прапори, що впливають на ітерацію.
