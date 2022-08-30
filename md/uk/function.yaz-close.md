Закриває з'єднання YAZ

-   [« yazcclparse](function.yaz-ccl-parse.html)
    
-   [yazconnect »](function.yaz-connect.html)
    
-   [PHP Manual](index.html)
    
-   [Функции YAZ](ref.yaz.html)
    
-   Закриває з'єднання YAZ
    

# yazclose

(PHP 4> = 4.0.1, PECL yaz> = 0.9.0)

yazclose — Закриває з'єднання YAZ

### Опис

```methodsynopsis
yaz_close(resource $id): bool
```

Закриває з'єднання, яке визначається параметром `id`

> **Зауваження**
> 
> Функція закриє лише непостійні з'єднання, відкриті функцією [yazconnect()](function.yaz-connect.html) з параметром `persistent` встановленим у значення **`false`**

### Список параметрів

`id`

Дескриптор з'єднання, що повертається [yazconnect()](function.yaz-connect.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [yazconnect()](function.yaz-connect.html) - Готує з'єднання із сервером Z39.50