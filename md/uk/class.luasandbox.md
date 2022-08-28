Клас LuaSandbox

-   [« Базовое использование LuaSandbox](luasandbox.examples-basic.html)
    
-   [LuaSandbox::callFunction »](luasandbox.callfunction.html)
    
-   [PHP Manual](index.html)
    
-   [LuaSandbox](book.luasandbox.html)
    
-   Клас LuaSandbox
    

# Клас LuaSandbox

(PECL luasandbox >= 1.0.0)

## Вступ

Клас LuaSandbox створює середовище Lua та дозволяє виконувати код Lua.

## Огляд класів

```classsynopsis



    
     
      class LuaSandbox
     
     {

    /* Константы */
    
     const
     int
      SAMPLES = 0;

    const
     int
      SECONDS = 1;

    const
     int
      PERCENT = 2;


    /* Методы */
    
   public callFunction(string $name, mixed ...$args): array|bool
public disableProfiler(): void
public enableProfiler(float $period = 0.02): bool
public getCPUUsage(): float
public getMemoryUsage(): int
public getPeakMemoryUsage(): int
public getProfilerFunctionReport(int $units = LuaSandbox::SECONDS): array
public static getVersionInfo(): array
public loadBinary(string $code, string $chunkName = ''): LuaSandboxFunction
public loadString(string $code, string $chunkName = ''): LuaSandboxFunction
public pauseUsageTimer(): bool
public registerLibrary(string $libname, array $functions): void
public setCPULimit(float|bool $limit): void
public setMemoryLimit(int $limit): void
public unpauseUsageTimer(): void
public wrapPhpFunction(callable $function): LuaSandboxFunction

   }
```

## Обумовлені константи

**`LuaSandbox::SAMPLES`**

Використовується з [LuaSandbox::getProfilerFunctionReport()](luasandbox.getprofilerfunctionreport.html) для повернення часу у зразках.

**`LuaSandbox::SECONDS`**

Використовується з [LuaSandbox::getProfilerFunctionReport()](luasandbox.getprofilerfunctionreport.html) для часу в секундах.

**`LuaSandbox::PERCENT`**

Використовується з [LuaSandbox::getProfilerFunctionReport()](luasandbox.getprofilerfunctionreport.html) повернення часу у відсотках від загального значення.

## Зміст

-   [LuaSandbox::callFunction](luasandbox.callfunction.html) — Викликає функцію у глобальній змінній Lua
-   [LuaSandbox::disableProfiler](luasandbox.disableprofiler.html) - Відключає профільник
-   [LuaSandbox::enableProfiler](luasandbox.enableprofiler.html) - Включає профільник
-   [LuaSandbox::getCPUUsage](luasandbox.getcpuusage.html) — Повертає поточний час використання процесора у середовищі Lua
-   [LuaSandbox::getMemoryUsage](luasandbox.getmemoryusage.html) — Повертає поточне використання пам'яті у середовищі Lua
-   [LuaSandbox::getPeakMemoryUsage](luasandbox.getpeakmemoryusage.html) — Повертає пікове використання пам'яті у середовищі Lua
-   [LuaSandbox::getProfilerFunctionReport](luasandbox.getprofilerfunctionreport.html) — Отримує дані профілювача
-   [LuaSandbox::getVersionInfo](luasandbox.getversioninfo.html) — Повертає версії LuaSandbox та Lua
-   [LuaSandbox::loadBinary](luasandbox.loadbinary.html) — Завантажує попередньо скомпільований двійковий фрагмент у середу Lua
-   [LuaSandbox::loadString](luasandbox.loadstring.html) — Завантажує код Lua у середу Lua
-   [LuaSandbox::pauseUsageTimer](luasandbox.pauseusagetimer.html) — Припиняє таймер використання процесора
-   [LuaSandbox::registerLibrary](luasandbox.registerlibrary.html) — Реєструє набір PHP-функцій як бібліотеку Lua
-   [LuaSandbox::setCPULimit](luasandbox.setcpulimit.html) — Встановлює обмеження часу процесора для середовища Lua
-   [LuaSandbox::setMemoryLimit](luasandbox.setmemorylimit.html) — Встановлює межу пам'яті для середовища Lua
-   [LuaSandbox::unpauseUsageTimer](luasandbox.unpauseusagetimer.html) — Відновлює таймер, зупинений LuaSandbox::pauseUsageTimer
-   [LuaSandbox::wrapPhpFunction](luasandbox.wrapphpfunction.html) — Обертає викликаний PHP-об'єкт у LuaSandboxFunction