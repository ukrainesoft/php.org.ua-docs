---
navigation:
  - function.ldap-mod_add-ext.md: « ldap\_mod\_add\_ext
  - function.ldap-mod_del-ext.md: ldap\_mod\_del\_ext »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_mod\_add
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_mod\_add

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_mod\_add — Додати значення атрибуту до поточних атрибутів

### Опис

```methodsynopsis
ldap_mod_add(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): bool
```

Додає один або більше атрибутів до зазначеного `dn`. Щоб додати повноцінний новий об'єкт, використовуйте [ldap\_add()](function.ldap-add.md)

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`dn`

Відмінне ім'я об'єкта LDAP.

`entry`

Асоціативний масив зі списком значень атрибутів, що додаються. Якщо який-небудь атрибут ще не існує, він буде доданий. Якщо атрибут вже існує, ви можете лише додати до нього значення, якщо він підтримує множинні значення.

`controls`

Массив[керуючих констант LDAP](ldap.controls.md)для отправки в запросе.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.0.0 | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
| 7.3.0 | Додано підтримку параметра `controls` |

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [ldap\_mod\_add\_ext()](function.ldap-mod_add-ext.md) \- Додати значення атрибуту до поточних атрибутів
-   [ldap\_mod\_del()](function.ldap-mod-del.md) \- Видалити значення атрибута із поточних атрибутів
-   [ldap\_mod\_replace()](function.ldap-mod-replace.md) \- Замінити значення атрибутів на нові
-   [ldap\_modify\_batch()](function.ldap-modify-batch.md) \- Формування та запуск пакетної зміни запису LDAP
