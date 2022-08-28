Створює об'єкт спостерігач EvChild

-   [« EvChild](class.evchild.html)
    
-   [EvChild::createStopped »](evchild.createstopped.html)
    
-   [PHP Manual](index.html)
    
-   [EvChild](class.evchild.html)
    
-   Створює об'єкт спостерігач EvChild
    

# EvChild::construct

(PECL ev >= 0.2.0)

EvChild::construct — Створює спостерігач об'єкт evChild

### Опис

public **EvChild::construct**  
int `$pid`  
bool `$trace`  
[callable](language.types.callable.html) `$callback`  
[mixed](language.types.declarations.html#language.types.declarations.mixed) `$data` **`null`**  
int `$priority`  

Створює об'єкт спостерігач [EvChild](class.evchild.html)

Викликає callback-функцію, коли настала подія зміни статусу процесу з ідентифікатором `pid` (або будь-яким *PID*, якщо `pid` заданий як **`0`** ). Статус процесу змінюється, коли процес завершується, або коли його вбивають, або якщо `trace` одно **`true`**, коли його зупинено або відновлено. Іншими словами, коли процес отримує сигнал **`SIGCHLD`** *Єв* отримує статус exit/wait для всіх змінених/зомбі дочірніх процесів і викликає callback-функцію.

Правильно встановлювати дочірнього спостерігача після того, як [EvChild](class.evchild.html) завершився, але до початку наступної ітерації подієвого циклу. Наприклад, спочатку викликається `fork`, після чого новий дочірній процес може вийти, і тільки після цього в батьків встановлюється спостерігач [EvChild](class.evchild.html) для нового *PID*

Ви можете отримати доступ до статусів exit/tracing та `pid` використовуючи властивості об'єкта спостерігача rstatus та rpid.

Кількість *PID*спостерігачів для кожного *PID* НЕ обмежено. Усіх їх буде викликано.

Метод [EvChild::createStopped()](evchild.createstopped.html) не стартує(не активує) створеного спостерігача.

### Список параметрів

`pid`

Очікує зміни статусу процесу з ідентифікатором PID (або будь-якого процесу, якщо PID заданий як **`0`**

`trace`

Якщо **`false`**активація спостерігача відбувається тільки при завершенні процесу. Якщо **`true`**активація відбувається також при зупинці/відновленні процесу.

`callback`

Дивіться [Callback-функции наблюдателей](ev.watcher-callbacks.html)

`data`

Довільні дані, пов'язані зі спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Дивіться також

-   [EvLoop::child()](evloop.child.html) - Створює об'єкт EvChild, пов'язаний із поточним циклом подій