---
navigation:
  - function.opcache-is-script-cached.md: « opcacheісscriptcached
  - book.outcontrol.md: Контроль виведення »
  - index.md: PHP Manual
  - ref.opcache.md: Функции OPcache
title: opcachereset
---
# opcachereset

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL ZendOpcache >= 7.0.0)

opcachereset — Скидає вміст кешу опкодів

### Опис

```methodsynopsis
opcache_reset(): bool
```

Функція скидає весь кеш. Після виклику **opcachereset()** всі скрипти будуть заново завантажені, скомпільовані та поміщені в кеш після їхнього наступного виклику. Функція скидає лише кеш у пам'яті, не торкаючись файлового кешу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо кеш скинутий або \*\*`false`\*\*якщо не використовується.

### Дивіться також

-   [opcacheinvalidate()](function.opcache-invalidate.md) - анулює закешований скрипт
