---
navigation:
  - function.ibase-close.html: « ibaseclose
  - function.ibase-commit.html: ibasecommit »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibasecommitret
---
# ibasecommitret

(PHP 5, PHP 7 < 7.4.0)

ibasecommitret - Фіксує транзакцію, не закриваючи її

### Опис

```methodsynopsis
ibase_commit_ret(resource $link_or_trans_identifier = null): bool
```

Фіксує транзакцію, не закриваючи її.

### Список параметрів

`link_or_trans_identifier`

Якщо викликається без аргументу, функція фіксує транзакцію за промовчанням для посилання за промовчанням. Якщо аргумент є ідентифікатором з'єднання, транзакція за промовчанням відповідного з'єднання буде зафіксована. Якщо аргумент є ідентифікатором транзакції, відповідна транзакція буде зафіксована. Контекст транзакції буде збережено, тому оператори, виконані з цієї транзакції, не будуть визнані недійсними.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
