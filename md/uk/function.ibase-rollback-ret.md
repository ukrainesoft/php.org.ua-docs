---
navigation:
  - function.ibase-restore.md: « ibase\_restore
  - function.ibase-rollback.md: ibase\_rollback »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_rollback\_ret
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_rollback\_ret

(PHP 5, PHP 7 < 7.4.0)

ibase\_rollback\_ret - Відкочує транзакцію, не закриваючи її

### Опис

```methodsynopsis
ibase_rollback_ret(resource $link_or_trans_identifier = null): bool
```

Відкочує транзакцію, не закриваючи її.

### Список параметрів

`link_or_trans_identifier`

Якщо це не викликає аргументу, ця функція відкочує транзакцію за промовчанням для посилання за промовчанням. Якщо аргумент є ідентифікатором з'єднання, транзакція за промовчанням для відповідного з'єднання буде скасована. Якщо аргумент є ідентифікатором транзакції, відповідну транзакцію буде скасовано. Контекст транзакції буде збережено, тому вирази, які виконуються з цієї транзакції, не будуть визнані недійсними.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
