---
navigation:
  - libxml.requirements.md: « Вимоги
  - libxml.installation_old.md: Установка для PHP < 7.4 »
  - index.md: PHP Manual
  - libxml.setup.md: Встановлення та налаштування
title: Установка для PHP >= 7.4
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка для PHP >= 7.4

Модуль libxml включений за замовчуванням, але може бути вимкнений за умови вказівки директиви **\--without-libxml**

PHP використовує утиліту `pkg-config` для вибору правильного файлу бібліотеки, заголовних файлів та прапорів компіляції для роботи з модулем libxml2. Щоб переконатися, що вибрано бажану версію модуля libxml2, можна перед запуском сценарію налаштування через змінну оточення PKG\_CONFIG\_PATH вказати утиліту `pkg-config` шлях для пошуку потрібної версії модуля:

```
PKG_CONFIG_PATH="/path/to/libxml2/prefix/lib/pkgconfig:/lib/pkgconfig"
```
