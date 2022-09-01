---
navigation:
  - splsubject.attach.md: '« SplSubject::attach'
  - splsubject.notify.md: 'SplSubject::notify »'
  - index.md: PHP Manual
  - class.splsubject.md: SplSubject
title: 'SplSubject::detach'
---
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

Об'єкт класу [SplObserver](class.splobserver.md) для від'єднання.

### Значення, що повертаються

Функція не повертає значення після виконання.
