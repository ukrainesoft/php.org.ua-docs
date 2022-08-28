Клас SwooleProcess

-   [« Swoole\\MySQL\\Exception](class.swoole-mysql-exception.html)
    
-   [Swoole\\Process::alarm »](swoole-process.alarm.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole](book.swoole.html)
    
-   Клас SwooleProcess
    

# Клас SwooleProcess

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

-   [Swoole\\Process::alarm](swoole-process.alarm.html) — Таймер високої точності, який запускає сигнал із фіксованим інтервалом
-   [Swoole\\Process::close](swoole-process.close.html) — Закриває канал для дочірнього процесу
-   [Swoole\\Process::\_\_construct](swoole-process.construct.html) - Створює процес
-   [Swoole\\Process::daemon](swoole-process.daemon.html) - Змінює процес на процес-демон
-   [Swoole\\Process::\_\_destruct](swoole-process.destruct.html) - Знищує процес
-   [Swoole\\Process::exec](swoole-process.exec.html) - Виконує системні команди
-   [Swoole\\Process::exit](swoole-process.exit.html) - Зупиняє дочірні процеси
-   [Swoole\\Process::freeQueue](swoole-process.freequeue.html) — Знищує чергу повідомлень, створену swooleprocess::useQueue
-   [Swoole\\Process::kill](swoole-process.kill.html) — Надсилає сигнал дочірньому процесу
-   [Swoole\\Process::name](swoole-process.name.html) — Встановлює назву процесу
-   [Swoole\\Process::pop](swoole-process.pop.html) — Читає та витягує дані з черги повідомлень
-   [Swoole\\Process::push](swoole-process.push.html) — Записує та поміщає дані в чергу повідомлень
-   [Swoole\\Process::read](swoole-process.read.html) - Читає дані відправки в процес
-   [Swoole\\Process::signal](swoole-process.signal.html) — Надсилає сигнал дочірнім процесам
-   [Swoole\\Process::start](swoole-process.start.html) - Запускає процес
-   [Swoole\\Process::statQueue](swoole-process.statqueue.html) — Отримує статистику черги повідомлень, яка використовується як метод зв'язку між процесами
-   [Swoole\\Process::useQueue](swoole-process.usequeue.html) — Створює чергу повідомлень як метод зв'язку між батьківським процесом та дочірніми процесами
-   [Swoole\\Process::wait](swoole-process.wait.html) — Чекає на події дочірніх процесів
-   [Swoole\\Process::write](swoole-process.write.html) — Записує дані до каналу та зв'язується з батьківським процесом або дочірніми процесами