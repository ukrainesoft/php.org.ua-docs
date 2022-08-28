Повертає параметр автентифікації

-   [« svn\_add](function.svn-add.html)
    
-   [svn\_auth\_set\_parameter »](function.svn-auth-set-parameter.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SVN](ref.svn.html)
    
-   Повертає параметр автентифікації
    

# svnauthgetparameter

(PECL svn >= 0.1.0)

svnauthgetparameter — Повертає параметр автентифікації

### Опис

```methodsynopsis
svn_auth_get_parameter(string $key): string
```

Повертає параметр аутентифікації за ключем `key`. Список можливих ключів та їх значень доступний у [списке констант аутентификации](svn.constants.html#svn.constants.auth)

### Список параметрів

`key`

Ім'я ключа (рядок). Щоб вказати ключ, використовуйте [список констант аутентификации](svn.constants.html#svn.constants.auth), Визначений даним модулем.

### Значення, що повертаються

Повертає значення параметра за ключем `key` у вигляді рядка, або **`null`**якщо параметр не існує.

### Примітки

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

### Дивіться також

-   [svn\_auth\_set\_parameter()](function.svn-auth-set-parameter.html) - Встановлює параметр автентифікації
-   [Константы аутентификации](svn.constants.html#svn.constants.auth)