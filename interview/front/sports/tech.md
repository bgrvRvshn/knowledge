Почему этот код не работает:
```javascript
import {tooLongString} from 'sting'

function whatString(string) {
   if (tooLongString(string)) {
      string.slice(2)
   }
}
```
1. Строки неизменяемы
2. Нет ключевого слова `return`

Необходимо из двух массивов получить один массив `result`. В котором элементы 1-го массива `sites` буду включены в элементы 2-го массива `pages` по соответствующим `id`.
```javascript
// Первый массив
const sites = [
   { id: 2, name: 'site 2' },
   { id: 1, name: 'site 1' },
];
// Второй массив
const pages = [
   { id: 1121, title: 'page 1', site_id: 1 },
   { id: 2234, title: 'page 2', site_id: 2 },
   { id: 3321, title: 'page 3', site_id: 1 },
];

// Результат, который необходимо получить
const result = [
   { id: 1121, title: 'page 1', site: { id: 1, name: 'site 1' } },
   { id: 2234, title: 'page 2', site: { id: 2, name: 'site 2' } },
   { id: 3321, title: 'page 3', site: { id: 1, name: 'site 1' } },
];


function joinSitesToPages(sites, pages) {
    const result = []

    // 1 вариант решения, но не оптимальный,
    // т.к. find полностью должен будет пройти по массиву
    for (const page of pages) {
        result.push({
            id: page.id,
            title: page.title,
            site: sites.find(({id}) => id === page.site_id)
        })
    }
    
    // 2 вариант решения, сначало сформировать объект,
    // чтобы потом можно было обратиться к нужному элементу по ключу
    const sitesMap = {
        1: { id: 1, name: 'site 1' },
        ...
    }
    for (const page of pages) {
        result.push({
            id: page.id,
            title: page.title,
            site: sitesMap[pages.site_id]
        })
    }
    
    return result;
}
```
