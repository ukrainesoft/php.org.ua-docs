Передаємо подію сигналу в Ev

-   [« Ev::embeddableBackends](ev.embeddablebackends.md)
    
-   [Ev::feedSignalEvent »](ev.feedsignalevent.md)
    
-   [PHP Manual](index.md)
    
-   [Єв](class.ev.md)
    
-   Передаємо подію сигналу в Ev
    

# Ev::feedSignal

(PECL ev >= 0.2.0)

Ev::feedSignal — Передаємо подію сигналу в Ev

### Опис

```methodsynopsis
final
   public
   static
   Ev::feedSignal(
    int
     $signum
   ): void
```

Симуляція прийому сигналу. Цю функцію можна безпечно викликати будь-коли, з будь-якого контексту, включаючи обробники сигналів або випадкові потоки виконання. Основне призначення – налаштування обробки сигналів під час виконання.

На відміну від [Ev::feedSignalEvent()](ev.feedsignalevent.md)Цей метод працює незалежно від того, який цикл зареєстрував сигнал.

### Список параметрів

`signum`

Номер сигналу. Дивіться сторінку man `signal(7)`. Ви можете використовувати константи, експортовані з модуля `pcntl`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [Ev::feedSignalEvent()](ev.feedsignalevent.md) - Надіслати подію сигналу в цикл за замовчуванням