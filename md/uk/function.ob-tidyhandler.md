Функція зворотного дзвінка obstart для відновлення буфера

-   [« Tidy](ref.tidy.md)
    
-   [tidyaccesscount »](function.tidy-access-count.html)
    
-   [PHP Manual](index.md)
    
-   [Tidy](ref.tidy.md)
    
-   Функція зворотного дзвінка obstart для відновлення буфера
    

# проtidyhandler

(PHP 5, PHP 7, PHP 8)

проtidyhandler — Функція зворотного дзвінка obstart для відновлення буфера

### Опис

```methodsynopsis
ob_tidyhandler(string $input, int $mode = ?): string
```

Функція зворотного дзвінка [проstart()](function.ob-start.html) на відновлення буфера.

### Список параметрів

`input`

Буфер.

`mode`

Режим буфера

### Значення, що повертаються

Повертає видозмінений буфер.

### Приклади

**Приклад #1 Приклад використання **проtidyhandler()****

```php
<?php
ob_start('ob_tidyhandler');

echo '<p>test</i>';
?>
```

Результат виконання цього прикладу:

```
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 3.2//EN">
<html>
<head>
<title></title>
</head>
<body>
<p>test</p>
</body>
</html>
```

### Дивіться також

-   [проstart()](function.ob-start.html) - Включення буферизації виводу