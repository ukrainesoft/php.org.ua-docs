---
navigation:
  - function.ldap-parse-result.md: « ldap\_parse\_result
  - function.ldap-rename-ext.md: ldap\_rename\_ext »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_read
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_read

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_read — Читає запис

### Опис

```methodsynopsis
ldap_read(    LDAP\Connection|array $ldap,    array|string $base,    array|string $filter,    array $attributes = [],    int $attributes_only = 0,    int $sizelimit = -1,    int $timelimit = -1,    int $deref = LDAP_DEREF_NEVER,    ?array $controls = null): LDAP\Result|array|false
```

Виконує пошук для вказаного `filter` у директорії в рамках **`LDAP_SCOPE_BASE`**. Еквівалентно читання запису з директорії.

Можна також виконувати паралельний пошук. У цьому випадку першим аргументом має бути масив екземплярів [LDAP\\Connection](class.ldap-connection.md), а чи не один екземпляр. Якщо пошук не повинен використовувати один і той же базовий DN і фільтр, як аргументи можна передати масив базових DN і/або масив фільтрів. Кількість елементів у масивах має збігатися з кількістю екземплярів [LDAP\\Connection](class.ldap-connection.md)оскільки перші записи масивів використовуються для одного пошуку, другі — для іншого і так далі. При паралельному пошуку повертається масив екземплярів [LDAP\\Result](class.ldap-result.md), за исключением возникновения ошибки, когда возвращается значение\*\*`false`\*\*

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`base`

Базове DN для каталогу.

`filter`

Порожній фільтр не допустимо. Якщо потрібно отримати абсолютно всю інформацію для цього запису, використовуйте фільтр `objectClass=*`. Якщо відомо, які типи запису використовуються на сервері каталогів, то можна використовувати відповідний фільтр, такий як `objectClass=inetOrgPerson`

`attributes`

Масив необхідних атрибутів, наприклад, `array("mail", "sn", "cn")`. . Зауважте, що "dn" завжди повертається, незалежно від того, які типи атрибутів потрібні.

Використання цього параметра набагато ефективніше, ніж дія за умовчанням (яка повертає всі атрибути та їх значення). Тому використання цього параметра слід вважати гарною практикою.

`attributes_only`

Повинен дорівнювати 1, тільки якщо потрібні типи атрибута. Якщо дорівнює 0, то, за умовчанням, вибираються типи атрибутів і значення.

`sizelimit`

Дозволяє обмежити кількість вибраних записів. Встановлення цього параметра дорівнює 0 означає, що обмеження відсутнє.

> **Зауваження** :
> 
> Цей параметр НЕ може перевизначати попереднє встановлення sizelimit на стороні сервера. Хоча його можна встановити нижче.
> 
> Деякі хости серверів каталогів будуть налаштовані так, щоб повернути не більше, ніж попередньо встановлена ​​кількість записів. Якщо це станеться, сервер вкаже, що тільки повернув частковий набір результатів. Це також відбувається, якщо використовується цей параметр, щоб обмежити кількість вибраних записів.

`timelimit`

Встановлює кількість секунд, що обмежує процес пошуку. Встановлення цього параметра дорівнює 0 означає, що обмеження відсутнє.

> **Зауваження** :
> 
> Цей параметр НЕ може перевизначати передустановку timelimit на стороні сервера. Хоча його можна встановити нижче.

`deref`

Визначає те, як псевдоніми мають бути опрацьовані під час пошуку. Може бути одним із наступних:

-   \*\*`LDAP_DEREF_NEVER`\*\*- (за умовчанням) псевдоніми ніколи не розіменовуються.
-   \*\*`LDAP_DEREF_SEARCHING`\*\*- псевдоніми мають бути розіменовані під час пошуку, але не при визначенні розташування базового об'єкта пошуку.
-   \*\*`LDAP_DEREF_FINDING`\*\*- псевдоніми мають бути розіменовані щодо місця розташування базового об'єкта, але з під час пошуку.
-   \*\*`LDAP_DEREF_ALWAYS`\*\*- псевдоніми повинні завжди розіменовуватись.

`controls`

Массив[керуючих констант LDAP](ldap.controls.md)для отправки в запросе.

### Значення, що повертаються

Повертає екземпляр [LDAP\\Result](class.ldap-result.md), масив екземплярів [LDAP\\Result](class.ldap-result.md)или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Повертає екземпляр [LDAP\\Result](class.ldap-result.md); раніше повертався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
| 4.0.5 | Було додано підтримку паралельного пошуку. Для більш детальної інформації дивіться [ldap\_search()](function.ldap-search.md) |
| 7.3.0 | Додано підтримку параметра `controls` |
