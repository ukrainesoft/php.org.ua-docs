Відстеження прогресу завантаження файлів за допомогою сесій

-   [« Пользовательские обработчики сессии](session.customhandler.html)
    
-   [Безопасность сессий »](session.security.html)
    
-   [PHP Manual](index.html)
    
-   [Сессии](book.session.html)
    
-   Відстеження прогресу завантаження файлів за допомогою сесій
    

# Відстеження прогресу завантаження файлів за допомогою сесій

PHP може відслідковувати прогрес завантаження окремих файлів при включеній опції [session.upload\_progress.enabled](session.configuration.html#ini.session.upload-progress.enabled). Ця інформація не дуже корисна для запиту, що безпосередньо закачує файл, однак, протягом даного завантаження програма може надсилати POST-запити на окрему сторінку (наприклад, за допомогою XHR) для перевірки статусу.

Прогрес закачування буде доступний у суперглобальній змінній [$\_SESSION](reserved.variables.session.html) під час виконання завантаження, а також при відправці POST-запитом змінної з ім'ям, що дорівнює значенню опції [session.upload\_progress.name](session.configuration.html#ini.session.upload-progress.name). Як тільки PHP виявить такий POST-запит, він створить масив у [$\_SESSION](reserved.variables.session.html), ключем якого буде конкатенація значень опцій [session.upload\_progress.prefix](session.configuration.html#ini.session.upload-progress.prefix) і [session.upload\_progress.name](session.configuration.html#ini.session.upload-progress.name). Ключ зазвичай можна отримати прочитавши ці опції, тобто:

```php
<?php
$key = ini_get("session.upload_progress.prefix") . $_POST[ini_get("session.upload_progress.name")];
var_dump($_SESSION[$key]);
?>
```

Також можливо *скасувати* файл, що завантажується в даний момент, встановивши ключ `$_SESSION[$key]["cancel_upload"]` на значення **`true`**. При завантаженні кількох файлів за один раз, ця дія скасує тільки поточний завантажуваний файл і всі наступні за ним, але не видалити вже завантажені до цього часу файли. Якщо закачування було скасовано цим способом, то елемент із ключем `error` у масиві [$\_FILES](reserved.variables.files.html) буде встановлений у **`UPLOAD_ERR_EXTENSION`**

Опції [session.upload\_progress.freq](session.configuration.html#ini.session.upload-progress.freq) і [session.upload\_progress.min\_freq](session.configuration.html#ini.session.upload-progress.min-freq) контролюють частоту оновлення інформації про прогрес завантаження. При розумних значеннях цих двох налаштувань накладні витрати цієї функції практично невідчутні.

**Приклад #1 Приклад**

Приклад структури масиву прогресу завантаження.

" value="123" />   

Дані у сесії виглядатимуть приблизно так:

```php
<?php
$_SESSION["upload_progress_123"] = array(
 "start_time" => 1234567890,   // Время начала запроса
 "content_length" => 57343257, // Длина содержимого POST
 "bytes_processed" => 453489,  // Количество полученных и обработанных байт
 "done" => false,              // true при завершении обработки POST, успешно или нет
 "files" => array(
  0 => array(
   "field_name" => "file1",       // Имя поля <input/>
   // Следующие 3 элемента аналогичны соответствующим элементам массива $_FILES
   "name" => "foo.avi",
   "tmp_name" => "/tmp/phpxxxxxx",
   "error" => 0,
   "done" => true,                // True, если обработчик POST закончил обработку данного файла
   "start_time" => 1234567890,    // Время начала обработки этого файла
   "bytes_processed" => 57343250, // Число полученных и обработанных байт этого файла
  ),
  // И ещё один файл, загрузка которого ещё не закончена в том же запросе
  1 => array(
   "field_name" => "file2",
   "name" => "bar.avi",
   "tmp_name" => NULL,
   "error" => 0,
   "done" => false,
   "start_time" => 1234567899,
   "bytes_processed" => 54554,
  ),
 )
);
```

**Увага**

Для успішної роботи цієї функції необхідно вимкнути буферизацію запиту веб-сервером. Інакше PHP побачить завантаження файлу тільки тоді, коли завантаження повністю завершиться. Сервери, такі як Nginx, буферизують великі запити.

**Застереження**

Інформація про прогрес завантаження записується в сесію до того, як буде запущено якийсь скрипт. Тому зміна імені сесії за допомогою [ini\_set()](function.ini-set.html) або [session\_name()](function.session-name.html) видасть сесію без інформації про прогрес завантаження.