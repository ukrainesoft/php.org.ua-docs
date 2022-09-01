---
navigation:
  - enchant.constants.md: « Обумовлені константи
  - ref.enchant.md: Функции Enchant »
  - index.md: PHP Manual
  - book.enchant.md: Enchant
title: Приклади
---
# Приклади

**Приклад #1 Приклад використання Enchant**

```php
<?php
$tag = 'en_US';
$r = enchant_broker_init();
$bprovides = enchant_broker_describe($r);
echo "Доступны следующие бэкенды:\n";
print_r($bprovides);

$dicts = enchant_broker_list_dicts($r);
print_r($dicts);
if (enchant_broker_dict_exists($r,$tag)) {
    $d = enchant_broker_request_dict($r, $tag);
    $dprovides = enchant_dict_describe($d);
    echo "словарь $tag:\n";
    $wordcorrect = enchant_dict_check($d, "soong");
    print_r($dprovides);
    if (!$wordcorrect) {
        $suggs = enchant_dict_suggest($d, "soong");
        echo "Предложения для 'soong':";
        print_r($suggs);
    }
    enchant_broker_free_dict($d);
} else {
}
enchant_broker_free($r);
?>
```
