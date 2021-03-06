- [«fgetss](function.fgetss.md)
- [file_get_contents »](function.file-get-contents.md)

- [PHP Manual](index.md)
- [Функції файлової системи](ref.filesystem.md)
- Перевіряє існування вказаного файлу чи каталогу

# file_exists

(PHP 4, PHP 5, PHP 7, PHP 8)

file_exists — Перевіряє наявність вказаного файлу або каталогу

### Опис

**file_exists**(string `$filename`): bool

Перевіряє наявність вказаного файлу чи каталогу.

### Список параметрів

`filename`
Шлях до файлу чи каталогу.

На платформах Windows для перевірки наявності файлів на мережевих ресурсах,
використовуйте імена, подібні до `//computername/share/filename` або
`\computername\share ilename`.

### Значення, що повертаються

Повертає **`true`**, якщо файл або каталог, вказаний параметром
`filename`, існує, інакше повертає **`false`**.

> **Примітка**:
>
> Ця функція повертає **`false`** для символічних посилань,
> що вказують на неіснуючі файли.

> **Примітка**:
>
> Перевірка відбувається за допомогою реальних UID/GID, а не ефективних
> ідентифікатори.

> **Примітка**: Так як тип integer в PHP є цілим числом
> знаком, і багато платформ використовують 32-х бітні цілі числа, то
> деякі функції файлових систем можуть повертати несподівані
> результати файлів розміром більше 2 Гб.

### Помилки

У разі невдалого завершення роботи генерується помилка рівня
**`E_WARNING`**.

### Приклади

**Приклад #1 Перевірка існування файлу**

` <?php$filename = '/path/to/foo.txt';if (file_exists($filename)) {   echo "Файл $filename існує";} else {    echo "" `

### Примітки

> **Примітка**: Результати цієї функції кешуються. Детальніше
> інформацію дивіться у розділі
> [clearstatcache()](function.clearstatcache.md).

**Підказка**

Починаючи з PHP 5.0.0, ця функція також може бути використана з
* Деякими * обгортками url. Список обгорток, що підтримуються сімейством
функцій [stat()](function.stat.md), дивіться у розділі [Підтримувані протоколи та обгортки](wrappers.md).

### Дивіться також

- [is_readable()](function.is-readable.md) - Визначає
існування файлу і чи доступний він для читання
- [is_writable()](function.is-writable.md) - Визначає, чи доступний
файл для запису
- [is_file()](function.is-file.md) - Визначає, чи є файл
звичайним файлом
- [file()](function.file.md) - Читає вміст файлу та поміщає
його в масив
- [SplFileInfo](class.splfileinfo.md)
