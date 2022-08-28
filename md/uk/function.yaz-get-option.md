Повертає значення параметра для підключення

-   [« yaz\_es](function.yaz-es.html)
    
-   [yaz\_hits »](function.yaz-hits.html)
    
-   [PHP Manual](index.html)
    
-   [Функции YAZ](ref.yaz.html)
    
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

Ресурс підключення, що повертається [yaz\_connect()](function.yaz-connect.html)

`name`

Назву параметра.

### Значення, що повертаються

Повертає значення вказаної опції або порожній рядок, якщо опцію не було встановлено.

### Дивіться також

-   Опис [yaz\_set\_option()](function.yaz-set-option.html) - Встановлює параметри з'єднання для перегляду доступних параметрів