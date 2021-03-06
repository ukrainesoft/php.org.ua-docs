- [«ldap_dn2ufn](function.ldap-dn2ufn.md)
- [ldap_errno»](function.ldap-errno.md)

- [PHP Manual](index.md)
- [Функції LDAP](ref.ldap.md)
- Перетворити код помилки LDAP на рядкове повідомлення про помилку

#ldap_err2str

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap_err2str — Перетворити код помилки LDAP на рядкове повідомлення про
помилці

### Опис

**ldap_err2str**(int `$errno`): string

Повертає рядкове повідомлення про помилку, що пояснює код помилки
`errno`. У той час як LDAP числа errno стандартизовані, різні
бібліотеки повертають різні або навіть локалізовані текстові
повідомлення про помилки. Ніколи не перевіряйте на певний текст
повідомлення про помилку завжди використовуйте коди помилок для перевірки.

### Список параметрів

`errno`
Номер помилки.

### Значення, що повертаються

Повертає повідомлення помилки у вигляді рядка.

### Приклади

**Приклад #1 Перелік усіх повідомлень про помилки LDAP**

` <?php for|($i=0;$i<100;$i++) {    printf("Помилка $i: %s<br />
", ldap_err2str($i));  }?> `

### Дивіться також

- [ldap_errno()](function.ldap-errno.md) - Повернути номер помилки
LDAP останньої команди
- [ldap_error()](function.ldap-error.md) - Повернути повідомлення про
помилка LDAP останньої команди
