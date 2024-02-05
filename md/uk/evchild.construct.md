---
navigation:
  - class.evchild.md: « EvChild
  - evchild.createstopped.md: 'EvChild::createStopped »'
  - index.md: PHP Manual
  - class.evchild.md: EvChild
title: 'EvChild::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvChild::\_\_construct

(PECL ev >= 0.2.0)

EvChild::\_\_construct — Створює спостерігач об'єкт evChild

### Опис

public**EvChild::\_\_construct**  
int`$pid`  
bool`$trace`  
[callable](language.types.callable.md) `$callback`  
[mixed](language.types.declarations.md#language.types.declarations.mixed) `$data` = **`null`**  
int`$priority` =  
) .

Створює об'єкт спостерігач [EvChild](class.evchild.md)

Викликає callback-функцію, коли настала подія зміни статусу процесу з ідентифікатором `pid` (або будь-яким *PID*, якщо `pid`задан как ). Статус процесу змінюється, коли процес завершується, або коли його вбивають, або якщо `trace` одно **`true`**, коли його зупинено або відновлено. Іншими словами, коли процес отримує сигнал **`SIGCHLD`** *Ev* отримує статус exit/wait для всіх змінених/зомбі дочірніх процесів і викликає callback-функцію.

Правильно встановлювати дочірнього спостерігача після того, як [EvChild](class.evchild.md) завершився, але до початку наступної ітерації подієвого циклу. Наприклад, спочатку викликається `fork`, після чого новий дочірній процес може вийти, і тільки після цього в батьків встановлюється спостерігач [EvChild](class.evchild.md)для нового*PID*

Ви можете отримати доступ до статусів exit/tracing та `pid` використовуючи властивості об'єкта спостерігача rstatus та rpid.

Кількість *PID*\-спостерігачів для кожного *PID* НЕ обмежено. Усіх їх буде викликано.

Метод[EvChild::createStopped()](evchild.createstopped.md) не стартує(не активує) створеного спостерігача.

### Список параметрів

`pid`

Очікує зміни статусу процесу з ідентифікатором PID (або будь-якого процесу, якщо PID заданий як

`trace`

Якщо \*\*`false`\*\*активація спостерігача відбувається тільки при завершенні процесу. Якщо \*\*`true`\*\*активація відбувається також при зупинці/відновленні процесу.

`callback`

Смотрите[Callback-функції спостерігачів](ev.watcher-callbacks.md)

`data`

Довільні дані, пов'язані зі спостерігачем.

`priority`

[Пріоритет спостерігача](class.ev.md#ev.constants.watcher-pri)

### Дивіться також

-   [EvLoop::child()](evloop.child.md) \- Створює об'єкт EvChild, пов'язаний із поточним циклом подій
