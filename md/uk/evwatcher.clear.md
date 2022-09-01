---
navigation:
  - class.evwatcher.md: « EvWatcher
  - evwatcher.construct.md: 'EvWatcher::construct »'
  - index.md: PHP Manual
  - class.evwatcher.md: EvWatcher
title: 'EvWatcher::clear'
---
# EvWatcher::clear

(PECL ev >= 0.2.0)

EvWatcher::clear — Очистити статус очікування спостерігача

### Опис

```methodsynopsis
public
   EvWatcher::clear(): int
```

Якщо спостерігач перебуває у стані pending, цей метод очищає його стан очікування та повертає його бітовий набір revents (якби була викликана його callback-функція). Якщо спостерігач не може очікувати, він нічого не робить і повертає **`0`**

Іноді може бути корисно "опитати" спостерігача, а не чекати на його callback-функцію, що може бути виконано за допомогою цієї функції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У випадку, якщо спостерігач перебуває в стані очікування, повертає бітовий набір revents, якби була викликана [callback-функция наблюдателя](ev.watcher-callbacks.md). В іншому випадку повертає **`0`**
