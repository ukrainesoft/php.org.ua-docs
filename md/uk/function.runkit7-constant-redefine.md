Перевизначає вже певну константу

-   [« runkit7constantadd](function.runkit7-constant-add.html)
    
-   [runkit7constantremove »](function.runkit7-constant-remove.html)
    
-   [PHP Manual](index.html)
    
-   [Функції runkit7](ref.runkit7.html)
    
-   Перевизначає вже певну константу
    

# runkit7constantredefine

(PECL runkit7> = Unknown)

runkit7constantredefine - Перевизначає вже певну константу

### Опис

```methodsynopsis
runkit7_constant_redefine(string $constant_name, mixed $value, int $new_visibility = ?): bool
```

### Список параметрів

`constant_name`

Константа, яку потрібно перевизначити. Або ім'я світової константи, або `classname::constname` для перевизначення константи класу.

`value`

Значення, яке присвоюється константі.

`new_visibility`

Нова видимість константи для констант класу. За промовчанням без змін. Одна з констант **`RUNKIT7_ACC_*`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [runkit7constantadd()](function.runkit7-constant-add.html) - Аналогічний define(), але також дозволяє визначити константу класу
-   [runkit7constantremove()](function.runkit7-constant-remove.html) - Видаляє вже певну константу