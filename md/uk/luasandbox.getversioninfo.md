---
navigation:
  - luasandbox.getprofilerfunctionreport.md: '« LuaSandbox::getProfilerFunctionReport'
  - luasandbox.loadbinary.md: 'LuaSandbox::loadBinary »'
  - index.md: PHP Manual
  - class.luasandbox.md: LuaSandbox
title: 'LuaSandbox::getVersionInfo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# LuaSandbox::getVersionInfo

(PECL luasandbox >= 1.6.0)

LuaSandbox::getVersionInfo — Повертає версії LuaSandbox та Lua

### Опис

```methodsynopsis
public static LuaSandbox::getVersionInfo(): array
```

Повертає версії LuaSandbox та Lua.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив із двома ключами:

| element | type | description |
| --- | --- | --- |
| LuaSandbox | string | Версія модуля LuaSandbox. |
| Lua | string | Ім'я та версія бібліотеки, визначені макросом LUA\_RELEASE, наприклад, "Lua 5.1.5". |
