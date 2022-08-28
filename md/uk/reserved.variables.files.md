Змінні файли, завантажені за HTTP

-   [« $\_POST](reserved.variables.post.html)
    
-   [$\_REQUEST »](reserved.variables.request.html)
    
-   [PHP Manual](index.html)
    
-   [Предопределённые переменные](reserved.variables.html)
    
-   Змінні файли, завантажені за HTTP
    

# FILES

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

FILES — Змінні файли, завантажені за HTTP

### Опис

Асоціативний масив (array) елементів, завантажених у поточний скрипт через метод HTTP POST. Структура цього масиву описана у розділі [Загрузка файлов методом POST](features.file-upload.post-method.html)

### Примітки

> **Зауваження**
> 
> Це 'суперглобальна' або автоматична глобальна змінна. Це просто означає, що вона доступна у всіх контекстах скрипту. Немає необхідності виконувати **global $variable;** для доступу до неї всередині методу чи функції.

### Дивіться також

-   [move\_uploaded\_file()](function.move-uploaded-file.html) - Переміщує завантажений файл у нове місце
-   [Загрузка файлов на сервер](features.file-upload.html)