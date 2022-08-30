Змінні файли, завантажені за HTTP

-   [POST](reserved.variables.post.md)
    
-   [REQUEST »](reserved.variables.request.md)
    
-   [PHP Manual](index.md)
    
-   [Зумовлені змінні](reserved.variables.md)
    
-   Змінні файли, завантажені за HTTP
    

# FILES

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

FILES — Змінні файли, завантажені за HTTP

### Опис

Асоціативний масив (array) елементів, завантажених у поточний скрипт через метод HTTP POST. Структура цього масиву описана у розділі [Завантаження файлів методом POST](features.file-upload.post-method.html)

### Примітки

> **Зауваження**
> 
> Це 'суперглобальна' або автоматична глобальна змінна. Це просто означає, що вона доступна у всіх контекстах скрипту. Немає необхідності виконувати **global $variable;** для доступу до неї всередині методу чи функції.

### Дивіться також

-   [moveuploadedfile()](function.move-uploaded-file.html) - Переміщує завантажений файл у нове місце
-   [Загрузка файлов на сервер](features.file-upload.html)