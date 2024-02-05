---
navigation:
  - class.compersisthelper.md: « COMPersistHelper
  - compersisthelper.getcurfilename.md: 'COMPersistHelper::GetCurFileName »'
  - index.md: PHP Manual
  - class.compersisthelper.md: COMPersistHelper
title: 'COMPersistHelper::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# COMPersistHelper::\_\_construct

(PHP 5, PHP 7, PHP 8)

COMPersistHelper::\_\_construct — Конструктор класу COMPersistHelper

### Опис

public**COMPersistHelper::\_\_construct**(?[variant](class.variant.md) `$variant` **`null`**) .

Створює об'єкт класу COMPersistHelper, зазвичай пов'язаний з `variant`

### Список параметрів

`variant`

Об'єкт COM, що реалізує інтерфейс **IDispatch**. Для успішного виклику методів [COMPersistHelper](class.compersisthelper.md), об'єкт повинен реалізовувати інтерфейси **IPersistFile** **IPersistStream**и/или**IPersistStreamInit**Передача\*\*`null`\*\* в якості `variant` виправдана тільки в тому випадку, якщо об'єкт буде завантажений із потоку за допомогою [COMPersistHelper::LoadFromStream()](compersisthelper.loadfromstream.md)
