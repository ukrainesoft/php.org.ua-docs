---
navigation:
  - class.splsubject.md: « SplSubject
  - splsubject.detach.md: 'SplSubject::detach »'
  - index.md: PHP Manual
  - class.splsubject.md: SplSubject
title: 'SplSubject::attach'
---
# SplSubject::attach

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplSubject::attach — Приєднати спостерігача (об'єкт класу SplObserver)

### Опис

```methodsynopsis
public SplSubject::attach(SplObserver $observer): void
```

Приєднує [SplObserver](class.splobserver.md), щоб він міг отримувати сповіщення про оновлення.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`observer`

Об'єкт класу [SplObserver](class.splobserver.md) для приєднання.

### Значення, що повертаються

Функція не повертає значення після виконання.
