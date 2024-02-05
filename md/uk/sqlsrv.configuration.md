---
navigation:
  - sqlsrv.installation.md: « Встановлення
  - sqlsrv.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - sqlsrv.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

Наступна таблиця показує список параметрів, доступних у модулі SQLSRV. Для отримання додаткової інформації про налаштування, зверніться до відповідного розділу документації - [» обробка помилок та попереджень у SQLSRV](http://msdn.microsoft.com/en-us/library/cc626302.aspx)

**SQLSRV Опції налаштування**

| Имя | По умолчанию | Место изменения | Изменения |
| --- | --- | --- | --- |
| sqlsrv.WarningsReturnAsErrors | 1 (**`true`**) . | **`INI_ALL`** | Доступно з версії SQLSRV 1.0 |
| sqlsrv.LogSubsystems |  | **`INI_ALL`** | Доступно з версії SQLSRV 1.0 |
| sqlsrv.LogSeverity |  | **`INI_ALL`** | Доступно з версії SQLSRV 1.0 |
