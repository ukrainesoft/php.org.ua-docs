---
navigation:
  - phar.fileformat.md: Чим відрізняється phar від tar-або zip-архіву?
  - phar.fileformat.stub.md: Заглушка Phar-файлу »
  - index.md: PHP Manual
  - phar.fileformat.md: Чим відрізняється phar від tar-або zip-архіву?
title: Складові всіх Phar-архівів незалежно від формату файлу
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Складові всіх Phar-архівів незалежно від формату файлу

Усі Phar-архіви містять від трьох до чотирьох секцій:

1.  заглушка
    
2.  маніфест, що описує вміст
    
3.  вміст файлу
    
4.  \[не обов'язково\]підпис для перевірки цілісності Phar (тільки для формату файлу phar)
