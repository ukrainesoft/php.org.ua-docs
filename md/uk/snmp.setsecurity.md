---
navigation:
  - snmp.set.md: '« SNMP::set'
  - snmp.walk.md: 'SNMP::walk »'
  - index.md: PHP Manual
  - class.snmp.md: SNMP
title: 'SNMP::setSecurity'
---
# SNMP::setSecurity

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SNMP::setSecurity — Налаштовує пов'язані з безпекою параметри сесії SNMPv3

### Опис

```methodsynopsis
public SNMP::setSecurity(    string $securityLevel,    string $authProtocol = "",    string $authPassphrase = "",    string $privacyProtocol = "",    string $privacyPassphrase = "",    string $contextName = "",    string $contextEngineId = ""): bool
```

setSecurity налаштовує пов'язані з безпекою параметри сесії, що використовуються у протоколі SNMP версії 3

### Список параметрів

`securityLevel`

рівень безпеки (noAuthNoPriv|authNoPriv|authPriv)

`authProtocol`

протокол аутентифікації (MD5 або SHA)

`authPassphrase`

пароль автентифікації

`privacyProtocol`

протокол конфіденційності (DES або AES)

`privacyPassphrase`

пароль конфіденційності

`contextName`

ім'я контексту

`contextEngineId`

контекст EngineID

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SNMP::setSecurity()****

```php
<?php
  $session = new SNMP(SNMP::VERSION_3, $hostname, $rwuser, $timeout, $retries);
  $session->setSecurity('authPriv', 'MD5', $auth_pass, 'AES', $priv_pass, '', 'aeeeff');
?>
```

### Дивіться також

-   [SNMP::construct()](snmp.construct.md) - Створює екземпляр SNMP, що представляє сесію віддаленого агента SNMP
