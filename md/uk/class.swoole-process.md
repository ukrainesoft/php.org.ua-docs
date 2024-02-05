---
navigation:
  - class.swoole-mysql-exception.md: « Swoole\\MySQL\\Exception
  - swoole-process.alarm.md: 'Swoole\\Process::alarm »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\Process
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\Process

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Process
     
     {

    /* Константы */
    
     const
     int
      IPC_NOWAIT = 256;


    /* Методы */
    
   public static alarm(int $interval_usec): void
public close(): void
public static daemon(bool $nochdir = ?, bool $noclose = ?): void
public __destruct(): void
public exec(string $exec_file, string $args): ReturnType
public exit(string $exit_code = ?): void
public freeQueue(): void
public static kill(int $pid, int $signal_no = ?): bool
public name(string $process_name): bool
public pop(int $maxsize = ?): mixed
public push(string $data): bool
public read(int $maxsize = ?): string
public static signal(string $signal_no, callable $callback): void
public start(): void
public statQueue(): array
public useQueue(int $key, int $mode = ?): bool
public static wait(bool $blocking = ?): array
public write(string $data): int

   }
```

## Обумовлені константи

**`Swoole\Process::IPC_NOWAIT`**

## Зміст

-   [Swoole\\Process::alarm](swoole-process.alarm.md)— Таймер високої точності, який запускає сигнал із фіксованим інтервалом
-   [Swoole\\Process::close](swoole-process.close.md)— Закриває канал для дочірнього процесу
-   [Swoole\\Process::\_\_construct](swoole-process.construct.md) \- Створює процес
-   [Swoole\\Process::daemon](swoole-process.daemon.md) \- Змінює процес на процес-демон
-   [Swoole\\Process::\_\_destruct](swoole-process.destruct.md) \- Знищує процес
-   [Swoole\\Process::exec](swoole-process.exec.md) \- Виконує системні команди
-   [Swoole\\Process::exit](swoole-process.exit.md) \- Зупиняє дочірні процеси
-   [Swoole\\Process::freeQueue](swoole-process.freequeue.md)— Знищує чергу повідомлень, створену swoole\_process::useQueue
-   [Swoole\\Process::kill](swoole-process.kill.md)— Надсилає сигнал дочірньому процесу
-   [Swoole\\Process::name](swoole-process.name.md) \- Встановлює назву процесу
-   [Swoole\\Process::pop](swoole-process.pop.md)— Читає та витягує дані з черги повідомлень
-   [Swoole\\Process::push](swoole-process.push.md)— Записує та поміщає дані в чергу повідомлень
-   [Swoole\\Process::read](swoole-process.read.md) \- Читає дані відправки в процес
-   [Swoole\\Process::signal](swoole-process.signal.md)— Надсилає сигнал дочірнім процесам
-   [Swoole\\Process::start](swoole-process.start.md) \- Запускає процес
-   [Swoole\\Process::statQueue](swoole-process.statqueue.md)— Отримує статистику черги повідомлень, яка використовується як метод зв'язку між процесами
-   [Swoole\\Process::useQueue](swoole-process.usequeue.md)— Створює чергу повідомлень як метод зв'язку між батьківським процесом та дочірніми процесами
-   [Swoole\\Process::wait](swoole-process.wait.md)— Чекає на події дочірніх процесів
-   [Swoole\\Process::write](swoole-process.write.md)— Записує дані до каналу та зв'язується з батьківським процесом або дочірніми процесами
