---
navigation:
  - function.ibase-set-event-handler.md: « ibase\_set\_event\_handler
  - function.ibase-wait-event.md: ibase\_wait\_event »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_trans
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_trans

(PHP 5, PHP 7 < 7.4.0)

ibase\_trans — Починає транзакцію

### Опис

```methodsynopsis
ibase_trans(int $trans_args = ?, resource $link_identifier = ?): resource
```

```methodsynopsis
ibase_trans(resource $link_identifier = ?, int $trans_args = ?): resource
```

Починає транзакцію.

> **Зауваження** :
> 
> Перший виклик **ibase\_trans()** не поверне транзакцію стандартного з'єднання. Усі транзакції, запущені за допомогою **ibase\_trans()**, будуть скасовані в кінці скрипту, якщо вони не були зафіксовані, або будуть скасовані за допомогою [ibase\_commit()](function.ibase-commit.md) або [ibase\_rollback()](function.ibase-rollback.md)

> **Зауваження** :
> 
> Ця функція приймає кілька аргументів `trans_args`и`link_identifier`. Це дозволяє виконувати транзакції через кілька з'єднань із базою даних, які фіксуються з використанням алгоритму двоетапної фіксації. Це означає, що ви можете розраховувати на те, що оновлення будуть успішними в кожній базі даних або завершаться помилкою в кожній базі даних. Це НЕ означає, що ви можете використовувати таблиці різних баз даних в одному запиті!
> 
> Якщо ви використовуєте транзакції у кількох базах даних, вам потрібно буде вказати як `link_id`, так и`transaction_id` у викликах [ibase\_query()](function.ibase-query.md) і [ibase\_prepare()](function.ibase-prepare.md)

### Список параметрів

`trans_args`

`trans_args` може бути комбінацією **`IBASE_READ`** **`IBASE_WRITE`** **`IBASE_COMMITTED`** **`IBASE_CONSISTENCY`** **`IBASE_CONCURRENCY`** **`IBASE_REC_VERSION`** **`IBASE_REC_NO_VERSION`** **`IBASE_WAIT`**и**`IBASE_NOWAIT`**

`link_identifier`

Ідентифікатор посилання InterBase. Якщо не вказано, передбачається останнє відкрите посилання.

### Значення, що повертаються

Повертає дескриптор транзакції або \*\*`false`\*\*в случае возникновения ошибки.
