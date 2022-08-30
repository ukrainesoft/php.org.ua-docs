Отримати оновлення від суб'єкта

-   [« SplObserver](class.splobserver.md)
    
-   [SplSubject »](class.splsubject.md)
    
-   [PHP Manual](index.md)
    
-   [SplObserver](class.splobserver.md)
    
-   Отримати оновлення від суб'єкта
    

# SplObserver::update

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplObserver::update — Отримати поновлення від суб'єкта

### Опис

```methodsynopsis
public SplObserver::update(SplSubject $subject): void
```

Цей метод викликається, коли будь-який [SplSubject](class.splsubject.md), до якого приєднано спостерігача, викликає [SplSubject::notify()](splsubject.notify.md)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`subject`

[SplSubject](class.splsubject.md), що повідомляє спостерігача про оновлення.

### Значення, що повертаються

Функція не повертає значення після виконання.