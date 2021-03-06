- [« ibase_restore](function.ibase-restore.md)
- [ibase_rollback »](function.ibase-rollback.md)

- [PHP Manual](index.md)
- [Функції Firebird/InterBase](ref.ibase.md)
- Відкочує транзакцію, не закриваючи її

# ibase_rollback_ret

(PHP 5, PHP 7 \< 7.4.0)

ibase_rollback_ret - Відкочує транзакцію, не закриваючи її

### Опис

**ibase_rollback_ret**(resource `$link_or_trans_identifier` =
**`null`**): bool

Відкочує транзакцію, не закриваючи її.

### Список параметрів

`link_or_trans_identifier`
Якщо викликається без аргументу, ця функція відкочує транзакцію по
за промовчанням для посилання за промовчанням. Якщо аргумент є
ідентифікатором з'єднання, транзакція за замовчуванням для відповідного
з'єднання буде скасовано. Якщо аргумент є ідентифікатором
транзакції, відповідну транзакцію буде скасовано. Контекст
транзакції буде збережено, тому вирази, що виконуються з цієї
транзакції, що не будуть визнані недійсними.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.
