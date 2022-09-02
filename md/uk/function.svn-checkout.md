---
navigation:
  - function.svn-cat.md: « svncat
  - function.svn-cleanup.md: svncleanup »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svncheckout
---
# svncheckout

(PECL svn> = 0.1.0)

svncheckout — Отримує робочу копію з репозиторію

### Опис

```methodsynopsis
svn_checkout(    string $repos,    string $targetpath,    int $revision = ?,    int $flags = 0): bool
```

Отримує робочу копію з ревізією `revision` з репозиторію `repos` і розміщує в `targetpath`

### Список параметрів

`repos`

Шлях (URL) до директорії, яку потрібно отримати з репозиторію.

`targetpath`

Локальний шлях, куди потрібно отримати робочу копію.

> **Зауваження**: Відносні шляхи будуть обчислені, якби поточна робоча директорія була домашньою папкою самого PHP Щоб використовувати робочу директорію скрипта, що викликає, використовуйте [realpath()](function.realpath.md) або dirname(FILE

`revision`

Номер ревізії (ціле число), яку потрібно отримати. За замовчуванням HEAD, тобто. найновіша версія.

`flags`

Комбінації із констант **`SVN_NON_RECURSIVE`** і **`SVN_IGNORE_EXTERNALS`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Простий приклад**

Цей приклад показує, як отримати директорію з репозиторію до папки calc:

```php
<?php
svn_checkout('http://www.example.com/svnroot/calc/trunk', dirname(__FILE__) . '/calc');
?>
```

Вираз `dirname(__FILE__)` використовується для перетворення з відносного шляху calc в абсолютний шлях. Якщо calc існує, можна використовувати [realpath()](function.realpath.md) для здобуття абсолютного шляху.

### Примітки

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

### Дивіться також

-   [svnadd()](function.svn-add.md) - Додає елементи до списку запланованих для додавання до робочої копії
-   [svncommit()](function.svn-commit.md) - Відправляє зміни з робочої директорії до репозиторію
-   [svnstatus()](function.svn-status.md) - Повертає SVN-статус файлів та директорій робочої копії
-   [svnupdate()](function.svn-update.md) - Оновлює робочу копію
-   [» SVN-документация о команде svn checkout](http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.checkout.md)
