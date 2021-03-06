- [« svn_blame](function.svn-blame.md)
- [svn_checkout »](function.svn-checkout.md)

- [PHP Manual](index.md)
- [Функції SVN](ref.svn.md)
- Повертає вміст файлу у репозиторії

# svn_cat

(PECL svn \>= 0.1.0)

svn_cat — Повертає вміст файлу у репозиторії

### Опис

**svn_cat**(string `$repos_url`, int `$revision_no` = ?): string

Повертає вміст по URL `repos_url` файлу в репозиторії за
станом на ревізію із номером `revision_no` (необов'язковий параметр).

### Список параметрів

`repos_url`
Шлях URL до елемента у репозиторії.

`revision_no`
Номер ревізії (ціле число) відповідного елемента, за замовчуванням -
HEAD (Остання ревізія).

### Значення, що повертаються

Повертає вміст елемента у репозиторії у разі успішного
завершення або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Простий приклад використання функції svn_cat()**

Цей приклад показує, як отримати вміст файлу ревізії 28:

` <?php$contents = svn_cat('http://www.example.com/svnroot/calc/gui.c', 28)?> `

### Примітки

**Увага**

Ця функція є ЕКСПЕРИМЕНТАЛЬНОЮ. Поведінка цієї функції, її ім'я
і документація, що відноситься до неї, можуть змінитися в наступних версіях
PHP без попередження. Використовуйте цю функцію на свій страх та ризик.

### Дивіться також

- **svn_list()**
- [» SVN-документація з svn cat](http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.cat.md)
