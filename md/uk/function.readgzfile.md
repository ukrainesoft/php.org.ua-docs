Виводить вміст gz-файлу

-   [« inflateinit](function.inflate-init.html)
    
-   [zlibdecode »](function.zlib-decode.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Zlib](ref.zlib.html)
    
-   Виводить вміст gz-файлу
    

# readgzfile

(PHP 4, PHP 5, PHP 7, PHP 8)

readgzfile — Виводить вміст gz-файлу

### Опис

```methodsynopsis
readgzfile(string $filename, int $use_include_path = 0): int|false
```

Читає файл, розпаковує його та записує у стандартний висновок.

Може також використовуватись для читання файлу, який не має формат gzip; в цьому випадку **readgzfile()** безпосередньо читає з файлу без розпакування.

### Список параметрів

`filename`

Ім'я файлу. Цей файл буде відкритий і його вміст буде записано у стандартний висновок.

`use_include_path`

Ви можете використовувати цей необов'язковий параметр і встановити його в `1`, якщо необхідно, щоб пошук файлу також здійснювався в директоріях [includepath](ini.core.html#ini.include-path)

### Значення, що повертаються

Повертає кількість байтів у файлі (після розпакування) у разі успішного виконання або **`false`** у разі виникнення помилки

### Помилки

У разі невдалого завершення роботи генерується помилка рівня **`E_WARNING`**

### Дивіться також

-   [gzpassthru()](function.gzpassthru.html) - Виведення всіх даних з покажчика gz-файлу.
-   [gzfile()](function.gzfile.html) - Зчитує весь gz-файл у масив
-   [gzopen()](function.gzopen.html) - Відкрити gz-файл