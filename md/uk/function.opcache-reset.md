Скидає вміст кешу опкодів

-   [« opcacheісscriptcached](function.opcache-is-script-cached.html)
    
-   [Контроль виведення »](book.outcontrol.md)
    
-   [PHP Manual](index.md)
    
-   [Функции OPcache](ref.opcache.md)
    
-   Скидає вміст кешу опкодів
    

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

-   [opcacheinvalidate()](function.opcache-invalidate.html) - анулює закешований скрипт