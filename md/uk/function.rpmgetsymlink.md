---
navigation:
  - function.rpmdbsearch.md: « rpmdbsearch
  - function.rpminfo.md: rpminfo »
  - index.md: PHP Manual
  - ref.rpminfo.md: Функції RpmInfo
title: rpmgetsymlink
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rpmgetsymlink

(PECL rpminfo >= 1.1.0)

rpmgetsymlink — Отримує файл або директорію, на яку посилається символічне посилання

### Опис

```methodsynopsis
rpmgetsymlink(string $path, string $name): ?string
```

Отримує файл або директорію, на яку посилається символічне посилання.

### Список параметрів

`path`

Шлях до RPM-файлу.

`name`

Назва файлу символічного посилання.

### Значення, що повертаються

Повертає рядок (string) – мета символічного посилання, NULL при помилці, а якщо це не символічне посилання – порожній рядок.
