---
navigation:
  - function.ibase-rollback-ret.md: « ibase\_rollback\_ret
  - function.ibase-server-info.md: ibase\_server\_info »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_rollback
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_rollback

(PHP 5, PHP 7 < 7.4.0)

ibase\_rollback - Відкочує транзакцію

### Опис

```methodsynopsis
ibase_rollback(resource $link_or_trans_identifier = null): bool
```

Відкочує транзакцію.

### Список параметрів

`link_or_trans_identifier`

Якщо це не викликає аргументу, ця функція відкочує транзакцію за промовчанням для посилання за промовчанням. Якщо аргумент є ідентифікатором з'єднання, транзакція за промовчанням для відповідного з'єднання буде скасована. Якщо аргумент є ідентифікатором транзакції, відповідну транзакцію буде скасовано.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
