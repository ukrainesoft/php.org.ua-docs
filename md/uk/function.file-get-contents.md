---
navigation:
  - function.file-exists.html: « fileexists
  - function.file-put-contents.html: fileputcontents »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: filegetcontents
---
# filegetcontents

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

filegetcontents — Читає вміст файлу в рядок

### Опис

```methodsynopsis
file_get_contents(    string $filename,    bool $use_include_path = false,    ?resource $context = null,    int $offset = 0,    ?int $length = null): string|false
```

Ця функція схожа на функцію [file()](function.file.md) з тією лише різницею, що **filegetcontents()** повертає вміст файлу в рядку, починаючи з вказаного усунення `offset` і до `length` байт. У разі невдачі, **filegetcontents()** поверне **`false`**

Використання функції **filegetcontents()** найкраще в разі необхідності отримати вміст файлу цілком, оскільки для поліпшення продуктивності функція використовує техніку відображення файлу в пам'ять (memory mapping), якщо вона підтримується вашою операційною системою.

> **Зауваження**
> 
> Якщо ви відкриваєте URI, що містить спецсимволи, такі як пропуск, вам потрібно закодувати URI за допомогою [urlencode()](function.urlencode.md)

### Список параметрів

`filename`

Ім'я файлу, що читається.

`use_include_path`

> **Зауваження**
> 
> Можна використовувати константу **`FILE_USE_INCLUDE_PATH`** для пошуку файлу в [include path](ini.core.html#ini.include-path). Тільки пам'ятайте, що якщо ви використовуєте [строгую типизацию](language.types.declarations.html#language.types.declarations.strict), то так зробити не вийде, оскільки **`FILE_USE_INCLUDE_PATH`** має тип int. У такому разі використовуйте **`true`**

`context`

Коректний ресурс контексту, створений за допомогою функції [streamcontextcreate()](function.stream-context-create.html). Якщо у використанні особливого контексту немає необхідності, можна пропустити цей параметр, передавши в нього значення **`null`**

`offset`

Усунення, з якого почнеться читання оригінального потоку. Негативне значення зміщення буде відраховуватись з кінця потоку.

Пошук усунення (`offset`) не підтримується під час роботи з віддаленими файлами. Спроба пошуку усунення на нелокальних файлах може працювати при невеликих усуненнях, але результат буде непередбачуваним, оскільки функція працює на буферизованому потоці.

`length`

Максимальний розмір даних, що читаються. За промовчанням читання здійснюється доки не буде досягнуто кінець файлу. Зверніть увагу, що цей параметр застосовується і до потоку з фільтрами.

### Значення, що повертаються

Функція повертає прочитані дані або **`false`** у разі виникнення помилки.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.md). Використовуйте [оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Помилки

Буде згенеровано помилку рівня **`E_WARNING`** у випадках, якщо не вдасться знайти `filename`, заданий `length` менше нуля, або пошук по зміщенню `offset` у потоці завершиться невдало.

Коли **filegetcontents()** викликається у каталозі, у Windows помилка генерується **`E_WARNING`**, а з PHP 7.4 також в інших операційних системах.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `length` тепер припускає значення **`null`** |
|  | Додано підтримку негативних значень `offset` |

### Приклади

**Приклад #1 Отримати та вивести вихідний код домашньої сторінки сайту**

```php
<?php
$homepage = file_get_contents('http://www.example.com/');
echo $homepage;
?>
```

**Приклад #2 Пошук файлів у includepath**

```php
<?php
// Если включены строгие типы, то есть объявлено (strict_types=1);
$file = file_get_contents('./people.txt', true);
// Иначе
$file = file_get_contents('./people.txt', FILE_USE_INCLUDE_PATH);
?>
```

**Приклад #3 Читання розділу файлу**

```php
<?php
// Читаем 14 символов, начиная с 21 символа
$section = file_get_contents('./people.txt', FALSE, NULL, 20, 14);
var_dump($section);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(14) "lle Bjori Ro"
```

**Приклад #4 Використання потокових контекстів**

```php
<?php
// Создаём поток
$opts = array(
  'http'=>array(
    'method'=>"GET",
    'header'=>"Accept-language: en\r\n" .
              "Cookie: foo=bar\r\n"
  )
);

$context = stream_context_create($opts);

// Открываем файл с помощью установленных выше HTTP-заголовков
$file = file_get_contents('http://www.example.com/', false, $context);
?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

**Підказка**

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо була увімкнена опція [fopen wrappers](filesystem.configuration.html#ini.allow-url-fopen). Докладніше про визначення імені файлу в описі функції [fopen()](function.fopen.md). Дивіться також список оберток URL, що підтримуються, їх можливості, зауваження щодо використання та список визначених констант у розділі [Підтримувані протоколи та обгортки](wrappers.md)

**Увага**

При використанні SSL Microsoft IIS порушує протокол, закриваючи з'єднання без надсилання індикатора `close_notify`. PHP повідомить про це як "SSL: Fatal Protocol Error" в той момент, коли ви досягнете кінця даних. Щоб обійти це, ви повинні встановити [errorreporting](errorfunc.configuration.html#ini.error-reporting) на рівень, що виключає EWARNING. PHP вміє визначати, що на стороні сервера перебуває проблемний IIS при відкритті потоку за допомогою обгортки `https://` та не виводить попередження. Якщо ви використовуєте [fsockopen()](function.fsockopen.md) для створення `ssl://` сокету, ви самі відповідаєте за визначення та придушення цього попередження.

### Дивіться також

-   [file()](function.file.md) - Читає вміст файлу та поміщає його в масив
-   [fgets()](function.fgets.md) - Читає рядок із файлу
-   [fread()](function.fread.md) - Бінарно-безпечне читання файлу
-   [readfile()](function.readfile.md) - Виводить файл
-   [fileputcontents()](function.file-put-contents.html) - Пише дані у файл
-   [streamgetcontents()](function.stream-get-contents.html) - Читає частину потоку, що залишилася, в рядок
-   [streamcontextcreate()](function.stream-context-create.html) - Створює контекст потоку
-   [$httpresponseheader](reserved.variables.httpresponseheader.md)
