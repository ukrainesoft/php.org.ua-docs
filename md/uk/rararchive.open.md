Відкриває архів RAR

-   [« RarArchive::isSolid](rararchive.issolid.md)
    
-   [RarArchive::setAllowBroken »](rararchive.setallowbroken.md)
    
-   [PHP Manual](index.md)
    
-   [RarArchive](class.rararchive.md)
    
-   Відкриває архів RAR
    

# RarArchive::open

# raropen

(PECL rar >= 2.0.0)

RarArchive::open -- raropen — Відкриває архів RAR

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public static RarArchive::open(string $filename, string $password = NULL, callable $volume_callback = NULL): RarArchive|false
```

Процедурний стиль:

```methodsynopsis
rar_open(string $filename, string $password = NULL, callable $volume_callback = NULL): RarArchive|false
```

Відкриває зазначений RAR-архів та повертає об'єкт [RarArchive](class.rararchive.md)представляє його.

> **Зауваження**
> 
> При відкритті багатотомного архіву шлях до першого тому має бути переданий першим параметром. Інакше не буде видно всіх файлів.

### Список параметрів

`filename`

Шлях до архіву Rar.

`password`

Пароль, якщо потрібно розшифрувати заголовки архіву. Цей пароль буде використовуватися за замовчуванням, якщо знайдено зашифровані файли. Зауважте, що файли можуть бути зашифровані з різними паролями.

`volume_callback`

Функція, якою передається єдиний параметр - шлях до того, який не був знайдений, і повертає рядок з правильним шляхом для цього тому або \*\*`null`\*\*якщо цей том не існує або невідомий. Розробник повинен бути впевнений, що дана функція не призведе до зациклювання, оскільки вона викликається повторно, якщо шлях, отриманий попереднім викликом, не відповідає потрібному тому. Вказівка ​​цього параметра усуває попередження, які б з'являлися, якби тому не було знайдено. Якщо функція повертає тільки **`null`**, то не буде жодного попередження.

**Увага**

До версії 2.0.0 ця функція не обробляла правильно відносні шляхи. У таких випадках використовуйте [realpath()](function.realpath.md)

### Значення, що повертаються

Повертає запитуваний об'єкт [RarArchive](class.rararchive.md) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| PECL rar 3.0.0 | Був доданий `volume_callback` |

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$rar_arch = RarArchive::open('encrypted_headers.rar', 'samplepassword');
if ($rar_arch === FALSE)
    die("Неудачное открытие файла");

$entries = $rar_arch->getEntries();
if ($entries === FALSE)
    die("Неудачное получение записей");

echo "Найдено " . count($entries) . " файлов.\n";

if (empty($entries))
    die("Не найдено корректных записей.");

$stream = reset($entries)->getStream();
if ($stream === FALSE)
    die("Неудачное открытие первого файла");

$rar_arch->close();

echo "Содержимое первого файла:\n";
echo stream_get_contents($stream);

fclose($stream);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Найдено 2 файлов.
Содержимое первого файла:
Encrypted file 1 contents.
```

**Приклад #2 Процедурний стиль**

```php
<?php
$rar_arch = rar_open('encrypted_headers.rar', 'samplepassword');
if ($rar_arch === FALSE)
    die("Неудачное открытие файла");

$entries = rar_list($rar_arch);
if ($entries === FALSE)
    die("Failed fetching entries");

echo "Найдено " . count($entries) . " файлов.\n";

if (empty($entries))
    die("Не найдено корректных записей.");

$stream = reset($entries)->getStream();
if ($stream === FALSE)
    die("Неудачное открытие первого файла");

rar_close($rar_arch);

echo "Содержимое первого файла:\n";
echo stream_get_contents($stream);

fclose($stream);
?>
```

**Приклад #3 Callback-функція для тому**

```php
<?php
/* В этом примере есть том с именем multi_broken.part1.rar,
 * а следующий том имеет имя multi.part2.rar */
function resolve($vol) {
    if (preg_match('/_broken/', $vol))
        return str_replace('_broken', '', $vol);
    else
        return null;
}
$rar_file1 = rar_open(dirname(__FILE__).'/multi_broken.part1.rar', null, 'resolve');
$entry = $rar_file1->getEntry('file2.txt');
$entry->extract(null, dirname(__FILE__) . "/temp_file2.txt");
?>
```

### Дивіться також

-   [`rar://`wrapper](wrappers.rar.md)