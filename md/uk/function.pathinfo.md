---
navigation:
  - function.parse-ini-string.html: « parseinistring
  - function.pclose.md: pclose »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: pathinfo
---
# pathinfo

(PHP 4> = 4.0.3, PHP 5, PHP 7, PHP 8)

pathinfo — Повертає інформацію про шлях до файлу

### Опис

```methodsynopsis
pathinfo(string $path, int $flags = PATHINFO_ALL): array|string
```

**pathinfo()** повертає інформацію про `path` у вигляді асоціативного масиву або рядка, залежно від `flags`

> **Зауваження**
> 
> Докладніше про отримання інформації про поточний шлях можна почитати в розділі [Обумовлені зарезервовані змінні](language.variables.predefined.md)

> **Зауваження**
> 
> **pathinfo()** оперує вхідним рядком і не знає фактичну файлову систему чи компоненти шляху, такі як "`..`".

**Застереження**

**pathinfo()** враховує налаштування локалі, тому для коректної обробки шляху з багатобайтними символами має бути встановлена ​​відповідна локаль за допомогою функції [setlocale()](function.setlocale.md)

### Список параметрів

`path`

Аналізований шлях.

`flags`

Якщо зазначено, то ставить, який з елементів шляху буде повернутий: **`PATHINFO_DIRNAME`** **`PATHINFO_BASENAME`** **`PATHINFO_EXTENSION`** і **`PATHINFO_FILENAME`**

Якщо `flags` не вказано, то повертаються всі доступні елементи.

### Значення, що повертаються

Якщо параметр `flags` не переданий, то асоціативний масив (array), що повертається, міститиме наступні елементи: `dirname` `basename` `extension` (якщо є) та `filename`

> **Зауваження**
> 
> Якщо `path` містить більше одного розширення, то **`PATHINFO_EXTENSION`** повертає тільки останній та **`PATHINFO_FILENAME`** видаляє лише останнє розширення. (Дивіться приклад нижче).

> **Зауваження**
> 
> Якщо `path` не містить розширення, то не буде повернено елемент `extension` (Дивіться нижче другий приклад).

> **Зауваження**
> 
> Якщо `basename` параметра `path` починається з точки, то всі наступні символи інтерпретуються як розширення файлу (`extension`) та ім'я файлу `filename` буде порожнім (дивіться третій приклад).

Якщо вказано параметр `flags`, буде повернуто рядок (string), що містить вказаний елемент.

### Приклади

**Приклад #1 Приклад використання функції **pathinfo()****

```php
<?php
$path_parts = pathinfo('/www/htdocs/inc/lib.inc.php');

echo $path_parts['dirname'], "\n";
echo $path_parts['basename'], "\n";
echo $path_parts['extension'], "\n";
echo $path_parts['filename'], "\n";
?>
```

Результат виконання цього прикладу:

```
/www/htdocs/inc
lib.inc.php
php
lib.inc
```

**Приклад #2 Приклад з **pathinfo()**, що показує різницю між null та відсутністю розширення**

```php
<?php
$path_parts = pathinfo('/path/emptyextension.');
var_dump($path_parts['extension']);

$path_parts = pathinfo('/path/noextension');
var_dump($path_parts['extension']);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(0) ""

Notice: Undefined index: extension in test.php on line 6
NULL
```

**Приклад #3 Приклад **pathinfo()** для файлу, що починається з точки**

```php
<?php
print_r(pathinfo('/some/path/.test'));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [dirname] => /some/path
    [basename] => .test
    [extension] => test
    [filename] =>
)
```

### Дивіться також

-   [dirname()](function.dirname.md) - Повертає ім'я батьківського каталогу із зазначеного шляху
-   [basename()](function.basename.md) - Повертає останній компонент імені із зазначеного шляху
-   [parseurl()](function.parse-url.md) - Розбирає URL та повертає його компоненти
-   [realpath()](function.realpath.md) - Повертає абсолютний канонізований шлях до файлу
