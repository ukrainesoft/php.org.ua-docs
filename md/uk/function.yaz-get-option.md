Повертає значення параметра для підключення

-   [« yazес](function.yaz-es.html)
    
-   [yazhits »](function.yaz-hits.html)
    
-   [PHP Manual](index.md)
    
-   [Функции YAZ](ref.yaz.md)
    
-   Повертає значення параметра для підключення
    

# yazgetoption

(PECL yaz >= 0.9.0)

yazgetoption — Повертає значення параметра для підключення

### Опис

```methodsynopsis
yaz_get_option(resource $id, string $name): string
```

Повертає значення параметра, вказаного в `name`

### Список параметрів

`id`

Ресурс підключення, що повертається [yazconnect()](function.yaz-connect.html)

`name`

Назву параметра.

### Значення, що повертаються

Повертає значення вказаної опції або порожній рядок, якщо опцію не було встановлено.

### Дивіться також

-   Опис [yazsetoption()](function.yaz-set-option.html) - Встановлює параметри з'єднання для перегляду доступних параметрів