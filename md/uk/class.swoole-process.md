Клас SwooleProcess

-   [« SwooleMySQLException](class.swoole-mysql-exception.html)
    
-   [SwooleProcess::alarm »](swoole-process.alarm.html)
    
-   [PHP Manual](index.md)
    
-   [Swoole](book.swoole.md)
    
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

-   [SwooleProcess::alarm](swoole-process.alarm.html) — Таймер високої точності, який запускає сигнал із фіксованим інтервалом
-   [SwooleProcess::close](swoole-process.close.html) — Закриває канал для дочірнього процесу
-   [SwooleProcess::construct](swoole-process.construct.html) - Створює процес
-   [SwooleProcess::daemon](swoole-process.daemon.html) - Змінює процес на процес-демон
-   [SwooleProcess::destruct](swoole-process.destruct.html) - Знищує процес
-   [SwooleProcess::exec](swoole-process.exec.html) - Виконує системні команди
-   [SwooleProcess::exit](swoole-process.exit.html) - Зупиняє дочірні процеси
-   [SwooleProcess::freeQueue](swoole-process.freequeue.html) — Знищує чергу повідомлень, створену swooleprocess::useQueue
-   [SwooleProcess::kill](swoole-process.kill.html) — Надсилає сигнал дочірньому процесу
-   [SwooleProcess::name](swoole-process.name.html) — Встановлює назву процесу
-   [SwooleProcess::pop](swoole-process.pop.html) — Читає та витягує дані з черги повідомлень
-   [SwooleProcess::push](swoole-process.push.html) — Записує та поміщає дані в чергу повідомлень
-   [SwooleProcess::read](swoole-process.read.html) - Читає дані відправки в процес
-   [SwooleProcess::signal](swoole-process.signal.html) — Надсилає сигнал дочірнім процесам
-   [SwooleProcess::start](swoole-process.start.html) - Запускає процес
-   [SwooleProcess::statQueue](swoole-process.statqueue.html) — Отримує статистику черги повідомлень, яка використовується як метод зв'язку між процесами
-   [SwooleProcess::useQueue](swoole-process.usequeue.html) — Створює чергу повідомлень як метод зв'язку між батьківським процесом та дочірніми процесами
-   [SwooleProcess::wait](swoole-process.wait.html) — Чекає на події дочірніх процесів
-   [SwooleProcess::write](swoole-process.write.html) — Записує дані до каналу та зв'язується з батьківським процесом або дочірніми процесами