Повертає точну копію тренувальних даних

-   [« fann\_destroy](function.fann-destroy.html)
    
-   [fann\_get\_activation\_function »](function.fann-get-activation-function.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає точну копію тренувальних даних
    

# fannduplicatetraindata

(PECL fann> = 1.0.0)

fannduplicatetraindata — Повертає точну копію тренувальних даних

### Опис

```methodsynopsis
fann_duplicate_train_data(resource $data): resource
```

Повертає ресурс (resource) з точною копією тренувальних даних

### Список параметрів

`data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Повертає ресурс (resource) навчальних даних, або **`false`** у разі виникнення помилки.