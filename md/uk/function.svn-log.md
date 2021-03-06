- [« svn_import](function.svn-import.md)
- [svn_ls »](function.svn-ls.md)

- [PHP Manual](index.md)
- [Функції SVN](ref.svn.md)
- Повертає коментарі до правок у репозиторії

# svn_log

(PECL svn \>= 0.1.0)

svn_log — Повертає коментарі до редагування в репозиторії

### Опис

**svn_log**(
string `$repos_url`,
int `$start_revision` = ?,
int `$end_revision` = ?,
int `$limit` = 0,
int `$flags` = SVN_DISCOVER_CHANGED_PATHS \| SVN_STOP_ON_COPY
): array

**svn_log()** повертає повну історію змін конкретного елемента
репозиторія, розташованого за URL `repos_url`, або історію правок
конкретному діапазоні, якщо вказано параметр start_revision. Дана
функція еквівалентна команді SVN
**`svn log --verbose -r $start_revision $repos_url`**.

### Список параметрів

`repos_url`
URL-адреса репозиторію для отримання історії правок елемента.

`start_revision`
Початковий номер ревізії для отримання. Використовуйте константу
**`SVN_REVISION_HEAD`** для отримання останньої ревізії.

`end_revision`
Кінцевий номер ревізії для отримання. За замовчуванням під час використання
параметра `start_revision` ідентичний йому, інакше дорівнює
**`SVN_REVISION_INITIAL`**.

`limit`
Кількість записів для отримання.

`flags`
Будь-яка комбінація **`SVN_OMIT_MESSAGES`**,
**`SVN_DISCOVER_CHANGED_PATHS`** та **`SVN_STOP_ON_COPY`**.

### Значення, що повертаються

У разі успішного виконання функція повертає масив формату:

``` returnvaluescode
[0] => Масив, відсортований спочатку найостаннішої (найбільшої) ревізії
(
[rev] => Номер ревізії (ціле число)
[author] => Автор правки (рядок)
[msg] => Коментар до змін (рядок)
[date] => Дата редагування у форматі ISO 8601, тобто. date('c')
[paths] => Масив із шляхами до змінених файлів
(
[0] => Array
(
[action] => Позначення характеру змін
[path] => Абсолютний шлях репозиторію до зміненого файлу
)
[1] => ...
)
)
[1] => ...
````

> **Примітка**:
>
> Висновок завжди представлений як пронумерований масив, що містить
> масиви, крім випадків відсутності або лише єдиного екземпляра
> Ревізії.

Значення `action` є підмножиною [» перших літер станів SVN](http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.status.md), де
можливі значення – це:

| Літера | Опис                  |
|--------|-----------------------|
| M      | Елемент змінено       |
| A      | Елемент було додано   |
| D      | Елемент було видалено |
| R      | Елемент замінили      |

**Дії**

Якщо змін елемента немає, повертається порожній масив.

### Приклади

**Приклад #1 Приклад використання **svn_log()****

` <?phpprint_r( svn_log('http://www.example.com/', 23) );?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => Array
(
[rev] => 23
[author] => 'joe'
[msg] => 'До нашого бутерброду додані сир та ковбаса.'
[date] => '2007-04-06T16:00:27-04:00'
[paths] => Array
(
[0] => Array
(
[action] => 'M'
[path] => '/sandwich.txt'
)
)
)
)

### Примітки

**Увага**

Ця функція є ЕКСПЕРИМЕНТАЛЬНОЮ. Поведінка цієї функції, її ім'я
і документація, що відноситься до неї, можуть змінитися в наступних версіях
PHP без попередження. Використовуйте цю функцію на свій страх та ризик.

### Дивіться також

- [»  SVN-документація за командою svn log](http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.log.md)
