Анулює закешований скрипт

-   [« opcache\_get\_status](function.opcache-get-status.html)
    
-   [opcache\_is\_script\_cached »](function.opcache-is-script-cached.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OPcache](ref.opcache.html)
    
-   Анулює закешований скрипт
    

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

-   [opcache\_compile\_file()](function.opcache-compile-file.html) - Скомпілювати та закешувати, але не виконувати скрипт PHP
-   [opcache\_reset()](function.opcache-reset.html) - скидає вміст кешу опкодів