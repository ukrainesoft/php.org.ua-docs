Отримати оновлення від суб'єкта

-   [« SplObserver](class.splobserver.html)
    
-   [SplSubject »](class.splsubject.html)
    
-   [PHP Manual](index.html)
    
-   [SplObserver](class.splobserver.html)
    
-   Отримати оновлення від суб'єкта
    

# SplObserver::update

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplObserver::update — Отримати поновлення від суб'єкта

### Опис

```methodsynopsis
public SplObserver::update(SplSubject $subject): void
```

Цей метод викликається, коли будь-який [SplSubject](class.splsubject.html), до якого приєднано спостерігача, викликає [SplSubject::notify()](splsubject.notify.html)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`subject`

[SplSubject](class.splsubject.html), що повідомляє спостерігача про оновлення.

### Значення, що повертаються

Функція не повертає значення після виконання.