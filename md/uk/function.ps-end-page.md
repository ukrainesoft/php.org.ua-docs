Завершує сторінку

-   [« ps\_delete](function.ps-delete.html)
    
-   [ps\_end\_pattern »](function.ps-end-pattern.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Завершує сторінку
    

# псendpage

(PECL ps >= 1.1.0)

псendpage — Завершує сторінку

### Опис

```methodsynopsis
ps_end_page(resource $psdoc): bool
```

Завершує сторінку, яку було розпочато за допомогою [ps\_begin\_page()](function.ps-begin-page.html). Завершення сторінки призведе до виходу з поточного контексту малювання, який, наприклад, вимагає перезавантаження шрифтів, якщо вони завантажувалися на сторінці та налаштування багатьох інших параметрів малювання, таких як ширина лінії або колір.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_begin\_page()](function.ps-begin-page.html) - Починає нову сторінку