---
navigation:
  - function.radius-demangle-mppe-key.md: « radiusdemanglemppekey
  - function.radius-get-attr.md: radiusgetattr »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiusdemangle
---
# radiusdemangle

(PECL radius >= 1.2.0)

radiusdemangle - Розшифровує дані

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

Повертає розшифрований рядок або **`false`** у разі виникнення помилки.
