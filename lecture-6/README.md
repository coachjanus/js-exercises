# js-dev-exercises

## Exercises for lecture #6 - Components

1. В середині exercises створіть піддирексторію lecture-6. В середині lecture-6 створіть файли index.html, css/main.css та js/main.js. 

## файл index.html:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Web component</title>  
    <link rel="stylesheet" href="css/main.css">
    
  </head>
  <body>
    <header>
        <nav>
          <ul>
            <li><a href="about.html">About</a></li>
            <li><a href="work.html">Work</a></li>
            <li><a href="contact.html">Contact</a></li>
          </ul>
        </nav>
      </header>

        <main>
          <!-- Your page's content -->
        </main>
      <footer>
        <ul>
          <li><a href="about.html">About</a></li>
          <li><a href="work.html">Work</a></li>
          <li><a href="contact.html">Contact</a></li>
        </ul>
        <ul class="social-row">
          <li><a href="https://github.com/my-github-profile"><i class="fab fa-github"></i></a></li>
          <li><a href="https://twitter.com/my-twitter-profile"><i class="fab fa-twitter"></i></a></li>
          <li><a href="https://www.linkedin.com/in/my-linkedin-profile"><i class="fab fa-linkedin"></i></a></li>
        </ul>
      </footer>
  
    <script type="module" src="js/main.js"></script>
  </body>
</html>

```
## Вміст css/main.css:
```css

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html, body {
  height: 100%;
}

body {
  color: #333;
  font-family: sans-serif;
  display: flex;
  flex-direction: column;
}

main {
  flex: 1 0 auto;
}

        nav {
          height: 40px;
          display: flex;
          align-items: center;
          justify-content: center;
          background-color:  #0a0a23;
        }

        ul {
          padding: 0;
        }
        
        a {
          font-weight: 700;
          margin: 0 25px;
          color: #fff;
          text-decoration: none;
        }
        
        a:hover {
          padding-bottom: 5px;
          box-shadow: inset 0 -2px 0 0 #fff;
        }

      footer {
          height: 60px;
          padding: 0 10px;
          list-style: none;
          display: flex;
          justify-content: space-between;
          align-items: center;
          background-color: #dfdfe2;
        }
        
        footer ul li {
          list-style: none;
          display: inline;
        }
        
        footer a {
          margin: 0 15px;
          color: inherit;
          text-decoration: none;
        }
        
        footer a:hover {
          padding-bottom: 5px;
          box-shadow: inset 0 -2px 0 0 #333;
        }
        
        .social-row {
          font-size: 20px;
        }
        
        .social-row li a {
          margin: 0 15px;
        }

```


## файл js/main.js:

```js
'use strict';


```
- створити власні елементи header-component для верхнього і footer-component для нижнього колонтитулів, замінивши ними header і footer блоки відповідно.
