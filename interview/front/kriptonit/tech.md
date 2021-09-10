```javascript
// Что выведет консоль?
console.log('10' + 2) // '102'
console.log('10' * 2) // 20
console.log('abc' * 2) // NaN
console.log(!!'false') // true

console.log(typeof NaN) // 'number'

// Как отличить число от NaN, если у обоих тип 'number'?
isNaN()

// Что выведет консоль?
const obj = {};
const arr = [];

console.log(typeof arr === typeof obj) // true

// Как убедиться что значение именно массив?
Array.isArray(arr)
arr instanceof Array

// Удалить из массива дубликаты
const numbers = [1, 0, 5, 5, 1, 1, 3, 5, 1, 1, 1, 4, 5, 1, 1, 4];

// Способ 1 - но данный способ сортирует массив
const deleteDuplicates = (numbers) => {
    const duplicatesNumbers = {}

    numbers.forEach((num) => duplicatesNumbers[num] = true)
    
    return Object.keys(duplicatesNumbers)
}

deleteDuplicates(numbers) // ['0', '1', '3', '4', '5']

// Способ 2
const deleteDuplicates = (numbers) => numbers.filter((num, index) => index === numbers.indexOf(num))

deleteDuplicates(numbers) // [1, 0, 5, 3, 4]

// Способ 3
// Объект Set сохраняет только уникальные значения
// Использование [] приводит к **обычному** массиву
const deleteDuplicates = (numbers) => [ ...Set(numbers) ]

deleteDuplicates(numbers); // [1, 0, 5, 3, 4]
```
