# js-dev-exercises

## Exercises for lecture #5 - Create Element

1. В середині exercises створіть піддирексторію lecture-5. В середині lecture-5 створіть файли index.html, css/main.css та js/main.js. 

## файл index.html:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="shortcut icon" href="/favicon.ico" type="image/x-icon">
    <title>Table Style</title>
    
    <link rel="stylesheet" href="css/main.css">
</head>
<body>

    <div class="table-title">
      <h3>Data Table</h3>
    </div>

    


    <script type="module" src="js/main.js"></script>
</body>
</html>


```
## Вміст css/main.css:
```css

@import url(https://fonts.googleapis.com/css?family=Roboto:400,500,700,300,100);

body {
  background-color: #3e94ec;
  font-family: "Roboto", helvetica, arial, sans-serif;
  font-size: 16px;
  font-weight: 400;
  text-rendering: optimizeLegibility;
}

div.table-title {
   display: block;
  margin: auto;
  max-width: 600px;
  padding:5px;
  width: 100%;
}

.table-title h3 {
   color: #fafafa;
   font-size: 30px;
   font-weight: 400;
   font-style:normal;
   font-family: "Roboto", helvetica, arial, sans-serif;
   text-shadow: -1px -1px 1px rgba(0, 0, 0, 0.1);
   text-transform:uppercase;
}


.table-fill {
  background: white;
  border-radius:3px;
  border-collapse: collapse;
  height: 320px;
  margin: auto;
  max-width: 600px;
  padding:5px;
  width: 100%;
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
  animation: float 5s infinite;
}
 
th {
  color:#D5DDE5;;
  background:#1b1e24;
  border-bottom:4px solid #9ea7af;
  border-right: 1px solid #343a45;
  font-size:23px;
  font-weight: 100;
  padding:24px;
  text-align:left;
  text-shadow: 0 1px 1px rgba(0, 0, 0, 0.1);
  vertical-align:middle;
}

th:first-child {
  border-top-left-radius:3px;
}
 
th:last-child {
  border-top-right-radius:3px;
  border-right:none;
}
  
tr {
  border-top: 1px solid #C1C3D1;
  border-bottom-: 1px solid #C1C3D1;
  color:#666B85;
  font-size:16px;
  font-weight:normal;
  text-shadow: 0 1px 1px rgba(256, 256, 256, 0.1);
}
 
tr:hover td {
  background:#4E5066;
  color:#FFFFFF;
  border-top: 1px solid #22262e;
}
 
tr:first-child {
  border-top:none;
}

tr:last-child {
  border-bottom:none;
}
 
tr:nth-child(odd) td {
  background:#EBEBEB;
}
 
tr:nth-child(odd):hover td {
  background:#4E5066;
}

tr:last-child td:first-child {
  border-bottom-left-radius:3px;
}
 
tr:last-child td:last-child {
  border-bottom-right-radius:3px;
}
 
td {
  background:#FFFFFF;
  padding:20px;
  text-align:left;
  vertical-align:middle;
  font-weight:300;
  font-size:18px;
  text-shadow: -1px -1px 1px rgba(0, 0, 0, 0.1);
  border-right: 1px solid #C1C3D1;
}

td:last-child {
  border-right: 0px;
}

th.text-left {
  text-align: left;
}

th.text-center {
  text-align: center;
}

th.text-right {
  text-align: right;
}

td.text-left {
  text-align: left;
}

td.text-center {
  text-align: center;
}

td.text-right {
  text-align: right;
}
```

## файл js/main.js:

```js
'use strict';


```
1. Використовуючи методи createElement, setAttribute та append, написати скрипт, що ствоює та заповнює таблицю даних. Результатом повиннв стати така структура:

```html

    <table class="table-fill">
        <thead>
            <tr>
                <th class="text-left">Month</th>
                <th class="text-left">Sales</th>
            </tr>
        </thead>
        <tbody class="table-hover">
            <tr>
                <td class="text-left">January</td>
                <td class="text-left">$ 50,000.00</td>
            </tr>
            <tr>
                <td class="text-left">February</td>
                <td class="text-left">$ 10,000.00</td>
            </tr>
            <tr>
                <td class="text-left">March</td>
                <td class="text-left">$ 85,000.00</td>
            </tr>
            <tr>
                <td class="text-left">April</td>
                <td class="text-left">$ 56,000.00</td>
            </tr>
            <tr>
                <td class="text-left">May</td>
                <td class="text-left">$ 98,000.00</td>
            </tr>
        </tbody>
    </table>

```

