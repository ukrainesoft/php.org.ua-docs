---
navigation:
  - function.radius-request-authenticator.md: « radius\_request\_authenticator
  - function.radius-send-request.md: radius\_send\_request »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_salt\_encrypt\_attr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_salt\_encrypt\_attr

(PECL radius >= 1.3.0)

radius\_salt\_encrypt\_attr — Зашифровує значення за допомогою солі

### Опис

```methodsynopsis
radius_salt_encrypt_attr(resource $radius_handle, string $data): string|false
```

Застосовує алгоритм шифрування RADIUS до заданого значення.

Як правило, це робиться автоматично шляхом надання опції **`RADIUS_OPTION_SALT`** функцію встановлення атрибута, але цю функцію можна використовувати, якщо потрібно створення низькорівневого запиту.

### Список параметрів

`data`

Дані, які потрібно зашифрувати за допомогою солі.

### Значення, що повертаються

Повертає дані, зашифровані за допомогою солі або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [radius\_put\_addr()](function.radius-put-addr.md) \- Приєднує атрибут IP-адреси
-   [radius\_put\_attr()](function.radius-put-attr.md) \- приєднує бінарний атрибут
-   [radius\_put\_int()](function.radius-put-int.md) \- Приєднує цілісний атрибут
-   [radius\_put\_string()](function.radius-put-string.md) \- Приєднує рядковий атрибут
