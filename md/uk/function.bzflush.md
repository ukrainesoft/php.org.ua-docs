Нічого не робить

-   [« bzerrstr](function.bzerrstr.html)
    
-   [bzopen »](function.bzopen.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Bzip2](ref.bzip2.html)
    
-   Нічого не робить
    

# bzflush

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

bzflush - Нічого не робить

### Опис

```methodsynopsis
bzflush(resource $bz): bool
```

Функція повинна примусово записувати всі буферизовані дані bzip2 у файл, який посилається покажчик `bz`але в libbz2 реалізована як нульова функція і тому нічого не робить.

### Список параметрів

`bz`

Вказівник на файл. Повинен бути коректним і вказувати на файл, успішно відкритий [bzopen()](function.bzopen.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [bzread()](function.bzread.html) - Бінарно-безпечне читання файлу bzip2
-   [bzwrite()](function.bzwrite.html) - Бінарно-безпечний запис bzip2 файлу