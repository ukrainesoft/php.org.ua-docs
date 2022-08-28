Створює об'єкт спостерігач EvIo

-   [« EvIo](class.evio.html)
    
-   [EvIo::createStopped »](evio.createstopped.html)
    
-   [PHP Manual](index.html)
    
-   [EvIo](class.evio.html)
    
-   Створює об'єкт спостерігач EvIo
    

# EvIo::construct

(PECL ev >= 0.2.0)

EvIo::construct — Створює спостерігач об'єкт EvIo

### Опис

public **EvIo::construct**  
[mixed](language.types.declarations.html#language.types.declarations.mixed) `$fd`  
int `$events`  
[callable](language.types.callable.html) `$callback`  
[mixed](language.types.declarations.html#language.types.declarations.mixed) `$data`  
int `$priority`  

Створює та автоматично стартує об'єкт спостерігач EvIo.

### Список параметрів

`fd`

Може бути потоком, відкритим за допомогою функції [fopen()](function.fopen.html) чи аналогічною, числовим дескриптором файлу чи сокетом.

`events`

**`Ev::READ`** та/або **`Ev::WRITE`**. Дивіться [битовые маски](class.ev.html#ev.constants.watcher-revents)

`callback`

Дивіться [Callback-функции наблюдателей](ev.watcher-callbacks.html)

`data`

Довільні дані, пов'язані зі спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Дивіться також

-   [EvIo::createStopped()](evio.createstopped.html) - Створює зупинений об'єкт спостерігача EvIo
-   [EvLoop::io()](evloop.io.html) - Створює об'єкт спостерігача EvIo, пов'язаний із поточним екземпляром циклу подій