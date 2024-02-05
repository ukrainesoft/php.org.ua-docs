---
navigation:
  - function.radius-demangle-mppe-key.md: « radius\_demangle\_mppe\_key
  - function.radius-get-attr.md: radius\_get\_attr »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_demangle
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_demangle

(PECL radius >= 1.2.0)

radius\_demangle - Розшифровує дані

### Опис

```methodsynopsis
radius_demangle(resource $radius_handle, string $mangled): string
```

Деякі дані (паролі, MS-CHAPv1 MPPE-ключі) спотворені з міркувань безпеки та їх необхідно розшифрувати, перш ніж ви зможете їх використовувати.

### Список параметрів

`radius_handle`

Ресурс RADIUS

`mangled`

Спотворені дані, які потрібно розшифрувати.

### Значення, що повертаються

Повертає розшифрований рядок або \*\*`false`\*\*в случае возникновения ошибки.
