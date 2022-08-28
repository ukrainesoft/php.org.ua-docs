Повертає номер помилки

-   [« yaz\_element](function.yaz-element.html)
    
-   [yaz\_error »](function.yaz-error.html)
    
-   [PHP Manual](index.html)
    
-   [Функции YAZ](ref.yaz.html)
    
-   Повертає номер помилки
    

# yazerrno

(PHP 4> = 4.0.1, PECL yaz> = 0.9.0)

yazerrno — Повертає номер помилки

### Опис

```methodsynopsis
yaz_errno(resource $id): int
```

Повертає номер помилки для сервера (останній запит) з ідентифікатором `id`

**yazerrno()** повинен викликатись після мережної активності для кожного сервера (після повернення [yaz\_wait()](function.yaz-wait.html)), щоб визначити успішне виконання або помилку останньої операції (наприклад, пошуку).

### Список параметрів

`id`

Ресурс підключення, що повертається [yaz\_connect()](function.yaz-connect.html)

### Значення, що повертаються

Повертає код помилки. Код помилки - це діагностичний код Z39.50 (зазвичай діагностика Bib-1), або код помилки на стороні клієнта, який генерується самим PHP/YAZ, наприклад "Connect failed", "Init Rejected" і т.д.

### Дивіться також

-   [yaz\_error()](function.yaz-error.html) - Повертає опис помилки
-   [yaz\_addinfo()](function.yaz-addinfo.html) - Повертає додаткову інформацію у разі виникнення помилки