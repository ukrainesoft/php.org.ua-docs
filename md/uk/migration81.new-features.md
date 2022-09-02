---
navigation:
  - migration81.md: « Миграция с PHP 8.0.x на PHP 8.1.x
  - migration81.new-classes.md: Нові класи та інтерфейси »
  - index.md: PHP Manual
  - migration81.md: Миграция с PHP 8.0.x на PHP 8.1.x
title: Нова функціональність
---
## Нова функціональність

### Ядро PHP

#### Літерний префікс вісімкових цілих чисел

Восьмеричні цілі числа тепер можуть використати явний префікс `0o``0O` у цілочисленних літералах, аналогічно двійковим та шістнадцятковим цілочисленним літералам.

```php
<?php
014;  // Восьмеричный литерал без префикса
0o14; // Восьмеричный литерал с префиксом
?>
```

#### Розпакування масиву за допомогою рядкових ключів

Додана підтримка [розпакування масивів з рядковими ключами](language.types.array.md#language.types.array.unpacking)

```php
<?php
$arr1 = [1, 'a' => 'b'];
$arr2 = [...$arr1, 'c' => 'd']; //[1, 'a' => 'b', 'c' => 'd']
?>
```

#### Іменований аргумент після розпакування аргументу

Тепер можна вказати іменовані аргументи після розпакування аргументів. наприклад: foo(...$args, named: $arg).

#### Ключ із повним шляхом при завантаженні файлів

При завантаженні файлів з'явився новий ключ `full_path`, який містить повний шлях (а не тільки відносний) завантаженого файлу. Призначений для використання разом з HTML-атрибутом webkitdirectory.

#### Перерахування

Додана підтримка [перечислений](language.enumerations.md)

#### Файбери

Додана підтримка [файберов](language.fibers.md)

#### Callback-функції як об'єкти першого класу

Замикання для callback-функцій тепер можна створювати синтаксисом. `myFunc(...)`, який ідентичний [синтаксису`Closure::fromCallable('myFunc')`](functions.first_class_callable_syntax.md)

> **Зауваження** `...` є частиною синтаксису, а чи не перепусткою.

#### Перетин типів

Додана підтримка [перетину типів](language.types.declarations.md#language.types.declarations.composite.intersection)

**Застереження**

[Перетин типів](language.types.declarations.md#language.types.declarations.composite.intersection) не можна використовувати разом з [об'єднаними типами](language.types.declarations.md#language.types.declarations.composite.union)

#### Тип never

Доданий новий тип значення, що повертається never. Тип свідчить про те, що функція чи викликає [exit()](function.exit.md), або викидає виняток, або завершується.

#### [`new`](language.oop5.basic.md#language.oop5.basic.new) в ініціалізації класу

Тепер можна використовувати вирази `new ClassName()` як значення за умовчанням для параметра, статичної змінної, ініціалізаторів глобальних констант і як аргументи атрибутів. Тепер об'єкти також можна передавати в [define()](function.define.md)

#### Readonly-властивості

Додана підтримка [readonly](language.oop5.properties.md#language.oop5.properties.readonly-properties)властивостей.

#### Остаточні константи класу

Додана підтримка [модификатора final при определении констант класса](language.oop5.final.md#language.oop5.final.example.php81). Крім того, константи інтерфейсу за умовчанням стають перевизначуваними.

### CURL

Додана опція **`CURLOPT_DOH_URL`**

Додані параметри для сертифіката BLOB-об'єкта, доступні з libcurl >= 7.71.0:

-   **`CURLOPT_ISSUERCERT_BLOB`**
-   **`CURLOPT_PROXY_ISSUERCERT`**
-   **`CURLOPT_PROXY_ISSUERCERT_BLOB`**
-   **`CURLOPT_PROXY_SSLCERT_BLOB`**
-   **`CURLOPT_PROXY_SSLKEY_BLOB`**
-   **`CURLOPT_SSLCERT_BLOB`**
-   **`CURLOPT_SSLKEY_BLOB`**

Доданий клас [CURLStringFile](class.curlstringfile.md), який можна використовувати для надсилання файлу з рядка (string), а не з файлу:

```php
<?php
$file = new CURLStringFile($data, 'filename.txt', 'text/plain');
curl_setopt($curl, CURLOPT_POSTFIELDS, ['file' => $file]);
?>
```

### FPM

Доданий формат статусу openmetrics. Prometheus може використовувати його для отримання метрик FPM.

Додано новий пул для диспетчера динамічних процесів під назвою `pm.max_spawn_rate`. Він дозволяє запускати кілька дочірніх процесів швидшими темпами, якщо обрано динамічний pm. Значення за замовчуванням - `32`, Яке раніше було фіксованим значенням.

### ДД

Підтримка Avif тепер доступна за допомогою [imagecreatefromavif()](function.imagecreatefromavif.md) і [imageavif()](function.imageavif.md)якщо libgd був зібраний з підтримкою Avif.

### Hash

Наступні функції [hash()](function.hash.md) [hashfile()](function.hash-file.md) і [hashinit()](function.hash-init.md) тепер підтримують додатковий необов'язковий аргумент `options`який можна використовувати для передачі специфічних для алгоритму даних.

#### MurmurHash3

Додана підтримка `MurmurHash3` за допомогою потокової передачі. Реалізовано такі варіанти:

-   murmur3a, 32-бітовий хеш
-   murmur3c, 128-розрядний хеш для x86
-   murmur3f, 128-розрядний хеш для x64

Початковий стан хешування можна передати за допомогою ключа `seed` у масиві `options`, наприклад:

```php
<?php
$h = hash("murmur3f", $data, options: ["seed" => 42]);
echo $h, "\n";
?>
```

Допустиме початкове значення знаходиться в діапазоні від `0` до певного платформою значення \*\*`UINT_MAX`\*\*зазвичай - `4294967295`

#### xxHash

Додана підтримка `xxHash`. Реалізовано такі варіанти:

-   xxh32, 32-bit hash
-   xxh64, 64-bit hash
-   xxh3, 64-bit hash
-   xxh128, 128-bit hash

Початковий стан хешування можна передати за допомогою ключа `seed` у масиві `options`, наприклад:

```php
<?php
$h = hash("xxh3", $data, options: ["seed" => 42]);
echo $h, "\n";
?>
```

Використання секрету також підтримується шляхом передачі ключа `secret` у масиві `options`

```php
<?php
$h = hash("xxh3", $data, options: ["secret" => "как минимум 136 байт секрета"]);
echo $h, "\n";
?>
```

Якість секрету користувача має вирішальне значення для якості хешу результату. Для секрету рекомендується використовувати максимально можливу ентропію.

### MySQLi

#### Нова INI-директива `mysqli.local_infile_directory`

Додано INI-директиву [mysqli.localinfiledirectory](mysqli.configuration.md#ini.mysqli.local-infile-directory), за допомогою якої можна вказати каталог, з якого дозволено завантаження файлів. Це має сенс тільки якщо [mysqli.allowlocalinfile](mysqli.configuration.md#ini.mysqli.allow-local-infile) не включено, оскільки в цьому випадку дозволено всі каталоги.

#### Прив'язка параметрів під час виконання

Тепер можна прив'язувати параметри, передавши їх у вигляді масиву [mysqlistmt::execute()](mysqli-stmt.execute.md). Усі значення будуть прив'язані як рядки. Дозволено лише облікові масиви. Ця нова функція недоступна, якщо MySQLi скомпільовано з libmysqlclient.

```php
<?php
$stmt = $mysqli->prepare('INSERT INTO users(id, name) VALUES(?,?)');
$stmt->execute([1, $username]);
?>
```

#### Новий метод [mysqliresult::fetchcolumn()](mysqli-result.fetch-column.md)

Доданий [mysqliresult::fetchcolumn()](mysqli-result.fetch-column.md) для вибірки єдиного скалярного значення набору результатів. Новий метод приймає необов'язковий параметр `column`, що починається з 0, у вигляді цілого числа (int), що вказує з якого стовпця робити вибірку.

```php
<?php
$result = $mysqli->query('SELECT username FROM users WHERE id = 123');
echo $result->fetch_column();
?>
```

### PDO

Доданий атрибут **`PDO::MYSQL_ATTR_LOCAL_INFILE_DIRECTORY`**, який можна використовувати для вказівки каталогу, з якого можна завантажити файли. Це має сенс лише в тому випадку, якщо **`PDO::MYSQL_ATTR_LOCAL_INFILE`** не включено, оскільки в цьому випадку дозволено всі каталоги.

### PDOSQLite

Підтримується новий елемент `"file:"` у DSN-префіксі SQLite, який дозволяє вказувати додаткові прапори. Він не буде працювати, якщо увімкнено опцію openbasedir.

```php
<?php
new PDO('sqlite:file:path/to/sqlite.db?mode=ro')
?>
```

### POSIX

Додані константи **`POSIX_RLIMIT_KQUEUES`** і **`POSIX_RLIMIT_NPTS`**. Ці обмеження доступні лише у FreeBSD.

### Стандартні функції

[fputcsv()](function.fputcsv.md) тепер приймає новий аргумент `eol`, який дозволяє визначати послідовність кінця рядка, що настроюється, значення за замовчуванням залишається колишнім - `"\n"`

### SPL

[SplFileObject::fputcsv()](splfileobject.fputcsv.md) тепер приймає новий аргумент `eol`, який дозволяє визначати послідовність кінця рядка, що настроюється, значення за замовчуванням залишається колишнім - `"\n"`
