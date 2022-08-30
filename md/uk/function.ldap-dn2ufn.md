Перетворити DN на зручний для користувача формат іменування

-   [« ldapdelete](function.ldap-delete.html)
    
-   [ldaperr2str »](function.ldap-err2str.html)
    
-   [PHP Manual](index.html)
    
-   [Функції LDAP](ref.ldap.html)
    
-   Перетворити DN на зручний для користувача формат іменування
    

# ldapdn2ufn

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapdn2ufn — Перетворити DN на зручний для користувача формат іменування

### Опис

```methodsynopsis
ldap_dn2ufn(string $dn): string|false
```

Перемикає вказаний `dn` більш зручну для користувача форму, знімаючи ізоляцію з імен типів.

### Список параметрів

`dn`

Відмінна назва об'єкта LDAP.

### Значення, що повертаються

Повертає зручне для користувача ім'я або **`false`** у разі виникнення помилки.