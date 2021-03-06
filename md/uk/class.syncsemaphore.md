- [«SyncMutex::unlock](syncmutex.unlock.md)
- [SyncSemaphore::\_\_construct »](syncsemaphore.construct.md)

- [PHP Manual](index.md)
- [Sync](book.sync.md)
- Клас SyncSemaphore

# Клас SyncSemaphore

(PECL sync \>= 1.0.0)

## Вступ

Кросплатформова, нативна реалізація іменованих та безіменних
об'єктів семафорів

Семафор обмежує доступ до обмеженого ресурсу обмеженим числом
екземплярів. Семафори відрізняються від м'ютексів тим, що вони можуть
дозволити доступ до ресурсу більш ніж одному екземпляру одночасно, в
той час, як м'ютекс допускає лише один екземпляр за раз.

## Огляд класів

class **SyncSemaphore** {

/\* Методи \*/

public [\_\_construct](syncsemaphore.construct.md)(string `$name` = ?,
int `$initialval` = 1, bool `$autounlock` = **`true`**)

public [lock](syncsemaphore.lock.md)(int `$wait` = -1): bool

public [unlock](syncsemaphore.unlock.md)(int `&$prevcount` = ?): bool

}

## Зміст

- [SyncSemaphore::\_\_construct](syncsemaphore.construct.md) -
Створює новий об'єкт SyncSemaphore
- [SyncSemaphore::lock](syncsemaphore.lock.md) — Зменшує рахунок
семафора чи чекає
- [SyncSemaphore::unlock](syncsemaphore.unlock.md) — Збільшує
рахунок семафору
