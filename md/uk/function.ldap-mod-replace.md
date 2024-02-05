---
navigation:
  - function.ldap-mod_replace-ext.md: « ldap\_mod\_replace\_ext
  - function.ldap-modify-batch.md: ldap\_modify\_batch »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_mod\_replace
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_mod\_replace

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_mod\_replace — Замінити значення атрибутів на нові

### Опис

```methodsynopsis
ldap_mod_replace(    LDAP\Connection $ldap,    string $dn,    array $entry,    ?array $controls = null): bool
```

Замінює один або більше атрибутів із зазначеного `dn`. Також її можна використовувати для видалення чи додавання атрибутів.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`dn`

Відмінне ім'я об'єкта LDAP.

`entry`

Асоціативний масив зі списком атрибутів, що замінюються. Якщо встановити порожній масив, то атрибут буде видалений. Якщо якийсь атрибут відсутній, він буде доданий.

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

-   [ldap\_mod\_replace\_ext()](function.ldap-mod_replace-ext.md) \- Замінити значення атрибута на нові
-   [ldap\_mod\_del()](function.ldap-mod-del.md) \- Видалити значення атрибута із поточних атрибутів
-   [ldap\_mod\_add()](function.ldap-mod-add.md) \- Додати значення атрибуту до поточних атрибутів
-   [ldap\_modify\_batch()](function.ldap-modify-batch.md) \- Формування та запуск пакетної зміни запису LDAP
