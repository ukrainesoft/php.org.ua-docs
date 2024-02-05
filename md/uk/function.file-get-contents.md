---
navigation:
  - function.file-exists.md: « file\_exists
  - function.file-put-contents.md: file\_put\_contents »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: file\_get\_contents
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# file\_get\_contents

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

file\_get\_contents — Читає вміст файлу в рядок

### Опис

```methodsynopsis
file_get_contents(    string $filename,    bool $use_include_path = false,    ?resource $context = null,    int $offset = 0,    ?int $length = null): string|false
```

Данная функция похожа на функцию[file()](function.file.md) з тією лише різницею, що **file\_get\_contents()** повертає вміст файлу в рядку, починаючи з вказаного усунення `offset`и до`length`байт. В случае неудачи,**file\_get\_contents()** поверне **`false`**

Использование функции**file\_get\_contents()** найкраще в разі необхідності отримати вміст файлу повністю, оскільки для поліпшення продуктивності функція використовує техніку відображення файлу в пам'ять (memory mapping), якщо вона підтримується вашою операційною системою.

> **Зауваження** :
> 
> Якщо ви відкриваєте URI, що містить спецсимволи, такі як пропуск, вам потрібно закодувати URI за допомогою [urlencode()](function.urlencode.md)

### Список параметрів

`filename`

Ім'я файлу, що читається.

`use_include_path`

> **Зауваження** :
> 
> Можна використовувати константу \*\*`FILE_USE_INCLUDE_PATH`\*\*для поиска файла в[include path](ini.core.md#ini.include-path). Тільки пам'ятайте, що якщо ви використовуєте [строгу типізацію](language.types.declarations.md#language.types.declarations.strict), то так зробити не вийде, оскільки **`FILE_USE_INCLUDE_PATH`** має тип int. У такому разі використовуйте **`true`**

`context`

Коректний ресурс контексту, створений за допомогою функції [stream\_context\_create()](function.stream-context-create.md). Якщо у використанні особливого контексту немає необхідності, можна пропустити цей параметр, передавши в нього значення **`null`**

`offset`

Усунення, з якого почнеться читання оригінального потоку. Негативне значення усунення буде відраховуватися з кінця потоку.

Пошук усунення (`offset`) не підтримується під час роботи з віддаленими файлами. Спроба пошуку усунення на нелокальних файлах може працювати при невеликих усуненнях, але результат буде непередбачуваним, оскільки функція працює на буферизованому потоці.

`length`

Максимальний розмір даних, що читаються. За промовчанням читання здійснюється доки не буде досягнуто кінець файлу. Зверніть увагу, що цей параметр застосовується і до потоку з фільтрами.

### Значення, що повертаються

Функція повертає прочитані дані або \*\*`false`\*\*в случае возникновения ошибки.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Помилки

Буде згенеровано помилку рівня **`E_WARNING`** у випадках, якщо не вдасться знайти `filename`, задан`length` менше нуля, або пошук по зміщенню `offset` у потоці завершиться невдало.

Когда**file\_get\_contents()** викликається у каталозі, у Windows помилка генерується **`E_WARNING`**, а з PHP 7.4 також в інших операційних системах.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`length` тепер припускає значення **`null`** |
| 7.1.0 | Додано підтримку негативних значень `offset` |

### Приклади

**Приклад #1 Отримати та вивести вихідний код домашньої сторінки сайту**

```php
<?php
$homepage = file_get_contents('http://www.example.com/');
echo $homepage;
?>
```

**Приклад #2 Пошук файлів у include\_path**

```php
<?php
// Если включены строгие типы, то есть объявлено (strict_types=1);
$file = file_get_contents('./people.txt', true);
// Иначе
$file = file_get_contents('./people.txt', FILE_USE_INCLUDE_PATH);
?>
```

**Приклад #3 Читання розділу файлу**

```php
<?php
// Читаем 14 символов, начиная с 21 символа
$section = file_get_contents('./people.txt', FALSE, NULL, 20, 14);
var_dump($section);
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(14) "lle Bjori Ro"
```

**Приклад #4 Використання потокових контекстів**

```php
<?php
// Создаём поток
$opts = array(
  'http'=>array(
    'method'=>"GET",
    'header'=>"Accept-language: en\r\n" .
              "Cookie: foo=bar\r\n"
  )
);

$context = stream_context_create($opts);

// Открываем файл с помощью установленных выше HTTP-заголовков
$file = file_get_contents('http://www.example.com/', false, $context);
?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

**Підказка**

У цю функцію як ім'я файлу можна передавати URL-адреси, якщо була включена директива [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про те, як вказати ім'я файлу, описано в описі функції [fopen()](function.fopen.md). В розділі "[Підтримувані протоколи та обгортки](wrappers.md)» також дано посилання на інформацію про можливості підтримуваних обгорток, зауваження щодо роботи з ними та список визначених змінних, які вони дають.

**Увага**

При використанні SSL Microsoft IIS порушує протокол, закриваючи з'єднання без надсилання індикатора `close_notify`. PHP повідомить про це як "SSL: Fatal Protocol Error" в той момент, коли буде досягнуто кінця даних. Щоб обійти це, потрібно встановити директиву [error\_reporting](errorfunc.configuration.md#ini.error-reporting)на уровень, исключающий E\_WARNING. PHP вміє визначати, що на стороні сервера проблемний IIS при відкритті потоку обгорткою `https://` та не виводить попередження. Якщо розробник створює сокет `ssl://` через виклик функції [fsockopen()](function.fsockopen.md), він сам відповідає за визначення та придушення цього попередження.

### Дивіться також

-   [file()](function.file.md) \- Читає вміст файлу та поміщає його в масив
-   [fgets()](function.fgets.md) \- Читає рядок із файлу
-   [fread()](function.fread.md) \- Бінарно-безпечне читання файлу
-   [readfile()](function.readfile.md) \- Виводить файл
-   [file\_put\_contents()](function.file-put-contents.md) \- Пише дані у файл
-   [stream\_get\_contents()](function.stream-get-contents.md) \- Читає частину потоку, що залишилася, в рядок
-   [stream\_context\_create()](function.stream-context-create.md) \- Створює контекст потоку
-   [$http\_response\_header](reserved.variables.httpresponseheader.md)
