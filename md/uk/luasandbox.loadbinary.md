Завантажує попередньо скомпільований двійковий фрагмент у середу Lua

-   [« LuaSandbox::getVersionInfo](luasandbox.getversioninfo.html)
    
-   [LuaSandbox::loadString »](luasandbox.loadstring.html)
    
-   [PHP Manual](index.html)
    
-   [LuaSandbox](class.luasandbox.html)
    
-   Завантажує попередньо скомпільований двійковий фрагмент у середу Lua
    

# LuaSandbox::loadBinary

(PECL luasandbox >= 1.0.0)

LuaSandbox::loadBinary — Завантажує попередньо скомпільований двійковий фрагмент у середу Lua

### Опис

```methodsynopsis
public LuaSandbox::loadBinary(string $code, string $chunkName = ''): LuaSandboxFunction
```

Завантажує дані, створені [LuaSandboxFunction::dump()](luasandboxfunction.dump.html)

### Список параметрів

`code`

Дані з [LuaSandboxFunction::dump()](luasandboxfunction.dump.html)

`chunkName`

Ім'я завантаженої функції.

### Значення, що повертаються

Повертає [LuaSandboxFunction](class.luasandboxfunction.html)

### Дивіться також

-   [LuaSandbox::loadString()](luasandbox.loadstring.html) - Завантажує код Lua у середу Lua