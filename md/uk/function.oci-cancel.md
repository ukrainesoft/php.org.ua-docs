---
navigation:
  - function.oci-bind-by-name.md: « ocibindбname
  - function.oci-client-version.md: ociclientversion »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ocicancel
---
# ocicancel

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocicancel — Закінчує процес читання з курсору

### Опис

```methodsynopsis
oci_cancel(resource $statement): bool
```

Скидає курсор, звільняючи всі пов'язані ресурси та скасовує можливість читати з нього.

### Список параметрів

`statement`

Запит OCI.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
