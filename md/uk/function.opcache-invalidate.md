---
navigation:
  - function.opcache-get-status.md: « opcachegetstatus
  - function.opcache-is-script-cached.md: opcacheісscriptcached »
  - index.md: PHP Manual
  - ref.opcache.md: Функции OPcache
title: opcacheinvalidate
---
# opcacheinvalidate

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL ZendOpcache >= 7.0.0)

opcacheinvalidate — Анулює закешований скрипт

### Опис

```methodsynopsis
opcache_invalidate(string $filename, bool $force = false): bool
```

Функція анулює закешований скрипт. Якщо параметр `force` не заданий або заданий як **`false`**, скрипт анулюється тільки якщо скрипт був модифікований після приміщення в кеш. Функція анулює лише кеш у пам'яті, не торкаючись файлового кешу.

### Список параметрів

`filename`

Шлях до сценарію.

`force`

Якщо встановлено як **`true`**, кеш скрипта буде примусово анульований незалежно від того, потрібно це чи ні

### Значення, що повертаються

Повертає **`true`**, якщо кеш опкодів для `filename` анульований, або якщо анулювати нічого. У випадку, якщо кеш опкодів вимкнено, повертається **`false`**

### Дивіться також

-   [opcachecompilefile()](function.opcache-compile-file.md) - Скомпілювати та закешувати, але не виконувати скрипт PHP
-   [opcachereset()](function.opcache-reset.md) - скидає вміст кешу опкодів
