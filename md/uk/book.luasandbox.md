LuaSandbox

-   [« LuaClosure::invoke](luaclosure.invoke.html)
    
-   [Введение »](intro.luasandbox.html)
    
-   [PHP Manual](index.html)
    
-   [Інші базові модулі](refs.basic.other.html)
    
-   LuaSandbox
    

# LuaSandbox

-   [Введение](intro.luasandbox.html)
-   [Установка и настройка](luasandbox.setup.html)
    -   [Требования](luasandbox.requirements.html)
    -   [Установка](luasandbox.installation.html)
    -   [Настройка во время выполнения](luasandbox.configuration.html)
    -   [Типы ресурсов](luasandbox.resources.html)
-   [Отличия от стандартного Lua](reference.luasandbox.differences.html)
-   [Примеры](luasandbox.examples.html)
    -   [Базовое использование LuaSandbox](luasandbox.examples-basic.html)
-   [LuaSandbox](class.luasandbox.html) - Клас LuaSandbox
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
    -   [LuaSandbox::wrapPhpFunction](luasandbox.wrapphpfunction.html) — Обертає PHP-об'єкт, що викликається в LuaSandboxFunction
-   [LuaSandboxFunction](class.luasandboxfunction.html) - Клас LuaSandboxFunction
    -   [LuaSandboxFunction::call](luasandboxfunction.call.html) - Викликає Lua-функцію
    -   [LuaSandboxFunction::construct](luasandboxfunction.construct.html) - Не використовується
    -   [LuaSandboxFunction::dump](luasandboxfunction.dump.html) — Вивантажує функцію у вигляді BLOB
-   [LuaSandboxError](class.luasandboxerror.html) - Клас LuaSandboxError
-   [LuaSandboxErrorError](class.luasandboxerrorerror.html) - Клас LuaSandboxErrorError
-   [LuaSandboxFatalError](class.luasandboxfatalerror.html) - Клас LuaSandboxFatalError
-   [LuaSandboxMemoryError](class.luasandboxmemoryerror.html) - Клас LuaSandboxMemoryError
-   [LuaSandboxRuntimeError](class.luasandboxruntimeerror.html) - Клас LuaSandboxRuntimeError
-   [LuaSandboxSyntaxError](class.luasandboxsyntaxerror.html) - Клас LuaSandboxSyntaxError
-   [LuaSandboxTimeoutError](class.luasandboxtimeouterror.html) - Клас LuaSandboxTimeoutError