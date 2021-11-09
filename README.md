# Frontend Mentor - 3-column preview card component solution

This is a solution to the [3-column preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/3column-preview-card-component-pH92eAR2-). 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![desktop-design](https://user-images.githubusercontent.com/58538880/140853438-3b89c65a-3171-4c1b-9447-9b53d3ff8491.jpg)
![mobile-design](https://user-images.githubusercontent.com/58538880/140853442-864703b8-47cd-4e1f-ab7c-29db3f5b036d.jpg)


### Links

- Live Site URL: [Live Demo](https://rluna15.github.io/3-column-preview-card-component-main/)

## My process

### Built with

- HTML 5
- Sass
- Flex Box (Styling)
- Gulp (Compile Sass)

### What I learned
For this component using the flex box made much simpler to create the equal spaced sections of the card.

```css
@use "../util" as *;
@use "../globals/" as *;

.card {
  width: 920px;
  height: 500px;
  border-radius: 10px;
  overflow: hidden;
  display: flex;

  & > div {
    padding: 48px;

    & > button {
      margin-top: 75px;
    }
  }

  & > div > h1 {
    color: $Very-light-gray;
    font-size: 35px;
    font-family: $Big-Shoulders;
    font-weight: 700;
    text-transform: uppercase;
    margin: 40px 0 40px 0;
  }

  & > div > p {
    color: $Transparent-white;
    font-family: $Lexend-Deca;
  }

  &-orange {
    background-color: $Bright-orange;
  }

  &-cyan {
    background-color: $Dark-cyan;
  }

  &-dark-cyan {
    background-color: $Very-dark-cyan;
  }

  @include breakpoint-down(small){
    width: 327px;
    height: 1326px;
    flex-direction: column;
    margin: 88px 0px 88px 0;

    & > div {
      // padding: 48px;
  
      & > button {
        margin-top: 30px;
      }
    }
  }
}

```


