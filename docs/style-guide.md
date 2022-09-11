
# Intro
This is a (flexible) set of coding rules that will guide us through this project. The goal is to make it easier to read our code and to create a universal, easy-to-understand stying ruleset for the project. Please abide by the rules. It will (I cannot emphasise this enough) make reading the code and life easier for anyone unfortunate enough to try to debug the code.

> DO not forget the D.R.Y principle

<br/>
<br/>

## Table of content

1. **Importants rules**
- [writing commit messages](#writing-commit-messages)
- [Writing comments]
2. **Coding rules**
- [html](#html)
    - [Naming classes and IDs](#naming-classes-and-ids)
    - [Organising elements](#organising-elements)

- [css](#css)
    - [Targeting elements](#targeting-elements-in-css)
    - [TYPOGRAPHY](#typography)
    - [Media query](#media-query)

<br/>
<br/>
---
<br/>
<br/>

## Writing comments
Write descriptive and intuitive comments. The comment should tell us what the code is doing, not how it's doing it. If you need an idea of what proper comments look like, t
**HTML**
```html
    <!-- navbar for mobile and desktop-->
  <header class="">
  </header>
```
if it's css:
```css
/* mobile nav[open] overlay*/
main .overlay {
}
```
<br/>
<br/>

## Writing commit messages
Writing good commit names is essential because it aids in future debugging, especially when trying to figure out what introduced a bug. `God abeg` is an example of a commit message that won't help you find the source of your problems.

Read this article for [how to write a proper commit message](https://cbea.ms/git-commit/).


<br/>


### Naming classes and IDs
I am not a master at naming things, but one thing that has been a pain in my ass is reading the names some people give things when they style elements in CSS. Terrible names can and will slow you down.

Here are some rules I like to follow when I name things in html:

1. If the element is a child, I suggest adding a reference to the parent's name.

**Example:**
```html
<div class="hero-img">
  <!-- or -->
<div class="hero-image">
```

2. Don't name things that don't need to be named, especially when a comment would suffice.

**An example of don'ts:**
```html
<nav class="navbar">
```
This is an example of a class that doesn't need to exist. If you're going to name a tag that has its use case literally as its name, let it be in edge cases.

**Example:**

```html
<nav class="desktop">
</nav>

<nav class="mobile">
</nav>
<!-- As you can see, their name suggests that the various menu items are for different views. -->
```

3. Don't use obscure names. Use names that are descriptive or easy to understand.

**Don't:**
```html
<div class="overlay has-fade"></div>
```
you can use:

```html
<div class="mobile-nav-overlay"></div>
```
Don't use obscure names. Use names that are descriptive or easy to understand. If you're going to use short forms, use things everyone will understand or add a comment at the beginning of the document explaining what the short form means.

4. Naming sections: For simplicity, I suggest we name sections like this:
```html
<section class="section-1" id="hero">
<!-- or -->
<section class="section-1 hero">
```
This, in my opinion, is a far simpler and easier-to-understand naming scheme😃. Plus, it follows a congruent naming scheme, so targeting the next section is much easier.

```html
<section class="section-1" id="hero">

<section class="section-2" id="about">
```
Because they follow the same pattern.

<br/>
<br/>

### Organising elements

I'm assuming we all know how to write proper HTML. I can't help you if you don't know how. If you don't, there's a doc somewhere on the internet that I have no idea how to find, so that's your problem. 

The only thing I ask here is that you adhere to the `globally accepted hierarchical standard for writing HTML` (I hope this is a real thing and not something I made up). 
Basically, arrange your elements in the order they will appear on screen (using desktop view as your reference). Don't put a `h1` tag at the bottom of the document and use `position:` to move it to the top. If you do, I'll do everything in my power to have you locked up in a mental institution.

<br/>
<br/>


### Targeting elements in css
Please write your style in a tree format, starting from the grandparent to the child.

**Example:**

```css
section.section-b .gallery-story .header h1{

}
```
that way it will be to understand what your styling does, and you wowuldn't have to give comments about it.
<br/>
<br/>

### Typography
The default font size for this website is `10px = 1em`.
The `em` unit will be used for this project.

>We are using a `black` and `white` colour scheme because we haven't found a suitable colour scheme for this project. The main priority, for now, is to code out the layout for the website. The colour choice can be decided later, so we can save time.

<br/>
<br/>

### Media query
For easier readability, all media queries should be at the bottom of the style sheet. Putting it in between lines of code is just plain satanic behaviour.