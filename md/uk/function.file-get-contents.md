- [«file_exists](function.file-exists.md)
- [file_put_contents »](function.file-put-contents.md)

- [PHP Manual](index.md)
- [Функції файлової системи](ref.filesystem.md)
- Читає вміст файлу в рядок

# file_get_contents

(PHP 4 \>= 4.3.0, PHP 5, PHP 7, PHP 8)

file_get_contents — Читає вміст файлу в рядок

### Опис

**file_get_contents**(
string `$filename`,
bool `$use_include_path` = **`false`**,
?resource `$context` = **`null`**,
int `$offset` = 0,
?int `$length` = **`null`**
): string\|false

Ця функція схожа на функцію [file()](function.file.md) з тієї лише
різницею, що **file_get_contents()** повертає вміст файлу в
рядку, починаючи з зазначеного усунення `offset` і до `length` байт. В
у разі невдачі, **file_get_contents()** поверне **`false`**.

Використання функції **file_get_contents()** найбільш переважно в
у разі необхідності отримати вміст файлу повністю, оскільки
покращення продуктивності функція використовує техніку відображення
файлу в пам'ять (memory mapping), якщо вона підтримується вашою
операційною системою.

> **Примітка**:
>
> Якщо ви відкриваєте URI, що містить спецсимволи, такі як пробіл, вам
> потрібно закодувати URI за допомогою
> [urlencode()](function.urlencode.md).

### Список параметрів

`filename`
Ім'я файлу, що читається.

`use_include_path`
> **Примітка**:
>
> Можна використовувати константу **`FILE_USE_INCLUDE_PATH`** для пошуку
> файлу [include path](ini.core.md#ini.include-path). Тільки
> пам'ятайте, що якщо ви використовуєте [сувору > типізацію](language.types.declarations.md#language.types.declarations.strict),
> то так зробити не вийде, оскільки **`FILE_USE_INCLUDE_PATH`**
> має тип int. У такому разі використовуйте **`true`**.

`context`
Коректний ресурс контексту, створений за допомогою функції
[stream_context_create()](function.stream-context-create.md). Якщо в
використання особливого контексту немає необхідності, можна пропустити цей
параметр передавши до нього значення **`null`**.

`offset`
Усунення, з якого почнеться читання оригінального потоку. Негативне
значення зміщення буде відраховуватись з кінця потоку.

Пошук зміщення (`offset`) не підтримується під час роботи з віддаленими
файлами. Спроба пошуку усунення на нелокальних файлах може працювати
при невеликих усуненнях, але результат буде непередбачуваним, оскільки
функція працює на буферизованому потоці.

`length`
Максимальний розмір даних, що читаються. За промовчанням читання здійснюється
поки не буде досягнуто кінця файлу. Врахуйте, що цей параметр
застосовується до потоку з фільтрами.

### Значення, що повертаються

Функція повертає прочитані дані або **`false`** у разі
виникнення помилки.

**Увага**

Ця функція може повертати як логічне значення **`false`**, так і
значення не типу boolean, яке наводиться до **`false`**. Більше
Детальну інформацію див. у розділі [Булев тип](language.types.boolean.md). Використовуйте [оператор ===](language.operators.comparison.md) для перевірки значення,
повертається цією функцією.

### Помилки

Буде згенерована помилка рівня **`E_WARNING`** у випадках, якщо не
вдасться знайти `filename`, заданий `length` менше нуля, або пошук по
зсуву `offset` у потоці завершиться невдало.

Коли **file_get_contents()** викликається в каталозі, у Windows помилка
генерується **`E_WARNING`**, а з PHP 7.4 також в інших операційних
системах.

### Список змін

| Версія | Опис                                              |
| ------ | ------------------------------------------------- |
| 8.0.0  | Параметр length тепер допускає значення **null**. |
| 7.1.0  | Додано підтримку негативних значень offset.       |

### Приклади

**Приклад #1 Отримати та вивести вихідний код домашньої сторінки сайту**

` <?php$homepage = file_get_contents('http://www.example.com/');echo $homepage;?> `

**Приклад #2 Пошук файлів у include_path**

`<?php// Якщо включені строгі типи, то є оголошено (strict_types=1);$file = file_get_contents('./people.txt', true);// Інакше$file = t| ', FILE_USE_INCLUDE_PATH);?> `

**Приклад #3 Читання секції файлу**

`<?php// Читаємо 14 символів, починаючи з 21 символу$section = file_get_contents('./people.txt', FALSE, NULL, 20, 14);var_dump($section);

Результатом виконання цього прикладу буде щось подібне:

string(14) "lle Bjori Ro"

**Приклад #4 Використання потокових контекстів**

` <?php// Створюємо потік$opts = array(  'http'=>array(   'method'=>"GET",   'header'=>"Accept-language: en
Cookie:foo=bar
"  ));$context = stream_context_create($opts);// Відкриваємо файл за допомогою встановлених вище HTTP-заголовків$file==file_get_contents('http://www.example.com/';>> `

### Примітки

> **Примітка**: Ця функція безпечна для обробки даних у двійковій
> Формі.

**Підказка**

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо
була включена опція [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Дивіться
докладнішу інформацію про визначення імені файлу в описі функції
[fopen()](function.fopen.md). Дивіться також список підтримуваних
оберток URL, їх можливості, зауваження щодо використання та список
визначених констант у розділі [Підтримувані протоколи та обертки](wrappers.md).

**Увага**

При використанні SSL Microsoft IIS порушує протокол, закриваючи
з'єднання без надсилання індикатора `close_notify`. PHP повідомить про це
як "SSL: Fatal Protocol Error" в той момент, коли ви досягнете кінця
даних. Щоб обійти це, ви повинні встановити
[error_reporting](errorfunc.configuration.md#ini.error-reporting)
рівень, що виключає E_WARNING. PHP вміє визначати, що на стороні
сервера знаходиться проблемний IIS при відкритті потоку за допомогою обгортки
`https://` і виводить попередження. Якщо ви використовуєте
[fsockopen()](function.fsockopen.md) для створення `ssl://` сокету, ви
самі відповідаєте за визначення та придушення цього попередження.

### Дивіться також

- [file()](function.file.md) - Читає вміст файлу та поміщає
його в масив
- [fgets()](function.fgets.md) - Читає рядок із файлу
- [fread()](function.fread.md) - Бінарно-безпечне читання файлу
- [readfile()](function.readfile.md) - Виводить файл
- [file_put_contents()](function.file-put-contents.md) - Пише
дані у файл
- [stream_get_contents()](function.stream-get-contents.md) - Читає
решту потоку в рядок
- [stream_context_create()](function.stream-context-create.md) -
Створює контекст потоку
- [$http_response_header](reserved.variables.httpresponseheader.md)
