# App.scss - SCSS Styling Documentation :art:
In this documentation, we'll explain the SCSS styling present in the **`App.scss`** file for a React application. :rocket:

## General Styles :triangular_ruler:
**`.app`**, **`.app__whitebg`**, and **`.app__primarybg`** are used to set background colors and font family for the entire application. :art:

```scss
.app {
  background-color: var(--primary-color);
  font-family: var(--font-base);
}

.app__whitebg {
  background-color: var(--white-color);
}

.app__primarybg {
  background-color: var(--primary-color);
}
``````
## Container and Flex Styles :package:
**`.app__container`** sets styles for the main container of the application. It is a flex container with a row direction, taking up the full width and at least the full height of the viewport. :card_file_box:

```scss 
.app__container {
  width: 100%;
  min-height: 100vh;
  display: flex;
  flex-direction: row;
}
``````

**`.app__flex`** defines a flex container with centered content both horizontally and vertically. It can be used to wrap elements and apply flexbox layout. :bento:

```scss
.app__flex {
  display: flex;
  justify-content: center;
  align-items: center;
}
``````
## Wrapper Styles :gift:
**`.app__wrapper`** sets styles for a flexible wrapper component inside the container. It takes up all available space, has a column direction, and has padding around its content. On smaller screens (max-width: 450px), the padding is adjusted. :gift:

```scss 
.app__wrapper {
  flex: 1;
  width: 100%;
  flex-direction: column;
  padding: 4rem 2rem;

  @media screen and (max-width: 450px) {
    padding: 4rem 1rem 2rem;
  }
}
``````
##Text and Typography Styles :pencil2:
**`.head-text`** sets styles for the heading text. It has varying font sizes based on different screen sizes, and it is centered and capitalized. The text inside the span element has a different color. :bookmark_tabs:

```scss 
.head-text {
  font-size: 2.75rem;
  font-weight: 800;
  text-align: center;
  color: var(--black-color);
  text-transform: capitalize;

  span {
    color: var(--secondary-color);
  }

  @media screen and (min-width: 2000px) {
    font-size: 4rem;
  }

  @media screen and (max-width: 450px) {
    font-size: 2rem;
  }
}
``````
**`.p-text`** sets styles for paragraph text. It has varying font sizes based on different screen sizes and a left-aligned text alignment. :memo:

```scss 
.p-text {
  font-size: 0.8rem;
  text-align: left;
  color: var(--gray-color);
  line-height: 1.5;

  @media screen and (min-width: 2000px) {
    font-size: 1.75rem;
  }
}
``````
**`.bold-text`** sets styles for bold text. It has varying font sizes based on different screen sizes and is left-aligned. :black_nib:

```scss 
.bold-text {
  font-size: 1rem;
  font-weight: 800;
  color: var(--black-color);
  text-align: left;

  @media screen and (min-width: 2000px) {
    font-size: 2rem;
  }

  @media screen and (max-width: 450px) {
    font-size: 0.9rem;
  }
}
``````
## Social Media Icons Styles :earth_americas:
**`.app__social`** sets styles for social media icons. It is a flex container with centered and aligned content. The icons have a circular shape, a background color, and a border. On hover, the background and border colors change, and the icon color changes to white. On larger screens (min-width: 2000px), the icons have larger dimensions. :computer:

```scss 
.app__social {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  flex-direction: column;
  padding: 1rem;

  div {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background-color: var(--white-color);
    margin: 0.25rem 0;
    border: 1px solid var(--lightGray-color);
    display: flex;
    justify-content: center;
    align-items: center;
    transition: all 0.3s ease-in-out;

    svg {
      width: 15px;
      height: 15px;
      color: var(--gray-color);
    }

    &:hover {
      background-color: var(--secondary-color);
      border-color: var(--secondary-color);
      svg {
        color: var(--white-color);
      }
    }

    @media screen and (min-width: 2000px) {
      width: 70px;
      height: 70px;
      margin: 0.5rem 0;

      svg {
        width: 30px;
        height: 30px;
      }
    }
  }
}
``````
## Navigation Dots Styles :large_blue_circle:
**`.app__navigation`** sets styles for navigation dots. It is a flex container with centered and aligned content. The dots have a circular shape, a background color, and a margin. On hover, the background color changes to the secondary color. On larger screens (min-width: 2000px), the dots have larger dimensions. :round_pushpin:

```scss 
.app__navigation {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding: 1rem;

  .app__navigation-dot {
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background-color: #cbcbcb;
    margin: 0.5rem;
    transition: background-color 0.2s ease-in-out;

    &:hover {
      background-color: var(--secondary-color);
    }

    @media screen and (min-width: 2000px) {
      width: 20px;
      height: 20px;
    }
  }
}
``````
## Media Query :iphone:
At max-width: 500px, the `.app__navigation` and `.app__social` containers are hidden. The padding of .copyright is adjusted.

```scss 
@media screen and (max-width: 500px) {
  .app__navigation,
  .app__social {
    display: none;
  }

  .copyright {
    padding: 2rem;
  }
}
``````
With these styles, the App.scss file defines the SCSS styles