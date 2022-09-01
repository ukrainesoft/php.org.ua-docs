---
navigation:
  - class.compersisthelper.html: « COMPersistHelper
  - compersisthelper.getcurfilename.html: 'COMPersistHelper::GetCurFileName »'
  - index.html: PHP Manual
  - class.compersisthelper.html: COMPersistHelper
title: 'COMPersistHelper::construct'
---
# COMPersistHelper::construct

(PHP 5, PHP 7, PHP 8)

COMPersistHelper::construct — Конструктор класу COMPersistHelper

### Опис

public **COMPersistHelper::construct**[variant](class.variant.html) `$variant` **`null`**

Створює об'єкт класу COMPersistHelper, зазвичай пов'язаний з `variant`

### Список параметрів

`variant`

Об'єкт COM, що реалізує інтерфейс **IDispatch**. Для успішного виклику методів [COMPersistHelper](class.compersisthelper.html), об'єкт повинен реалізовувати інтерфейси **IPersistFile** **IPersistStream** та/або **IPersistStreamInit**. Передача **`null`** в якості `variant` виправдана лише в тому випадку, якщо об'єкт буде завантажений із потоку за допомогою [COMPersistHelper::LoadFromStream()](compersisthelper.loadfromstream.html)
