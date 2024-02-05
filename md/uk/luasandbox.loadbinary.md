---
navigation:
  - luasandbox.getversioninfo.md: '« LuaSandbox::getVersionInfo'
  - luasandbox.loadstring.md: 'LuaSandbox::loadString »'
  - index.md: PHP Manual
  - class.luasandbox.md: LuaSandbox
title: 'LuaSandbox::loadBinary'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# LuaSandbox::loadBinary

(PECL luasandbox >= 1.0.0)

LuaSandbox::loadBinary — Завантажує попередньо скомпільований двійковий фрагмент у середу Lua

### Опис

```methodsynopsis
public LuaSandbox::loadBinary(string $code, string $chunkName = ''): LuaSandboxFunction
```

Завантажує дані, створені [LuaSandboxFunction::dump()](luasandboxfunction.dump.md)

### Список параметрів

`code`

Дані з [LuaSandboxFunction::dump()](luasandboxfunction.dump.md)

`chunkName`

Ім'я завантаженої функції.

### Значення, що повертаються

Повертає [LuaSandboxFunction](class.luasandboxfunction.md)

### Дивіться також

-   [LuaSandbox::loadString()](luasandbox.loadstring.md) \- Завантажує код Lua у середу Lua
