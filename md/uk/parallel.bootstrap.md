Початкове завантаження

-   [« Функциональный API](functional.parallel.html)
    
-   [parallelrun »](parallel.run.html)
    
-   [PHP Manual](index.html)
    
-   [Функциональный API](functional.parallel.html)
    
-   Початкове завантаження
    

# parallelbootstrap

parallelbootstrap — Початкове завантаження

### Опис

```methodsynopsis
parallel\bootstrap(string $file): void
```

Повинен використовувати наданий `file` для початкового завантаження всіх середовищ виконання, створених для автоматичного планування за допомогою [parallelrun()](parallel.run.html)

### Список параметрів

`file`

Шлях до файлу для завантаження всіх середовищ виконання.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

**Увага**

Викидає parallelRuntimeErrorBootstrap, якщо цей процес був раніше викликаний.

**Увага**

Викидає parallelRuntimeErrorBootstrap, якщо викликається після [parallelrun()](parallel.run.html)

### Дивіться також

-   [parallelRuntime::run](parallel-runtime.run.html)