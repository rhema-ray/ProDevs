
# Intro
This is a (flexible) set of coding rules that will guide us through this project. The goal is to make it easier to read our code and to create a universal, easy-to-understand stying ruleset for the project. Please abide by the rules. It will (I cannot emphasise this enough) make reading the code and life easier for anyone unfortunate enough to try to debug the code.

> DO not forget the D.R.Y principle

# Table of content

**importants rules**
- [writing commit messages](#writing-commit-messages)

**Coding rules**
- [html](#html)
    - [Naming classes and IDs](#naming-classes-and-ids)
    - [Organising elements](#organising-elements)

- [css](#css)
    - [Targeting elements](#targeting-elements-in-css)
    - [TYPOGRAPHY](#typography)
    - [Media query](#media-query)



## Writing commit messages
Writing good commit names is essential because it aids in future debugging, especially when trying to figure out what introduced a bug. ==God abeg== is an example of a commit message that won't help you find the source of your problems.

Read this article for [how to write a proper commit message](https://cbea.ms/git-commit/).


<br/>

## html

### Naming classes and IDs

### Organising elements

I'm assuming we all know how to write proper HTML. I can't help you if you don't know how. If you don't, there's a doc somewhere on the internet that I have no idea how to find, so that's your problem. 

The only thing I ask here is that you adhere to the ==globally accepted hierarchical standard for writing HTML== (I hope this is a real thing and not something I made up). 
Basically, arrange your elements in the order they will appear on screen (using desktop view as your reference). Don't put a `h1` tag at the bottom of the document and use `position:` to move it to the top. If you do, I'll do everything in my power to have you locked up in a mental institution.

<br/>
<br/>

## css
<br/>
<br/>

### targeting elements in css
Please write your style in a tree format, starting from the grandparent to the child.

**Example:**

```css
.section-b .gallery-story .header h1{

  }
```


### TYPOGRAPHY
The default font size for this website is `10px = 1em`.
The `em` unit will be used for this project.

>We are using a `black` and `white` colour scheme because we haven't found a suitable colour scheme for this project. The main priority, for now, is to code out the layout for the website. The colour choice can be decided later, so we can save time.

### Media query
For easier readability, all media queries should be at the bottom of the style sheet. Putting it in between lines of code is just plain satanic behaviour.