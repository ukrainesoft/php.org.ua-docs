- [« Користувальницькі обробники сесії](session.customhandler.md)
- [Безпека сесій »](session.security.md)

- [PHP Manual](index.md)
- [Сесії](book.session.md)
- Відстеження прогресу завантаження файлів за допомогою сесій

# Відстеження прогресу завантаження файлів за допомогою сесій

PHP може відслідковувати прогрес завантаження окремих файлів при включеній
опції
[session.upload_progress.enabled](session.configuration.md#ini.session.upload-progress.enabled).
Ця інформація не дуже корисна для запиту, безпосередньо
закачує файл, однак, протягом даного завантаження програма може
посилати POST-запити на окрему сторінку (наприклад, за допомогою XHR)
для перевірки статусу.

Прогрес закачування буде доступний у суперглобальній змінній `$_SESSION`
під час виконання завантаження, а також під час надсилання POST-запитом
змінної з ім'ям, рівним значенню опції
[session.upload_progress.name](session.configuration.md#ini.session.upload-progress.name).
Як тільки PHP виявить такий POST-запит, він створить масив у
`$_SESSION`, ключем якого буде конкатенація значень опцій
[session.upload_progress.prefix](session.configuration.md#ini.session.upload-progress.prefix)
і
[session.upload_progress.name](session.configuration.md#ini.session.upload-progress.name).
Ключ зазвичай можна отримати прочитавши ці опції, тобто:

` <?php$key = ini_get("session.upload_progress.prefix") . $_POST[ini_get("session.upload_progress.name")];var_dump($_SESSION[$key]);?> `

Також можливо *скасувати* файл, що завантажується в даний момент, встановивши
ключ `$_SESSION[$key]["cancel_upload"]` у значення **`true`**. При
завантаження декількох файлів за один раз, ця дія скасує тільки
поточний файл, що завантажується, і всі наступні за ним, але не видалить вже
успішно завантажені на той час файли. Якщо закачування було скасовано
цим способом, то елемент з ключем `error` у масиві `$_FILES` буде
встановлений у **`UPLOAD_ERR_EXTENSION`**.

Опції [session.upload_progress.freq](session.configuration.md#ini.session.upload-progress.freq)
і
[session.upload_progress.min_freq](session.configuration.md#ini.session.upload-progress.min-freq)
контролюють частоту оновлення інформації про прогрес завантаження. При
розумних значеннях цих двох налаштувань, накладні витрати даної функції
практично невідчутні.

**Приклад #1 Приклад**

Приклад структури масиву прогресу завантаження.

```htmlcode
<form action="upload.php" method="POST" enctype="multipart/form-data">
<input type="hidden" name="<?php echo ini_get("session.upload_progress.name"); ?>" value="123" />
<input type="file" name="file1" />
<input type="file" name="file2" />
<input type="submit" />
</form>
````

Дані в сесії виглядатимуть приблизно так:

` <?php$_SESSION["upload_progress_123"] = array( "start_time" => 1234567890,   // Время начала запроса "content_length" => 57343257, // Длина содержимого POST "bytes_processed" => 453489,  // Количество полученных и обработанных байт "done" => false,              // true при завершении обработки POST, успешно или нет "files" => array(  0 => array(   "field_name" => "file1",       // Имя поля <input/>   / / Следующие 3 элемента аналогичны соответствующим элементам массива $_FILES   "name" => "foo.avi",   "tmp_name" => "/tmp/phpxxxxxx",   "error" => 0,   "done" => true,                // True , если обработчик POST закончил обработку данного файла   "start_time" => 1234567890,    // Время начала обработки этого файла   "bytes_processed" => 57343250, // Число полученных и обработанных байт этого файла  ),  // И ещё один файл, загрузка которого ещё не закінчена в том ж запиті  1 => array(  "field_name" => "file2",   "name" => "bar.avi",   "tmp_name" =>    fa lse,  "start_time" => 1234567899,  "bytes_processed" => 54554,  ), )); `

**Увага**

Для успішної роботи цієї функції необхідно відключити буферизацію
запит на веб-сервер. Інакше PHP побачить завантаження файлу лише коли
завантаження повністю завершиться. Сервери, такі як Nginx,
буферизують великі запити.

**Застереження**

Інформація про прогрес завантаження записується в сесію до того, як буде
запущений якийсь скрипт. Тому зміна імені сесії за допомогою
[ini_set()](function.ini-set.md) або
[session_name()](function.session-name.md) видасть сесію без
інформації про прогрес завантаження.
