Серіалізує одне значення всередині пакету WDDX

-   [« wddx\_packet\_start](function.wddx-packet-start.html)
    
-   [wddx\_serialize\_vars »](function.wddx-serialize-vars.html)
    
-   [PHP Manual](index.html)
    
-   [Функции WDDX](ref.wddx.html)
    
-   Серіалізує одне значення всередині пакету WDDX
    

# wddxserializevalue

(PHP 4, PHP 5, PHP 7)

wddxserializevalue - Серіалізує одне значення всередині пакету WDDX

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 7.4.0.

### Опис

```methodsynopsis
wddx_serialize_value(mixed $var, string $comment = ?): string
```

Створює пакет WDDX з заданого значення.

### Список параметрів

`var`

Значення для серіалізації

`comment`

Необов'язковий рядок із коментарем, який відображається в заголовку пакета.

### Значення, що повертаються

Повертає пакет WDDX або **`false`** у разі виникнення помилки.