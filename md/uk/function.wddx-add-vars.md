Додати змінні в пакет WDDX із зазначеним ідентифікатором

-   [« Функції WDDX](ref.wddx.md)
    
-   [wddxdeserialize »](function.wddx-deserialize.html)
    
-   [PHP Manual](index.md)
    
-   [Функції WDDX](ref.wddx.md)
    
-   Додати змінні в пакет WDDX із зазначеним ідентифікатором
    

# wddxaddvars

(PHP 4, PHP 5, PHP 7)

wddxaddvars — Додати змінні до пакету WDDX із зазначеним ідентифікатором

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 7.4.0.

### Опис

```methodsynopsis
wddx_add_vars(resource $packet_id, mixed $var_name, mixed ...$var_names): bool
```

Серіалізує передані змінні та додає результат до цього пакету.

### Список параметрів

Функція приймає змінну кількість параметрів.

`packet_id`

Пакет WDDX, що повертається [wddxpacketstart()](function.wddx-packet-start.html)

`var_name`

Може бути або рядком, що означає змінну, або масивом, що містить рядки з іменами змінних або інші масиви і т.д.

`var_names`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.