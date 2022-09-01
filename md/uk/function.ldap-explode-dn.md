---
navigation:
  - function.ldap-exop.html: « ldapexop
  - function.ldap-first-attribute.html: ldapfirstattribute »
  - index.html: PHP Manual
  - ref.ldap.html: Функції LDAP
title: ldapexplodeдн
---
# ldapexplodeдн

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapexplodedn — Розділити DN на його складові

### Опис

```methodsynopsis
ldap_explode_dn(string $dn, int $with_attrib): array|false
```

Поділяє DN, повернутий функцією [ldapgetdn()](function.ldap-get-dn.md)і розбиває його на складові. Кожна частина відома як відносне ім'я або RDN.

### Список параметрів

`dn`

Відмінна назва об'єкта LDAP.

`with_attrib`

Використовується для запиту, якщо RDNs повернені лише зі значеннями або з їх атрибутами. Для отримання RDN з атрибутами (тобто у форматі attribute=value) встановіть параметр `with_attrib` в 0 та для отримання лише значень встановіть його у 1.

### Значення, що повертаються

Повертає масив усіх компонентів DN або **`false`** у разі виникнення помилки. Перший елемент у цьому масиві має ключ `count`, і він є число повернених значень. Наступні елементи – це компоненти DN із цифровими індексами.
