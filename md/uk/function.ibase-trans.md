Починає транзакцію

-   [« ibase\_set\_event\_handler](function.ibase-set-event-handler.html)
    
-   [ibase\_wait\_event »](function.ibase-wait-event.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Починає транзакцію
    

# ibasetrans

(PHP 5, PHP 7 < 7.4.0)

ibasetrans — Починає транзакцію

### Опис

```methodsynopsis
ibase_trans(int $trans_args = ?, resource $link_identifier = ?): resource
```

```methodsynopsis
ibase_trans(resource $link_identifier = ?, int $trans_args = ?): resource
```

Починає транзакцію.

> **Зауваження**
> 
> Перший виклик **ibasetrans()** не поверне транзакцію стандартного з'єднання. Усі транзакції, запущені за допомогою **ibasetrans()**, будуть скасовані в кінці скрипту, якщо вони не були зафіксовані, або будуть скасовані за допомогою [ibase\_commit()](function.ibase-commit.html) або [ibase\_rollback()](function.ibase-rollback.html)

> **Зауваження**
> 
> Ця функція приймає кілька аргументів `trans_args` і `link_identifier`. Це дозволяє виконувати транзакції через кілька з'єднань із базою даних, які фіксуються з використанням алгоритму двоетапної фіксації. Це означає, що ви можете розраховувати на те, що оновлення будуть успішними в кожній базі даних або завершаться помилкою в кожній базі даних. Це НЕ означає, що ви можете використовувати таблиці різних баз даних в одному запиті!
> 
> Якщо ви використовуєте транзакції у кількох базах даних, вам потрібно буде вказати як `link_id`, так і `transaction_id` у викликах [ibase\_query()](function.ibase-query.html) і [ibase\_prepare()](function.ibase-prepare.html)

### Список параметрів

`trans_args`

`trans_args` може бути комбінацією **`IBASE_READ`** **`IBASE_WRITE`** **`IBASE_COMMITTED`** **`IBASE_CONSISTENCY`** **`IBASE_CONCURRENCY`** **`IBASE_REC_VERSION`** **`IBASE_REC_NO_VERSION`** **`IBASE_WAIT`** і **`IBASE_NOWAIT`**

`link_identifier`

Ідентифікатор посилання InterBase. Якщо не вказано, передбачається останнє відкрите посилання.

### Значення, що повертаються

Повертає дескриптор транзакції або **`false`** у разі виникнення помилки.