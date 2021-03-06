- [« svn_fs_youngest_rev](function.svn-fs-youngest-rev.md)
- [svn_log »](function.svn-log.md)

- [PHP Manual](index.md)
- [Функції SVN](ref.svn.md)
- Імпорт шляху без версії до репозиторії

# svn_import

(PECL svn \>= 0.2.0)

svn_import — Імпорт шляху без версії до репозиторії

### Опис

**svn_import**(string `$path`, string `$url`, bool `$nonrecursive`):
bool

Додавання неверсіонованого шляху `path` до репозиторію за адресою
`url`. Якщо `path` є директорією і параметр `nonrecursive` має
значення **`false`**, директорія буде додана до репозиторію
рекурсивно.

### Список параметрів

`path`
Шлях до файлу або каталогу для імпорту.

> **Примітка**: Відносні шляхи будуть обчислені, наче поточна
> робоча директорія була домашньою папкою самого PHP. Щоб
> використовувати робочу директорію скрипта, що викликає, використовуйте
> [realpath()](function.realpath.md) або dirname(\_\_FILE\_\_).

`url`
URL-адреса репозиторію.

`nonrecursive`
Чи слід обробити директорії рекурсивно чи ні.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Простий приклад**

Цей приклад ілюструє базове використання цієї функції. Імпорт
директорії з ім'ям `new-files` у репозиторій з адресою
` http://www.example.com/svnroot/incoming/abc` виглядає наступним
чином:

` <?phpsvn_import(realpath('new-files'), 'http://www.example.com/svnroot/incoming/abc', false);?> `

### Примітки

**Увага**

Ця функція є ЕКСПЕРИМЕНТАЛЬНОЮ. Поведінка цієї функції, її ім'я
і документація, що відноситься до неї, можуть змінитися в наступних версіях
PHP без попередження. Використовуйте цю функцію на свій страх та ризик.

### Дивіться також

- [svn_add()](function.svn-add.md) - Додає елементи до списку
запланованих для додавання до робочої копії
- [» SVN-документація з svn import](http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.import.md)
