# js-exercises

## Exercises for lecture #2 - DOM

1. створіть піддирексторію exercis-2. В середині exercis-2 створіть файли index.html та js/main.js. 


## файл index.html:

```html
<!DOCTYPE html>
<html lang="en" >

<head>
  
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>lecture 2</title>
  
</head>

<body>
  <h1>Hello, javascript!</h1>
  
  <script type="module" src="js/main.js"></script>
</body>

</html>

```

## файл js/main.js:

```js
'use strict';


```
1. Напишіть функцію checkAge(age), що приймає параметр age та повертає true, якщо параметр age перевищує 18, в іншому випадку запитує підтвердження 'Did parents allow you?' та повертає результат. Реалізуйте функцію checkAge(age) двома способами - використовуючи оператор if () { } else { } та - використовуючи тернарний оператор ?.
    

2. Напишіть функцію min(a,b), яка повертає найменше з двох чисел a і b. У випадку рівності a == b немає значення, що повертати. Наприклад:
```js
min(2, 5) == 2
min(3, -1) == -1
min(1, 1) == 1
```

  - реалізуйте функцію min, використовуючи оператор if else
  - реалізуйте функцію min, використовуючи тернарний оператор

3. Напишіть функцію pow(x,n), яка повертає x у ступені n. Або, іншими словами, множить x на себе n разів і повертає результат. У цьому завданні функція повинна підтримувати лише натуральні значення n: цілі числа від 1.

```js
pow(3, 2) = 3 * 3 = 9
pow(3, 3) = 3 * 3 * 3 = 27
pow(1, 100) = 1 * 1 * ...* 1 = 1
```
Створіть сценарій, де спочатку користувачу пропонують ввести x і n, а потім показують результат pow(x,n), або повідомлення про неправильне значення параметра n.

4. Переписати функцію ask, використовуючи функцію стрілок:

```js
function ask(question, yes, no) {
  if (confirm(question)) yes();
  else no();
}

```
5. Переписати функцію ask, використовуючи функціональний вираз

6. Маємо 3 функції.
```js
function A() { console.log('A was called'); return undefined;}
function B() { console.log('B was called'); return false;}
function C() { console.log('C was called'); return "foo";}
```
  - Яким чином виконати виклик функцій A() і C(), щоб на консолі отримати такий результат
'''  
  A was called
  C was called
  foo 
'''
  - Яким чином виконати виклик функцій B() і C(), щоб на консолі отримати такий результат
'''  
  B was called
  C was called
  foo
'''

7. Створити об'єкт person, що має властивості name з типом рядка та age з типом цілого числа. Надати значення цим властивостям. Вивести значення властивостей об'єкту на консоль. Змінити тип властивості name з рядка на об'єкт, з ключами  firstName та lastName. Надати значення цим властивостям. Вивести значення властивостей об'єкту на консоль.

8. Маємо масив fruits:
```js
const fruits = ['apple', 'banana', 'cantaloupe', 'blueberries', 'grapefruit'];

```
  - Використовуючи цикл for вивести на консоль список елементів з масиву fruits.  
  - Використовуючи цикл while вивести на консоль список елементів з масиву fruits.  
  - Використовуючи цикл do...while вивести на консоль список елементів з масиву fruits.  

9. Маємо масив Numbs. 

```js
const Numbs = [1,2,3,4,5,6,7,8,9,10];

```
  - Використовуючи цикл for вивести на консоль парні елементи з масиву Numbs.  


10. Маємо масив names:

```js
const names = ['Batman'];
```
  - Додати 'Joker' в кінець масиву names:
  - Додати 'Bane' на початок масиву names
  - Перевірити чи існує рядок 'Alfred' у масиві names, і якщо не існує, додати його до кінця масиву. 
  - Перевірити чи існує рядок 'Batman' у масиві names, і якщо існує, видалити його з масиву. 



## файл index.html:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>lecture №2 - об'єктна модель документа</title>
   <link rel="shortcut icon" href="/favicon.ico" type="image/x-icon">
   <link rel="stylesheet" href="css/main.css">
</head>
<body>

    <div class="container">
        <header>
            <h1 class='title' id='first-title'>First Title</h1>
        </header>
        
        <p id="p1">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Labore accusantium distinctio explicabo iure possimus natus obcaecati fugiat voluptas id, eveniet ab, voluptate repellat? Inventore voluptate perferendis sequi distinctio qui consectetur.
          <button>It's First Button</button>
        </p>
    </div>
    
    <div class="container">
        <header>
            <h1 class='title' id='second-title'>Second Title</h1>
        </header>
        
        <p id="p2">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Labore accusantium distinctio explicabo iure possimus natus obcaecati fugiat voluptas id, eveniet ab, voluptate repellat? Inventore voluptate perferendis sequi distinctio qui consectetur.
          <button>It's Second Button</button>
        </p>
    </div>
    
    <div class="container">
        <header>
            <h1 class='title' id='third-title'>Third Title</h1>
        </header>
        
        <p id="p3">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Labore accusantium distinctio explicabo iure possimus natus obcaecati fugiat voluptas id, eveniet ab, voluptate repellat? Inventore voluptate perferendis sequi distinctio qui consectetur.
        <button>It's Third Button</button>
      </p>
    </div>
    
    <div class="container">
        <header>
            <h1 class='title' id='fourth-title'>Fourth Title</h1>
        </header>
    
        <p id="p4">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Labore accusantium distinctio explicabo iure possimus natus obcaecati fugiat voluptas id, eveniet ab, voluptate repellat? Inventore voluptate perferendis sequi distinctio qui consectetur.
          <button>It's Fourth Button</button>
        </p>
    </div>

      <script type="module" src="js/main.js"></script>
</body>
</html>



```
## Вміст app.css:
```css
.first {
    color: red;
}
.second {
    color: blue;
}
.third {
    color: green;
    background-color: yellow;
}

.fourth {
    color: gray;
    
}
.border {
    border: solid red 1px;
}

.title {
    padding: 1rem 2rem;
    border: double 2px violet;
}
```

## файл js/main.js:

```js
'use strict';

const classes = ['first', 'second', 'third', 'fourth'];
```
11. Отримати перший абзац за допомогою **_document.querySelector('#id')_** за його ідентифікатором p1. Встановити для нього стиль background-color = "gold"
    

12. Отримати другий абзац за допомогою **_document.querySelector('#id')_** за його ідентифікатором p2. Встановити для нього стилі background-color:gold; color: blue; font-size: 2rem;

13. Отримати третій абзац за допомогою **_document.querySelector('#id')_** за його ідентифікатором p3. Призначити для нього клас third 

14. Отримати четвертий абзац за допомогою **_document.querySelector('#id')_** за його ідентифікатором p4. Призначити для нього класи fourth та border

15. Отримати першу кнопку за допомогою **_document.querySelector()_**. Призначити для неї стилі background-color:gold; color: blue;

16. Отримати другу кнопку за допомогою **_document.querySelector()_**. Виконати обробку події натискання на цю кнопку, що призводить до приховування параграфа p1.

17. Отримати третю кнопку за допомогою **_document.querySelector()_**. Виконати обробку події натискання на цю кнопку, що відображає прихований параграф p1.

18. Отримати четверту кнопку за допомогою **_document.querySelector()_**. Виконати обробку події натискання на цю кнопку, що переключає тему документа з світлої на темну і навпаки.