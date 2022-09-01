---
navigation:
  - pdo.error-handling.html: « Ошибки и их обработка
  - class.pdo.html: PDO »
  - index.html: PHP Manual
  - book.pdo.html: PDO
title: Великі об'єкти (LOB)
---
# Великі об'єкти (LOB)

Іноді для роботи програми необхідно зберігати великі порції даних у базі. Зазвичай під великим розуміють обсяг даних "близько 4 кілобайт або більше", хоча деякі бази даних можуть спокійно обробляти до 32 кілобайт, перш ніж розмір даних стає "великим". Великі об'єкти можуть бути текстовими або бінарними. PDO дозволяє працювати з такими об'єктами шляхом встановлення типу даних **`PDO::PARAM_LOB`** у методах [PDOStatement::bindParam()](pdostatement.bindparam.html) або [PDOStatement::bindColumn()](pdostatement.bindcolumn.html). . **`PDO::PARAM_LOB`** повідомляє PDO, що потрібно позначити ці дані як потік. І відповідно працювати з такими об'єктами можна, використовуючи [API потоків PHP](ref.stream.html)

**Приклад #1 Виведення зображення, що зберігається у базі даних**

У цьому прикладі змінної $lob задають у відповідність великий об'єкт LOB, а потім відсилають її до браузера за допомогою функції [fpassthru()](function.fpassthru.html). Оскільки LOB представляється як потоку, з ним можуть працювати такі функції, як [fgets()](function.fgets.html) [fread()](function.fread.html) і [streamgetcontents()](function.stream-get-contents.html)

```php
<?php
$db = new PDO('odbc:SAMPLE', 'db2inst1', 'ibmdb2');
$stmt = $db->prepare("select contenttype, imagedata from images where id=?");
$stmt->execute(array($_GET['id']));
$stmt->bindColumn(1, $type, PDO::PARAM_STR, 256);
$stmt->bindColumn(2, $lob, PDO::PARAM_LOB);
$stmt->fetch(PDO::FETCH_BOUND);

header("Content-Type: $type");
fpassthru($lob);
?>
```

**Приклад #2 Вставлення зображення до бази даних**

У цьому прикладі буде відкриватися файл із зображенням, його файловий покажчик передається PDO, який у свою чергу вставляє зображення до бази у вигляді LOB. PDO витягне вміст файлу і помістить його в базу найбільш ефективним способом.

```php
<?php
$db = new PDO('odbc:SAMPLE', 'db2inst1', 'ibmdb2');
$stmt = $db->prepare("insert into images (id, contenttype, imagedata) values (?, ?, ?)");
$id = get_new_id(); // какая-то функция для выделения нового ID

// предположим, что мы находимся на странице загрузки файлов на удалённый сервер

$fp = fopen($_FILES['file']['tmp_name'], 'rb');

$stmt->bindParam(1, $id);
$stmt->bindParam(2, $_FILES['file']['type']);
$stmt->bindParam(3, $fp, PDO::PARAM_LOB);

$db->beginTransaction();
$stmt->execute();
$db->commit();
?>
```

**Приклад #3 Вставлення зображення до бази даних: Oracle**

У випадку з базами Oracle потрібен інший синтаксис для вилучення вмісту файлу і приміщення в базу. Також необхідно виконувати вставку в рамках транзакції, інакше вставлений LOB буде зафіксований у базі з нульовою довжиною, оскільки якщо не позначити межі транзакції, зміни фіксуватимуться після кожного виконаного запиту.

```php
<?php
$db = new PDO('oci:', 'scott', 'tiger');
$stmt = $db->prepare("insert into images (id, contenttype, imagedata) " .
"VALUES (?, ?, EMPTY_BLOB()) RETURNING imagedata INTO ?");
$id = get_new_id(); // какая-то функция для выделения ID

// предположим, что мы находимся на странице загрузки файлов на удалённый сервер

$fp = fopen($_FILES['file']['tmp_name'], 'rb');

$stmt->bindParam(1, $id);
$stmt->bindParam(2, $_FILES['file']['type']);
$stmt->bindParam(3, $fp, PDO::PARAM_LOB);

$db->beginTransaction();
$stmt->execute();
$db->commit();
?>
```
