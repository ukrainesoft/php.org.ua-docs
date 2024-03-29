---
navigation:
  - function.svn-client-version.md: « svn\_client\_version
  - function.svn-delete.md: svn\_delete »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svn\_commit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# svn\_commit

(PECL svn >= 0.1.0)

svn\_commit — Відправляє зміни з робочої директорії до репозиторію

### Опис

```methodsynopsis
svn_commit(string $log, array $targets, bool $recursive = true): array
```

Відправляє зміни у файлах локальної робочої копії, перелічені у масиві `targets`в репозиторий, с сообщением`log`. Директорії з масиву `targets` будуть рекурсивно додані, якщо параметр `recursive`не установлен в\*\*`false`\*\*

> **Зауваження**: Ця функція не має параметрів для встановлення даних аутентифікації, тому ім'я користувача та пароль мають бути задані за допомогою функції [svn\_auth\_set\_parameter()](function.svn-auth-set-parameter.md)

### Список параметрів

`log`

Рядок коментаря для поточної зміни.

`targets`

Масив із шляхами до локальних файлів або директорій, які будуть надіслані.

**Увага**

Параметр має бути масивом, рядкове значення додавання одиничного елемента не підтримується.

> **Зауваження**: Відносні шляхи будуть обчислені, якби поточна робоча директорія була домашньою папкою самого PHP Щоб використовувати робочу директорію скрипта, що викликає, використовуйте [realpath()](function.realpath.md)или dirname(\_\_FILE\_\_

`recursive`

Прапор для відключення рекурсивної відправки директорій з масиву `targets`По умолчанию\*\*`true`\*\*

### Значення, що повертаються

Повертає масив у форматі:

array( 0 => Номер ревізії зробленої зміни 1 => Рядок з датою та часом зміни у форматі ISO 8601 2 => Ім'я зміни, що зробив (коммітер) )

При неудаче операции возвращается\*\*`false`\*\*

### Приклади

**Приклад #1 Простий приклад**

Цей приклад відправляє директорію calculator в репозиторій, використовуючи ім'я користувача Bob і пароль abc123 (будемо сподіватися, що пароль надійний):

```php
<?php
svn_auth_set_parameter(SVN_AUTH_PARAM_DEFAULT_USERNAME, 'Bob');
svn_auth_set_parameter(SVN_AUTH_PARAM_DEFAULT_PASSWORD, 'abc123');
var_dump(svn_commit('Комментарий Bob\'а', array(realpath('calculator'))));
?>
```

Результат виконання наведеного прикладу:

```
array(
  0 => 1415,
  1 => '2007-05-26T01:44:28.453125Z',
  2 => 'Bob'
)
```

### Примітки

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

### Дивіться також

-   [svn\_auth\_set\_parameter()](function.svn-auth-set-parameter.md) \- Встановлює параметр автентифікації
-   [» SVN-документація з svn commit](http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.commit.md)
