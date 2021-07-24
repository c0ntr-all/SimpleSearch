# MODX SimpleSearch
Это Fork SimpleSearch by Sterc - https://github.com/Sterc/SimpleSearch
Добавлена возможность чтобы поиск мог отображать категории, в которых найдены ресурсы.

## Использование
*Пока можно только указать категории, в которых искать. Сниппет simplesearch 72 строка, переменная `$categoriesForSearch`.

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