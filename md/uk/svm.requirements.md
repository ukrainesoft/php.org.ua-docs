---
navigation:
  - svm.setup.md: « Встановлення та налаштування
  - svm.installation.md: Установка »
  - index.md: PHP Manual
  - svm.setup.md: Встановлення та налаштування
title: Вимоги
---
## Вимоги

Потрібно, власне, сам Libsvm та його розробний пакет: для систем використовують RPM він називається libsvm-devel, а систем на базі Debian - libsvm-dev. Або ж можете завантажити безпосередньо з веб-сайту. Якщо встановлюєте з [» официального веб-сайта](http://www.csie.ntu.edu.tw/~cjlin/libsvm), треба буде зробити деякі дії, оскільки пакет самостійно не встановлюється. Наприклад, для встановлення останньої версії (3.1):

```
wget http://www.csie.ntu.edu.tw/~cjlin/cgi-bin/libsvm.cgi?+http://www.csie.ntu.edu.tw/~cjlin/libsvm+tar.gz
tar xvzf libsvm-3.1.tar.gz
cd libsvm-3.1
make lib
cp libsvm.so.1 /usr/lib
ln -s libsvm.so.1 libsvm.so
ldconfig
ldconfig --print | grep libsvm
```

На останньому кроці буде виведено розташування встановленого libsvm.
