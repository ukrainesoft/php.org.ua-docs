---
navigation:
  - install.windows.apache2.md: Apache 2.x в Microsoft Windows
  - install.cloud.md: Встановлення на платформах Cloud Computing »
  - index.md: PHP Manual
  - install.windows.md: Встановлення у системах Windows
title: Стандартні проблеми PHP під Windows
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Стандартні проблеми PHP під Windows

### Перевірка прав на тимчасову директорію

1.  У Провіднику натисніть правою кнопкою миші на тимчасовій директорії, виберіть пункт "Властивості" та перейдіть в закладку "Доступ".
    
2.  Для IIS, перевірте, що користувач IIS\_User має право на зміну для цієї директорії. Шлях тимчасової директорії можна переглянути у файлі php.ini.
