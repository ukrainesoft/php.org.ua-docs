Від'єднати спостерігача

-   [« SplSubject::attach](splsubject.attach.html)
    
-   [SplSubject::notify »](splsubject.notify.html)
    
-   [PHP Manual](index.html)
    
-   [SplSubject](class.splsubject.html)
    
-   Від'єднати спостерігача
    

# SplSubject::detach

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplSubject::detach — Від'єднати спостерігача

### Опис

```methodsynopsis
public SplSubject::detach(SplObserver $observer): void
```

Від'єднує спостерігача від суб'єкта, щоб більше не повідомляти його про оновлення.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`observer`

Об'єкт класу [SplObserver](class.splobserver.html) для від'єднання.

### Значення, що повертаються

Функція не повертає значення після виконання.