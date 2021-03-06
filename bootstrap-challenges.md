# Bootstrap Challenges

| Objectives |
| :--- |
| Explain why UX is important as a developer |
| Build a static webpage with HTML and CSS (review) |
| Add the Bootstrap library to your projects |

## Challenges
1. Create an `index.html` file and add the [Bootstrap CDN](http://getbootstrap.com/getting-started/#download) (or use this [Bootstrap boilerplate](https://github.com/sf-wdi-19-20/modules/tree/master/w1_d2_2_bootstrap_css/bootstrap_boilerplate) to get started)
2. Add one `.container`, one `.row`, and three `.col-*` classes (your columns can be any widths that add up to 12)
3. Make these girds
  * Mobile (xs) - 12/12
  * Tablet (sm) - 4/8
  * Laptop (md) - 4/8
  * Desktop (lg) - 3/7 (offset-1)
3. Make these girds
  * Mobile (xs) - 3/9
  * Tablet (sm) - 4/8
  * Laptop (md) - 5/7
  * Desktop (lg) - 5/5 (offset-1)
4. Add some [buttons](http://getbootstrap.com/css/#buttons) (you can even put [icons](http://getbootstrap.com/components/#glyphicons) inside!)

## Stretch Challenges
1. Add a [nav bar](http://getbootstrap.com/components/#navbar) to the top of your page.
2. Add a [form](http://getbootstrap.com/css/#forms) to your page.
3. Visit [Bootsnipp](http://bootsnipp.com), and choose any element(s) from the gallery to add to your page. (**Hint:** You will have to add your own stylesheet if any extra CSS is required for the element(s) you choose)

## Further Reading

#### HTML & CSS
  * [Learn CSS Layout](http://learnlayout.com)
  * [WTF, HTML and CSS?](http://wtfhtmlcss.com)
  * [Opening the Box Model](http://learn.shayhowe.com/html-css/opening-the-box-model)
  * [70 Expert Ideas For Better CSS Coding](http://www.smashingmagazine.com/2007/05/10/70-expert-ideas-for-better-css-coding)

#### Bootstrap
  * [Understanding the Bootstrap Grid System](https://scotch.io/tutorials/understanding-the-bootstrap-3-grid-system)
  * [Inspiring Uses of Bootstrap](http://expo.getbootstrap.com)

#### Other CSS Frameworks
  * [Foundation](http://foundation.zurb.com)
  * [Pure.css](http://purecss.io)

#### UX & UI
  * [UX is UI](https://medium.com/@mikeatherton/ux-is-ui-105460807734)
  * [A Good User Interface](http://goodui.org)
  * [[VIDEO] Designing for Cross-Screen Experiences](http://aneventapart.com/news/post/screen-time-an-event-apart-video-by-luke-wroblewski)


  #### Bootstrap Boilerplate

  ```html
  <!DOCTYPE html>
  <html>
  <head>
    <meta charset="utf-8">

    <!-- set viewport to device width to allow responsiveness -->
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap CDN -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">

    <!-- custom styles (always require after Bootstrap) -->
    <link rel="stylesheet" href="style.css">

    <title>Bootstrap Boilerplate</title>
  </head>
  <body>
    <div class="container">
      <div class="row">
        <div class="col-sm-6">
          <h1>col-sm-6</h1>
          <p>These columns take up half the page.</p>
        </div>
        <div class="col-sm-6">
          <h1>col-sm-6</h1>
          <p>And they take up the whole page on small devices.</p>
        </div>
      </div>
    </div>
  </body>
  </html>
  ```
