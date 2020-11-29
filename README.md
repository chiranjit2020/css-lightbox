# Simple CSS Lightbox
  Simple Lightbox using CSS **(NO JAVASCRIPT)**
***

#### HTML
 ```html
    <div class="block">
        <h1>Scroll your Mouse.</h1>
    </div>
    <div class="links">
        <a href="#section1">section 1</a>
        <a href="#section2">section 2</a>
        <a href="#section3">section 3</a>
    </div>


    <section class="section " id="section1">
        <h1>Section 1</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Obcaecati impedit, beatae qui, maiores quae, ab officia ratione tenetur voluptates perferendis eius saepe minus, commodi similique quam tempora unde laboriosam ex? Velit corporis minima explicabo, eligendi quod, iure cumque facere, sed modi tempora enim optio. Doloribus similique temporibus placeat, et laborum.</p>
        <a href="#!" class="close">Close</a>
    </section>

    <section class="section " id="section2">
        <h1>Section 2</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Obcaecati impedit, beatae qui, maiores quae, ab officia ratione tenetur voluptates perferendis eius saepe minus, commodi similique quam tempora unde laboriosam ex? Velit corporis minima explicabo, eligendi quod, iure cumque facere, sed modi tempora enim optio. Doloribus similique temporibus placeat, et laborum.</p>
        <a href="#!" class="close">Close</a>
    </section>
    <section class="section " id="section3">
        <h1>Section 3</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Obcaecati impedit, beatae qui, maiores quae, ab officia ratione tenetur voluptates perferendis eius saepe minus, commodi similique quam tempora unde laboriosam ex? Velit corporis minima explicabo, eligendi quod, iure cumque facere, sed modi tempora enim optio. Doloribus similique temporibus placeat, et laborum.</p>
        <a href="#!" class="close">Close</a>
    </section>
```
#### CSS
***
```css
        * {
            padding: 0;
            margin: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
        }

        .block {
            height: 100vh;
            background: lightblue;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .links {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: pink;
        }

        .links a {
            display: inline-block;
            text-decoration: none;
            font-size: 18px;
            color: #fff;
            line-height: 1.3;
            text-transform: uppercase;
            background-color: #fd017f;
            padding: 10px 25px;
            margin: 10px;
            box-shadow: 0 0 15px 0 rgba(255, 80, 167, .7);
            transition: all .3s ease;
        }

        .links a:hover {
            background-color: #d4006a;
        }

        section {
            position: fixed;
            left: 0;
            top: 0;
            width: 100%;
            height: 100vh;
            background-color: aliceblue;
            color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            padding: 0 30%;
            transform: scale(1, 0);
            transform-origin: top;
            transition: all .5s cubic-bezier(.04, .85, .26, .88);
        }

        .section .close {
            display: inline-block;
            text-decoration: none;
            font-size: 18px;
            color: #fff;
            line-height: 20px;
            text-transform: uppercase;
            background-color: #fd017f;
            padding: 10px 30px;
            margin: 10px;
            box-shadow: 0 0 15px 0 rgba(255, 80, 167, .7);
        }

        #section1:target {
            background-color: #123;
            transform: scale(1);
        }

        #section2:target {
            background-color: #456;
            transform: scale(1);
        }

        #section3:target {
            background-color: #789;
            transform: scale(1);
        }

```