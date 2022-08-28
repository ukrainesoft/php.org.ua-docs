Повертає опис помилки

-   [« yaz\_errno](function.yaz-errno.html)
    
-   [yaz\_es\_result »](function.yaz-es-result.html)
    
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

**yazerror()** повертає текстове повідомлення англійською мовою, що відповідає останньому номеру помилки, поверненому [yaz\_errno()](function.yaz-errno.html)

### Список параметрів

`id`

Ресурс підключення, що повертається [yaz\_connect()](function.yaz-connect.html)

### Значення, що повертаються

Повертає текстове повідомлення про помилку для сервера (останній запит) з ідентифікатором `id`. Якщо остання операція пройшла успішно, повертається порожній рядок.

### Дивіться також

-   [yaz\_errno()](function.yaz-errno.html) - Повертає номер помилки
-   [yaz\_addinfo()](function.yaz-addinfo.html) - Повертає додаткову інформацію у разі виникнення помилки