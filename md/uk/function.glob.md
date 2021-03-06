- [«fwrite](function.fwrite.md)
- [is_dir »](function.is-dir.md)

- [PHP Manual](index.md)
- [Функції файлової системи](ref.filesystem.md)
- Знаходить файлові шляхи, що збігаються із шаблоном

# glob

(PHP 4 \>= 4.3.0, PHP 5, PHP 7, PHP 8)

glob — Знаходить файлові шляхи, що збігаються із шаблоном

### Опис

**glob**(string `$pattern`, int `$flags` = 0): array\|false

Функція **glob()** шукає всі шляхи, що збігаються із шаблоном `pattern`
згідно з правилами, що використовуються у функції glob() бібліотеки libc,
які схожі на правила, що використовуються більшістю поширених
оболонок.

### Список параметрів

`pattern`
Візерунок. Не відбувається розкриття тильди та встановлення параметрів.

Спеціальні символи:

- `*` - Відповідає нулю або більшій кількості символів.
- `?` - Відповідає рівно одному символу (будь-якому символу).
- `[...]` - Відповідає одному символу із групи. Якщо перший
символ `!`, то відповідає будь-якому символу, що не входить до групи
- `\` - Екранує наступний символ, крім випадків, коли
використовується прапор **GLOB_NOESCAPE**.

`flags`
Допустимі прапори:

- **`GLOB_MARK`** - Додає слєш (зворотний слєш у Windows) до кожної
директорії, що повертається.
- **`GLOB_NOSORT`** - Повертає файли у тому вигляді, в якому вони
утримуються в директорії (без сортування). Якщо цей прапор не вказано,
то імена сортуються за абеткою.
- **`GLOB_NOCHECK`** - Повертає шаблон пошуку, якщо за його допомогою
не було знайдено жодного файлу.
- **`GLOB_NOESCAPE`** - Зворотні сліші не екранують метасимволи.
- **`GLOB_BRACE`** - Розкриває {a,b,c} для збігу з 'a', 'b' або
'c'.
- **`GLOB_ONLYDIR`** - Повертає тільки директорії, що збігаються з
шаблон.
- **`GLOB_ERR`** - Зупиняється при помилках читання (наприклад,
директорії без права читання), за промовчанням помилки ігноруються.

> **Примітка**: Прапор **`GLOB_BRACE`** недоступний на деяких не
> GNU-системи, наприклад, Solaris або Alpine Linux.

### Значення, що повертаються

Повертає масив, який містить файли/директорії, що збігаються, порожній
масив у разі відсутності збігу або **`false`** у разі помилки.

> **Примітка**:
>
> На деяких системах неможливо відрізнити відсутність збігу та
> помилки.

### Приклади

**Приклад #1 Зручний спосіб, як за допомогою **glob()** можна замінити
[opendir()](function.opendir.md) та її аналоги.**

` <?phpforeach (glob("*.txt") as $filename) {    echo "$filename розмір " . filesize($filename) . "
";}?> `

Результатом виконання цього прикладу буде щось подібне:

funclist.txt розмір 44686
funcsummary.txt розмір 267625
quickref.txt розмір 137820

### Примітки

> **Примітка**: Ця функція не застосовується для роботи з [віддаленими > файлами](features.remote-files.md), оскільки файл має бути
> доступний через файлову систему сервера.

> **Примітка**: Функція недоступна на деяких системах (наприклад,
> Старий Sun OS).

### Дивіться також

- [opendir()](function.opendir.md) - Відкриває дескриптор каталогу
- [readdir()](function.readdir.md) - Отримує елемент каталогу
його дескриптору
- [closedir()](function.closedir.md) - Закриває дескриптор каталогу
- [fnmatch()](function.fnmatch.md) - Перевіряє збіг імені
файлу із шаблоном
