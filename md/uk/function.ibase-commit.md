Фіксує транзакцію

-   [« ibasecommitret](function.ibase-commit-ret.html)
    
-   [ibaseconnect »](function.ibase-connect.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Фіксує транзакцію
    

# ibasecommit

(PHP 5, PHP 7 < 7.4.0)

ibasecommit - Фіксує транзакцію

### Опис

```methodsynopsis
ibase_commit(resource $link_or_trans_identifier = null): bool
```

Фіксує транзакцію.

### Список параметрів

`link_or_trans_identifier`

Якщо викликається без аргументу, функція фіксує транзакцію за промовчанням для посилання за промовчанням. Якщо аргумент є ідентифікатором з'єднання, транзакція за промовчанням відповідного з'єднання буде зафіксована. Якщо аргумент є ідентифікатором транзакції, відповідна транзакція буде зафіксована.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.