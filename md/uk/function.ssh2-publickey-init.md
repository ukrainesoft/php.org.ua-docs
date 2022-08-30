Ініціалізує підсистему відкритого ключа

-   [« ssh2publickeyadd](function.ssh2-publickey-add.html)
    
-   [ssh2publickeylist »](function.ssh2-publickey-list.html)
    
-   [PHP Manual](index.md)
    
-   [Функції SSH2](ref.ssh2.md)
    
-   Ініціалізує підсистему відкритого ключа
    

# ssh2publickeyinit

(PECL ssh2> = 0.10)

ssh2publickeyinit - Ініціалізує підсистему відкритого ключа

### Опис

```methodsynopsis
ssh2_publickey_init(resource $session): resource|false
```

Запитує підсистему відкритого ключа із вже відкритого з'єднання SSH2.

Підсистема відкритого ключа дозволяє авторизованому клієнту керувати списком авторизованих відкритих ключів, що зберігаються на сервері незалежно. Якщо віддалений сервер не підтримує підсистему відкритого ключа, функція **ssh2publickeyinit()** поверне **`false`**

### Список параметрів

`session`

### Значення, що повертаються

Повертає ресурс `подсистемы открытого ключа SSH2` (SSH2 Publickey Subsystem) для використання з іншими методами ssh2publickey() або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**: Підсистема відкритих ключів використовується для керування відкритими ключами на сервері, на якому клієнт *вже* пройшов авторизацію. Для авторизації за допомогою відкритого ключа на віддаленій системі, використовуйте натомість функцію [ssh2authpubkeyfile()](function.ssh2-auth-pubkey-file.html)

### Дивіться також

-   [ssh2publickeyadd()](function.ssh2-publickey-add.html) - Додає авторизований відкритий ключ
-   [ssh2publickeyremove()](function.ssh2-publickey-remove.html) - Видаляє авторизований відкритий ключ
-   [ssh2publickeylist()](function.ssh2-publickey-list.html) - Список вже авторизованих відкритих ключів