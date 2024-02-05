---
navigation:
  - function.svn-cat.md: « svn\_cat
  - function.svn-cleanup.md: svn\_cleanup »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svn\_checkout
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# svn\_checkout

(PECL svn >= 0.1.0)

svn\_checkout — Отримує робочу копію з репозиторію

### Опис

```methodsynopsis
svn_checkout(    string $repos,    string $targetpath,    int $revision = ?,    int $flags = 0): bool
```

Отримує робочу копію з ревізією `revision`из репозитория`repos` і розміщує в `targetpath`

### Список параметрів

`repos`

Шлях (URL) до директорії, яку потрібно отримати з репозиторію.

`targetpath`

Локальний шлях, куди потрібно отримати робочу копію.

> **Зауваження**: Відносні шляхи будуть обчислені, якби поточна робоча директорія була домашньою папкою самого PHP Щоб використовувати робочу директорію скрипта, що викликає, використовуйте [realpath()](function.realpath.md)или dirname(\_\_FILE\_\_

`revision`

Номер ревізії (ціле число), яку потрібно отримати. За замовчуванням HEAD, тобто. найновіша версія.

`flags`

Комбинации из констант\*\*`SVN_NON_RECURSIVE`**и**`SVN_IGNORE_EXTERNALS`\*\*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Простий приклад**

Цей приклад показує, як отримати директорію з репозиторію до папки calc:

```php
<?php
svn_checkout('http://www.example.com/svnroot/calc/trunk', dirname(__FILE__) . '/calc');
?>
```

Вираз `dirname(__FILE__)` використовується для перетворення з відносного шляху calc в абсолютний шлях. Якщо calc існує, можна використовувати [realpath()](function.realpath.md)для получения абсолютного пути.

### Примітки

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

### Дивіться також

-   [svn\_add()](function.svn-add.md) \- Додає елементи до списку запланованих для додавання до робочої копії
-   [svn\_commit()](function.svn-commit.md) \- Відправляє зміни з робочої директорії до репозиторію
-   [svn\_status()](function.svn-status.md) \- Повертає SVN-статус файлів та директорій робочої копії
-   [svn\_update()](function.svn-update.md) \- Оновлює робочу копію
-   [» SVN-документація про команду svn checkout](http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.checkout.md)
