Отримує об'єкт із слабким посиланням

-   [« WeakReference::create](weakreference.create.html)
    
-   [WeakMap »](class.weakmap.html)
    
-   [PHP Manual](index.html)
    
-   [WeakReference](class.weakreference.html)
    
-   Отримує об'єкт із слабким посиланням
    

# WeakReference::get

(PHP 7> = 7.4.0, PHP 8)

WeakReference::get — Отримує об'єкт із слабким посиланням

### Опис

```methodsynopsis
public WeakReference::get(): ?object
```

Отримує об'єкт із слабким посиланням. Якщо об'єкт вже було знищено, повертається **`null`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає посилання object або **`null`**, якщо об'єкт було знищено.