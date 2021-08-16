# MODX SimpleSearch
Это Fork SimpleSearch by Sterc - https://github.com/Sterc/SimpleSearch
Добавлена возможность чтобы поиск мог отображать категории, в которых найдены ресурсы.

## Использование
Передаем параметр `ids` для сниппета `simplesearch` и на основе переданных id будут найдены категории с результатами. 
Параметр `ids` явно указывает в каких категориях искать

Указываем в массиве id категорий, результаты которых отображать. Чтобы не было расхождения результатов, эти id должны совпадать с  
параметром `ids` для сниппета simplesearch, который указывает где искать.

В чанке с результатами можно вывести категории таким образом:
```
    <ul class="search-categories">
      <li class="search-categories__item"><div>Все результаты</div><div>{$_pls['total']}</div></li>
      {foreach $_pls['categories'] as $category}
        <li class="search-categories__item"><div>{$category.pagetitle}</div><div>{$category.count}</div></li>
      {/foreach}
    </ul>
```