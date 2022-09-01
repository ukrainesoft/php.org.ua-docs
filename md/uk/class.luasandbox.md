---
navigation:
  - luasandbox.examples-basic.html: « Базовое использование LuaSandbox
  - luasandbox.callfunction.md: 'LuaSandbox::callFunction »'
  - index.md: PHP Manual
  - book.luasandbox.md: LuaSandbox
title: Клас LuaSandbox
---
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

Використовується з [LuaSandbox::getProfilerFunctionReport()](luasandbox.getprofilerfunctionreport.md) для повернення часу у зразках.

**`LuaSandbox::SECONDS`**

Використовується з [LuaSandbox::getProfilerFunctionReport()](luasandbox.getprofilerfunctionreport.md) для часу в секундах.

**`LuaSandbox::PERCENT`**

Використовується з [LuaSandbox::getProfilerFunctionReport()](luasandbox.getprofilerfunctionreport.md) повернення часу у відсотках від загального значення.

## Зміст

-   [LuaSandbox::callFunction](luasandbox.callfunction.md) — Викликає функцію у глобальній змінній Lua
-   [LuaSandbox::disableProfiler](luasandbox.disableprofiler.md) - Відключає профільник
-   [LuaSandbox::enableProfiler](luasandbox.enableprofiler.md) - Включає профільник
-   [LuaSandbox::getCPUUsage](luasandbox.getcpuusage.md) — Повертає поточний час використання процесора у середовищі Lua
-   [LuaSandbox::getMemoryUsage](luasandbox.getmemoryusage.md) — Повертає поточне використання пам'яті у середовищі Lua
-   [LuaSandbox::getPeakMemoryUsage](luasandbox.getpeakmemoryusage.md) — Повертає пікове використання пам'яті у середовищі Lua
-   [LuaSandbox::getProfilerFunctionReport](luasandbox.getprofilerfunctionreport.md) — Отримує дані профілювача
-   [LuaSandbox::getVersionInfo](luasandbox.getversioninfo.md) — Повертає версії LuaSandbox та Lua
-   [LuaSandbox::loadBinary](luasandbox.loadbinary.md) — Завантажує попередньо скомпільований двійковий фрагмент у середу Lua
-   [LuaSandbox::loadString](luasandbox.loadstring.md) — Завантажує код Lua у середу Lua
-   [LuaSandbox::pauseUsageTimer](luasandbox.pauseusagetimer.md) — Припиняє таймер використання процесора
-   [LuaSandbox::registerLibrary](luasandbox.registerlibrary.md) — Реєструє набір PHP-функцій як бібліотеку Lua
-   [LuaSandbox::setCPULimit](luasandbox.setcpulimit.md) — Встановлює обмеження часу процесора для середовища Lua
-   [LuaSandbox::setMemoryLimit](luasandbox.setmemorylimit.md) — Встановлює межу пам'яті для середовища Lua
-   [LuaSandbox::unpauseUsageTimer](luasandbox.unpauseusagetimer.md) — Відновлює таймер, зупинений LuaSandbox::pauseUsageTimer
-   [LuaSandbox::wrapPhpFunction](luasandbox.wrapphpfunction.md) — Обертає викликаний PHP-об'єкт у LuaSandboxFunction
