Видаляє вже певну константу

-   [« runkit7constantredefine](function.runkit7-constant-redefine.html)
    
-   [runkit7functionadd »](function.runkit7-function-add.html)
    
-   [PHP Manual](index.html)
    
-   [Функції runkit7](ref.runkit7.html)
    
-   Видаляє вже певну константу
    

# runkit7constantremove

(PECL runkit7> = Unknown)

runkit7constantremove — Видаляє вже певну константу

### Опис

```methodsynopsis
runkit7_constant_remove(string $constant_name): bool
```

### Список параметрів

`constant_name`

Константа, яку потрібно видалити. Або ім'я світової константи, або `classname::constname` видалення константи класу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [define()](function.define.html) - визначає іменовану константу
-   [runkit7constantadd()](function.runkit7-constant-add.html) - Аналогічний define(), але також дозволяє визначити константу класу
-   [runkit7constantredefine()](function.runkit7-constant-redefine.html) - Перевизначає вже певну константу