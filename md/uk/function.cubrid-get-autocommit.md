Повертає налаштування авто-комміту для з'єднання

-   [« cubrid\_free\_result](function.cubrid-free-result.html)
    
-   [cubrid\_get\_charset »](function.cubrid-get-charset.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Повертає налаштування авто-комміту для з'єднання
    

# cubridgetautocommit

(PECL CUBRID >= 8.4.0)

cubridgetautocommit — Повертає налаштування автокомміту для з'єднання

### Опис

```methodsynopsis
cubrid_get_autocommit(resource $conn_identifier): bool
```

Функція **cubridgetautocommit()** використовується для визначення, чи дозволено в цьому з'єднанні авто-комміт чи ні.

Для CUBRID 8.4.0, авто-коміт транзакцій заборонено за замовчуванням.

Для CUBRID 8.4.0, авто-коміт транзакцій дозволено за замовчуванням.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

### Значення, що повертаються

**`true`**, якщо автокоміт дозволено.

**`false`**, якщо автокоміт заборонено.

**`null`** у разі виникнення помилки.

### Дивіться також

-   [cubrid\_set\_autocommit()](function.cubrid-set-autocommit.html) - Встановлює режим авто-комміту для з'єднання
-   [cubrid\_commit()](function.cubrid-commit.html) - підтвердження транзакції