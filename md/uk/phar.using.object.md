---
navigation:
  - phar.using.stream.md: '« Використання Phar-архівів: обгортка потоку phar'
  - phar.creating.md: Створення Phar-архівів »
  - index.md: PHP Manual
  - phar.using.md: Використання Phar-архівів
title: 'Використання Phar-архівів: класи Phar та PharData'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Використання Phar-архівів: класи Phar та PharData

Класс[Phar](class.phar.md) підтримує читання та обробку Phar-архівів, а також ітерацію через успадковану функціональність класу [RecursiveDirectoryIterator](class.recursivedirectoryiterator.md)Благодаря поддержке интерфейса[ArrayAccess](class.arrayaccess.md), доступ до файлів всередині Phar-архіву може бути отриманий, якби вони були частиною асоціативного масиву.

Класс[PharData](class.phardata.md) розширює клас [Phar](class.phar.md) і дозволяє створювати та змінювати невиконані tar- та zip-архіви даних навіть у тому випадку, якщо параметр `phar.readonly`\=1 у php.ini. Фактично функції [PharData::setAlias()](phardata.setalias.md) і [PharData::setStub()](phardata.setstub.md) відключені, оскільки концепція псевдоніма та заглушки є унікальною для виконуваних phar-архівів.

При створенні Phar-архіву в конструктор об'єкта [Phar](class.phar.md) має бути переданий повний шлях. Спроби ініціалізації об'єкта Phar з відносними шляхами зазнають невдачі.

Припустимо, що `$p` - об'єкт Phar, ініціалізований, як показано нижче:

```php
<?php
$p = new Phar('/путь/к/myphar.phar', 0, 'myphar.phar');
?>
```

Порожній Phar-архів буде створено в `/шлях/до/myphar.phar`, або якщо файл `/path/to/myphar.phar` вже існує, він буде відкрито повторно. Використання `myphar.phar` показує концепцію псевдоніма, який може бути використаний для вказівки на `/шлях/до/myphar.phar` в URL-адресах, подібно до того, як показано нижче:

```php
<?php
// эти два вызова file_get_contents() равнозначны в том случае, если
// /путь/к/myphar.phar имеет явно заданный псевдоним "myphar.phar"
// в своём манифесте, или если phar был инициализирован созданием объекта Phar,
// как показано в предыдущем Прикладе
$f = file_get_contents('phar:///путь/к/myphar.phar/whatever.txt');
$f = file_get_contents('phar://myphar.phar/whatever.txt');
?>
```

З щойно створеним об'єктом `$p`класса[Phar](class.phar.md) можливо наступне:

-   `$a = $p['file.php']`створить об'єкт класу[PharFileInfo](class.pharfileinfo.md), який посилатиметься на вміст`phar://myphar.phar/file.php`
-   `$p['file.php'] = $v`створить новий файл (`phar://myphar.phar/file.php`) або перезапише існуючий усередині`myphar.phar`. . `$v`може бути рядком або вказівником на відкритий файл. В останньому випадку для створення нового файлу буде використано весь вміст відкритого файлу. Зверніть увагу, що функціонально еквівалентним цьому буде виклик`$p->addFromString('file.php', $v)`. Також є можливість додавання вмісту файлу за допомогою`$p->addFile('/path/to/file.php', 'file.php')`. Нарешті, порожній каталог може бути створений за допомогою`$p->addEmptyDir('empty')`
-   `isset($p['file.php'])`може бути використано для визначення існування файлу`phar://myphar.phar/file.php`внутри`myphar.phar`
-   `unset($p['file.php'])`видаляє файл`phar://myphar.phar/file.php`из`myphar.phar`

Крім того, використання об'єкта [Phar](class.phar.md) є єдиним способом отримати доступ до метаданих архіву (через [Phar::getMetadata()](phar.getmetadata.md)) і єдиним способом встановити або отримати заглушку Phar-архіву через [Phar::getStub()](phar.getstub.md) і [Phar::setStub()](phar.setstub.md). До того ж, працювати зі стисненням цілого Phar-архіву можна лише використовуючи клас [Phar](class.phar.md)

Повний перелік функціоналу об'єкту [Phar](class.phar.md) задокументовано нижче.

Класс[PharFileInfo](class.pharfileinfo.md) розширює клас [SplFileInfo](class.splfileinfo.md) та додає кілька методів для роботи з деталями, властивими файлам, які містяться в Phar-архіві, такими як робота зі стисненням та метаданими.
