Перетворити DN на зручний для користувача формат іменування

-   [« ldap\_delete](function.ldap-delete.html)
    
-   [ldap\_err2str »](function.ldap-err2str.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
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