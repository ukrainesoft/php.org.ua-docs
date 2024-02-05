---
navigation:
  - function.parse-ini-string.md: « parse\_ini\_string
  - function.pclose.md: pclose »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: pathinfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pathinfo

(PHP 4 >= 4.0.3, PHP 5, PHP 7, PHP 8)

pathinfo — Повертає інформацію про шлях до файлу

### Опис

```methodsynopsis
pathinfo(string $path, int $flags = PATHINFO_ALL): array|string
```

**pathinfo()** повертає інформацію про `path` у вигляді асоціативного масиву або рядка, залежно від `flags`

> **Зауваження** :
> 
> Докладніше про отримання інформації про поточний шлях можна почитати в розділі [Обумовлені зарезервовані змінні](language.variables.predefined.md)

> **Зауваження** :
> 
> **pathinfo()** оперує вхідним рядком і не знає фактичну файлову систему чи компоненти шляху, такі як " `.. .` ".

> **Зауваження** :
> 
> Лише у системах Windows символ `\` інтерпретуватиметься як роздільник каталогів. В інших системах він розглядатиметься як будь-який інший символ.

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

> **Зауваження** :
> 
> Якщо `path` містить більше одного розширення, то **`PATHINFO_EXTENSION`** повертає тільки останній та \*\*`PATHINFO_FILENAME`\*\*удаляет только последнее расширение. (смотрите Приклад ниже).

> **Зауваження** :
> 
> Якщо `path` не містить розширення, то не буде повернутий елемент `extension` (Дивіться нижче другий приклад).

> **Зауваження** :
> 
> Якщо `basename`параметра`path` починається з точки, то всі наступні символи інтерпретуються як розширення файлу (`extension`) та ім'я файлу `filename` буде порожнім (дивіться третій приклад).

Если указан параметр`flags`, буде повернуто рядок (string), що містить вказаний елемент.

### Приклади

**Приклад #1 Приклад использования функции**pathinfo()\*\*\*\*

```php
<?php
$path_parts = pathinfo('/www/htdocs/inc/lib.inc.php');

echo $path_parts['dirname'], "\n";
echo $path_parts['basename'], "\n";
echo $path_parts['extension'], "\n";
echo $path_parts['filename'], "\n";
?>
```

Результат виконання наведеного прикладу:

```
/www/htdocs/inc
lib.inc.php
php
lib.inc
```

**Приклад #2 Приклад с**pathinfo()**, що показує різницю між null та відсутністю розширення**

```php
<?php
$path_parts = pathinfo('/path/emptyextension.');
var_dump($path_parts['extension']);

$path_parts = pathinfo('/path/noextension');
var_dump($path_parts['extension']);
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(0) ""

Notice: Undefined index: extension in test.php on line 6
NULL
```

**Приклад #3 Приклад**pathinfo()\*\* для файлу, що починається з точки\*\*

```php
<?php
print_r(pathinfo('/some/path/.test'));
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [dirname] => /some/path
    [basename] => .test
    [extension] => test
    [filename] =>
)
```

**Приклад #4 Приклад використання** pathinfo()\*\* з розіменуванням масиву\*\*

Параметр`flags` не є бітовою маскою. Можливе лише одне значення. Щоб вибрати лише обмежений набір розібраних значень, використовуйте деструктуризацію масиву таким чином:

```php
<?php
['basename' => $basename, 'dirname' => $dirname] = pathinfo('/www/htdocs/inc/lib.inc.php');

var_dump($basename, $dirname);
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(11) "lib.inc.php"
string(15) "/www/htdocs/inc"
```

### Дивіться також

-   [dirname()](function.dirname.md) \- Повертає ім'я батьківського каталогу із зазначеного шляху
-   [basename()](function.basename.md) \- Повертає останній компонент імені із зазначеного шляху
-   [parse\_url()](function.parse-url.md) \- Розбирає URL та повертає його компоненти
-   [realpath()](function.realpath.md) \- Повертає абсолютний канонізований шлях до файлу
