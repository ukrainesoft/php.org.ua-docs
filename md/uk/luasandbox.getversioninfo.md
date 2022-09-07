---
navigation:
  - luasandbox.getprofilerfunctionreport.md: '« LuaSandbox::getProfilerFunctionReport'
  - luasandbox.loadbinary.md: 'LuaSandbox::loadBinary »'
  - index.md: PHP Manual
  - class.luasandbox.md: LuaSandbox
title: 'LuaSandbox::getVersionInfo'
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
| Lua | string | Ім'я та версія бібліотеки, визначені макросом LUARELEASE, наприклад, "Lua 5.1.5". |
