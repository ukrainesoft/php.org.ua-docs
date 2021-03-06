- [«getallheaders](function.getallheaders.md)
- [Менеджер процесів FastCGI»](book.fpm.md)

- [PHP Manual](index.md)
- [Функції Apache](ref.apache.md)
- Виконує підзапит Apache

# virtual

(PHP 4, PHP 5, PHP 7, PHP 8)

virtual — Виконує підзапит Apache

### Опис

**virtual**(string `$uri`): bool

Функція **virtual()** є специфічною для сервера Apache і є
еквівалентом конструкції `<!--#include virtual...-->`, що використовується в
`mod_include`. Ця функція виконує запит Apache. Це буває
корисним у тих випадках, коли необхідно включити до свого скрипту
результат виконання інших CGI-скриптів або файлів `.shtml`, а також
додавання всього, що потрібно обробити Apache. Зверніть увагу,
що CGI-скрипти повинні давати коректні CGI-заголовки. Як мінімум,
CGI-скрипт повинен створювати заголовок `Content-Type`.

Перед тим, як здійсниться виконання підзапиту, всі буфери
скидаються і видаються в браузер, при цьому надсилаються заголовки,
поміщені у буфер.

Ця функція підтримується лише якщо PHP встановлено як модуль
Apache у веб-серверах.

### Список параметрів

`uri`
Ім'я файлу, для якого буде виконано підзапит.

### Значення, що повертаються

Результат виконання підзапиту у разі успішного виконання або
**`false`** у разі виникнення помилки.

### Приклади

Приклад використання дивіться у функції
[apache_note()](function.apache-note.md).

### Примітки

**Увага**

Рядок запиту може бути переданий файлу, однак значення
змінною `$_GET` буде скопійовано з батьківського скрипту, лише
`$_SERVER['QUERY_STRING']` міститиме переданий рядок запиту.
Рядок запиту може бути переданий лише за умови використання Apache 2.
Запитаний файл не відображатиметься в журналі доступу (access log) Apache.

> **Примітка**:
>
> Змінні оточення, встановлені в файлі, не видимі з
> скрипта, що його викликав.

> **Примітка**:
>
> Ця функція може бути використана в PHP-скрипті, але, як правило, більше
> правильним буде вибрати [include](function.include.md) або
> [require](function.require.md).

### Дивіться також

- [apache_note()](function.apache-note.md) - Повертає та
встановлює повідомлення до запиту Apache
