---
navigation:
  - function.ibase-commit-ret.md: « ibase\_commit\_ret
  - function.ibase-connect.md: ibase\_connect »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_commit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_commit

(PHP 5, PHP 7 < 7.4.0)

ibase\_commit - Фіксує транзакцію

### Опис

```methodsynopsis
ibase_commit(resource $link_or_trans_identifier = null): bool
```

Фіксує транзакцію.

### Список параметрів

`link_or_trans_identifier`

Якщо викликається без аргументу, функція фіксує транзакцію за промовчанням для посилання за промовчанням. Якщо аргумент є ідентифікатором з'єднання, транзакція за промовчанням відповідного з'єднання буде зафіксована. Якщо аргумент є ідентифікатором транзакції, відповідна транзакція буде зафіксована.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
