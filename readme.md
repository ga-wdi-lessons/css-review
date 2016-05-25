# CSS Review

## Learning Objectives
- Describe what on a webpage can be modified with CSS, and what cannot
- Identify CSS methods that can replace bad habits in HTML
- Properly separate the concerns of semantics and style
- Identify the components of the box model
- Differentiate between border-box and content-box values for box-sizing

## Framing (10 min / 10 min)

### What is CSS?

> Cascading Style Sheets are what make webpages look like more than just words on a page. HTML's only purpose is to say what purpose chunks of content serve; CSS's only purpose is to say what a chunk with a certain purpose should look like.

This lesson is going to be almost entirely you working through some exercises we have prepared for you. You will not turn in these exercises. However, whoever completes them first and best gets bragging rights!

These exercises may use CSS properties with which you're unfamiliar. In fact, you may not be familiar with CSS at all.


### What should you do if something is unfamiliar?

> 1. Read it like English. CSS is intended to be readable, although sometimes it's more successful than at other times.
> 2. Look it up. If you don't know what `box-sizing` means, Google `css box-sizing`.

The purpose of this class isn't for you to walk away being an expert in all things CSS. That takes months. Rather, it's for you to be exposed to all the things that can be accomplished with CSS. If they're on your radar, you can always look them up later.

Remember: being a good web designer is like being a good artist. We can teach you to hold the paintbrush, but it's on you to create a masterpiece!

## HTML / CSS Review

See the [slides](html_css_review.pdf).

### The Three Places CSS can go

#### Inline Styles (Bad)

```html
<section>
  <article style='border-bottom: 1px solid black;'>
     ...
  </article>
</section>
```

#### Internal Styles (Better)

```html
<!doctype html>
<html>
  <head>
    <style>
      article {
        border-bottom: 1px solid black;
      }
    </style>
  </head>
  <body>
    <section>
      <article>
	 ...
      </article>
    </section>
  </body>
</html>
```

#### External Styles (Best)

```html
<!doctype html>
<html>
  <head>
    <link rel='stylesheet' type='text/css' href='styles.css'>
  </head>
  <body>
    <section>
      <article>
	 ...
      </article>
    </section>
  </body>
</html>
```

```css
/* styles.css */

article {
  border-bottom: 1px solid black;
}
```

### Selecting Elements

| Pattern | Meaning |
|---|---|
| * | any element |
| E | an element of type E |
| #myid | any element with ID equal to "myid" |
| .myclass | any element with class equal to "myclass" |
| E#myid | an E element with ID equal to "myid" |
| E.myclass | an E element with class equal to "myclass" |
| E F | an F element child of an E element |

[And many more!](https://www.w3.org/TR/css3-selectors/#selectors)

## You Do: [CSS Diner](http://flukeout.github.io/)

### Box Model

![](https://dl.dropbox.com/s/d1fk9mu23q0byhh/Screenshot%202016-05-25%2009.08.53.png?dl=0)

The Box Model explains how CSS Width is Calculated

How big is the box in [box-model.html](http://www.wdidc.org/~jesse/box-model.html)?

## You Do: CSS Crash Course (30 min / 40 min)

Please count off from 1 to `[class size / 2]`. In pairs, please work to complete this exercise:

[CSS Review Exercise](https://github.com/ga-wdi-exercises/css-review)

Whoever completes the most questions gets bragging rights!

### Questions (10 min / 60 min)

## Break (10 min / 50 min)

## You do: Fashion Blog

[fashion blog](https://github.com/ga-wdi-exercises/fashion-blog)

Check out https://www.google.com/fonts/specimen/Lato
and https://itunes.apple.com/us/app/sip/id507257563?mt=12

### Questions (10 min / 100 min)

## Bonus! You Do: eCardly

Please count off again, and complete this exercise:

[eCardly](https://github.com/ga-wdi-exercises/ecardly)



### Questions (10 min / 140 min)

## Outtro

There are over 500 CSS properties. It's impossible to memorize them. The key is to just get an idea of what you can accomplish with CSS, and then know what to Google.

### Tools that can help

**[The CSS Validator](http://jigsaw.w3.org/css-validator/#validate_by_input)** is a tool into which you can copy and paste your CSS, and it'll tell you precisely what's wrong with it. We'll be expecting you to validate your CSS during this course.

**The Chrome element inspector** lets you look at a specific element on a page, see exactly which CSS rules are being applied to it, and turn those rules on and off and modify them. It doesn't change your file; refresh the page, and the changes are gone.

Q. What is Bootstrap, and how do you feel about it?
---
> Bootstrap is a CSS *library*: it's a stylesheet you can link to in your HTML, and it provides you with a bunch of classes that you can apply that make things look really nice.

> Many designers sniff at Bootstrap because, they argue, sites that use it all look the same. However, unless you plan on specializing in front-end design, a Bootstrapped site may be better than a site with no CSS, or a site with handmade CSS: it shows that you recognize what your strengths are and are focused on delivering a product, rather than doing things the "right" way.

## Quiz Questions

- What is the purpose of `flex-box`?
- What does `*` select?
- What does `box-sizing:border-box` do?
- What's the difference between `position:relative`, `position:absolute`, and `position:fixed`?
- What's the difference between borders, margins, and padding?
- What's the difference between an outline and a border?
- How would you apply styles only for screens narrower than 480 pixels?

## Further Reading

- [Shay Howe's HTML/CSS Guide](http://learn.shayhowe.com)
- [LearnLayout.com](http://learnlayout.com/)
  - An great interactive tutorial that details CSS' many properties and quirks.
- [W3Schools CSS Reference](http://www.w3schools.com/cssref/default.asp)
  - Almost every CSS property ever.
- [Mozilla Developer Network CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)
  - Like W3Schools, but in *much* more detail.
- [CanIUse.com](http://caniuse.com/)
  - Search for a CSS property (or HTML, or JS), and it'll tell you on which web browsers it functions.
- [CSS Validator](https://jigsaw.w3.org/css-validator/#validate_by_input)
  - Copy and paste your CSS in here and it tells you what's wrong with it.
- [CSS Tricks Almanac](https://css-tricks.com/almanac/)
  - A list of css selectors and properties
- [CSS Units - em vs px etc](http://kyleschaeffer.com/development/css-font-size-em-vs-px-vs-pt-vs/)
