- [« svn_log](function.svn-log.md)
- [svn_mkdir »](function.svn-mkdir.md)

- [PHP Manual](index.md)
- [Функції SVN](ref.svn.md)
- Повертає список вмісту директорії репозиторію URL,
опціонально для конкретної ревізії

# svn_ls

(PECL svn \>= 0.1.0)

svn_ls — Повертає список вмісту директорії репозиторію URL,
опціонально для конкретної ревізії

### Опис

**svn_ls**(
string `$repos_url`,
int `$revision_no` = SVN_REVISION_HEAD,
bool `$recurse` = **`false`**,
bool `$peg` = **`false`**
): array

Ця функція будує запит на URL адресу репозиторію і отримує список
файлів та директорій, опціонально для конкретної ревізії. Це
еквівалентно команді SVN **`svn list $repos_url[@$revision_no]`**

> **Примітка**:
>
> Ця функція не працює з локальними робочими копіями репозиторію.
> Параметр `repos_url` *має* бути URL-адресою репозиторію.

### Список параметрів

`url`
URL-адреса репозиторію, наприклад **`http://www.example.com/svnroot`**.
Для доступу до локального репозиторію Subversion через файлову систему
використовуйте файлову URI-схему, наприклад
**`file:///home/user/svn-repos`**.

`revision`
Цілочисленний номер ревізії для отримання списку вмісту. Якщо
параметр опущений, використовується остання ревізія (HEAD).

`recurse`
Включає в себе рекурсивний запит.

### Значення, що повертаються

У разі успішного виконання ця функція повертає масив імен
файлів/директорій у форматі:

``` returnvaluescode
[0] => Array
(
[created_rev] => Номер останньої ревізії файлу/папки
[last_author] => Ім'я автора останньої редагування
[size] => Розмір файлу в байтах
[time] => Дата останньої зміни у форматі 'M d H:i'
або 'M d Y', залежно від того, скільки пройшло часу з останньої редагування.
[time_t] => позначка часу unix про останню зміну (ціле число)
[name] => ім'я файлу/директорії
[type] => тип, може приймати значення 'file' (файл) або 'dir' (директорія)
)
[1] => ...
````

### Приклади

**Приклад #1 Приклад використання **svn_ls()****

` <?phpprint_r( svn_ls('http://www.example.com/svnroot/') );?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => Array
(
[created_rev] => 20
[last_author] => Joe
[size] => 0
[time] => Apr 02 09:28
[time_t] => 1175520529
[name] => tags
[type] => dir
)
[1] => Array
(
[created_rev] => 23
[last_author] => Bob
[size] => 0
[time] => Apr 02 15:15
[time_t] => 1175541322
[name] => trunk
[type] => dir
)
)

### Примітки

**Увага**

Ця функція є ЕКСПЕРИМЕНТАЛЬНОЮ. Поведінка цієї функції, її ім'я
і документація, що відноситься до неї, можуть змінитися в наступних версіях
PHP без попередження. Використовуйте цю функцію на свій страх та ризик.

### Дивіться також

- [» SVN-документація з svn list](http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.list.md)
