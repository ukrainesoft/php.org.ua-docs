Відкочує транзакцію

-   [« ibaserollbackret](function.ibase-rollback-ret.html)
    
-   [ibaseserverinfo »](function.ibase-server-info.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Firebird/InterBase](ref.ibase.md)
    
-   Відкочує транзакцію
    

# ibaserollback

(PHP 5, PHP 7 < 7.4.0)

ibaserollback - Відкочує транзакцію

### Опис

```methodsynopsis
ibase_rollback(resource $link_or_trans_identifier = null): bool
```

Відкочує транзакцію.

### Список параметрів

`link_or_trans_identifier`

Якщо це не викликає аргументу, ця функція відкочує транзакцію за промовчанням для посилання за промовчанням. Якщо аргумент є ідентифікатором з'єднання, транзакція за промовчанням для відповідного з'єднання буде скасована. Якщо аргумент є ідентифікатором транзакції, відповідну транзакцію буде скасовано.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.