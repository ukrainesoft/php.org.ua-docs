Повертає опис помилки

-   [« yazerrno](function.yaz-errno.html)
    
-   [yazесresult »](function.yaz-es-result.html)
    
-   [PHP Manual](index.html)
    
-   [Функции YAZ](ref.yaz.html)
    
-   Повертає опис помилки
    

# yazerror

(PHP 4> = 4.0.1, PECL yaz> = 0.9.0)

yazerror — Повертає опис помилки

### Опис

```methodsynopsis
yaz_error(resource $id): string
```

**yazerror()** повертає текстове повідомлення англійською мовою, що відповідає останньому номеру помилки, поверненому [yazerrno()](function.yaz-errno.html)

### Список параметрів

`id`

Ресурс підключення, що повертається [yazconnect()](function.yaz-connect.html)

### Значення, що повертаються

Повертає текстове повідомлення про помилку для сервера (останній запит) з ідентифікатором `id`. Якщо остання операція пройшла успішно, повертається порожній рядок.

### Дивіться також

-   [yazerrno()](function.yaz-errno.html) - Повертає номер помилки
-   [yazaddinfo()](function.yaz-addinfo.html) - Повертає додаткову інформацію у разі виникнення помилки