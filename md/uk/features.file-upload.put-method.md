---
navigation:
  - features.file-upload.multiple.md: « Завантаження кількох файлів
  - features.file-upload.errors.seealso.md: Дивіться також "
  - index.md: PHP Manual
  - features.file-upload.md: Завантаження файлів на сервер
title: Підтримка методу PUT
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Підтримка методу PUT

PHP підтримує завантаження файлів методом HTTP PUT, який використовується в деяких клієнтах для завантаження файлів на сервер. Запити PUT набагато простіше, ніж завантаження файлу з використанням POST-запитами і виглядають приблизно так:

PUT /path/filename.md HTTP/1.1

Такий виклик означає, що віддалений клієнт хотів би зберегти файл під ім'ям /path/filename.md у дереві каталогів вашого веб-сервера. Очевидно, що можливість клієнта автоматично перезаписувати файли веб-сервера за допомогою Apache або PHP не є добрим рішенням. Тому для того, щоб обробляти такі запити, вам необхідно вказати веб-сервер PHP-скрипт, якому ви довіряєте їх обробку. У веб-сервері Apache ви можете зробити це, використовуючи директиву *Script*. Як правило, ця директива розташована всередині блоку `<Directory>`или же внутри блока`<VirtualHost>`. Сам запис виглядає так:

```
Script PUT /put.php
```

Це вказує веб-серверу Apache на необхідність перенаправляти всі запити PUT, контекст яких збігається з контекстом, в якому ви розмістили цей рядок, у файл put.php. Передбачається, що файли з розширенням .php обробляються як PHP-скрипти, і що сам PHP встановлений і працює. Ресурсом призначення для всіх PUT-запитів на цей скрипт повинен бути сам скрипт, а не ім'я файлу, яке повинен мати файл, що завантажується.

Усередині файлу put.php ви можете помістити щось схоже на наступний приклад. Він скопіює вміст завантаженого файлу у файл myputfile.ext на сервер. Можливо, вам потрібно буде здійснити кілька перевірок та/або автентифікувати користувача перед копіюванням цього файлу.

**Приклад #1 Збереження файлів, надісланих через HTTP PUT**

```php
<?php
/* PUT данные приходят в потоке ввода stdin */
$putdata = fopen("php://input", "r");

/* Открываем файл на запись */
$fp = fopen("myputfile.ext", "w");

/* Читаем 1 KB данных за один раз
   и пишем в файл */
while ($data = fread($putdata, 1024))
  fwrite($fp, $data);

/* Закрываем потоки */
fclose($fp);
fclose($putdata);
?>
```
