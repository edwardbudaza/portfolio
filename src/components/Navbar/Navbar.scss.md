# SCSS Styling Documentation :nail_care:

This file contains the SCSS (Sass) stylesheet for styling a React application's Navbar component. :computer:

## .app__navbar :house:

- **Description** : This is the main container for the Navbar component. It spans the entire width of its parent container and uses a flexbox layout to align its children horizontally. The children are vertically centered within the Navbar. :house_with_garden:

- **Styles** : 
```scss
width: 100%;
display: flex;
justify-content: space-between;
align-items: center;
padding: 1rem 2rem;
background: rgba(255, 255, 255, 0.25);
backdrop-filter: blur(4px);
-webkit-backdrop-filter: blur(4px);
border: 1px solid rgba(255, 255, 255, 0.18);
position: fixed;
z-index: 2;
``````
## .app__navbar-logo :art:
- **Description** : This is the container for the logo within the Navbar. It aligns the logo to the left side and vertically centers it. The logo's image has fixed dimensions of 250px width and 50px height, which change to 360px width and 80px height when the screen width is at least 2000px. :leftwards_arrow_with_hook:

- **Styles** : 
```scss
display: flex;
justify-content: flex-start;
align-items: center;
``````
## .app__navbar-links :link:
- **Description** : This is the container for the navigation links within the Navbar. It allows the links to take up all available space in the Navbar, pushing the logo to the left and the menu button to the right. The links are centered horizontally and vertically. The default list-style bullet points are removed from the list items. Each list item (li) has a horizontal margin for spacing between each link and a pointer cursor on hover. The link text is transformed to uppercase and made bold. A smooth transition effect is added for changes in link appearance, and the link color changes on hover using custom CSS variables. :mag_right:

- **Styles** : 
```scss
flex: 1;
display: flex;
justify-content: center;
align-items: center;
list-style: none;
``````
## .app__navbar-menu :hamburger:
- **Description** : This is the container for the menu button (hamburger icon) within the Navbar. It creates a circular shape for the menu button and aligns it both horizontally and vertically. The menu button has a background color using a custom CSS variable. The SVG icon inside the menu button has fixed dimensions and color. :sparkles:

- **Styles** : 
```scss
width: 35px;
height: 35px;
border-radius: 50%;
position: relative;
display: flex;
justify-content: center;
align-items: center;
background-color: var(--secondary-color);
``````
## Media Queries :iphone:
- **Description** : For screens with a width of 900px or less, the` .app__navbar-links` and `.app__navbar-menu` containers have display: none, which hides the navigation links and menu button, effectively creating a responsive design for smaller screens. :twisted_rightwards_arrows:


- **Styles** : 
```scss
@media screen and (max-width: 900px) {
  .app__navbar-links, .app__navbar-menu {
    display: none;
  }
}
``````
It's important to note that some of the styles depend on custom CSS variables like `--gray-color`, `--secondary-color`, and `--white-color`. The actual values of these variables would be defined elsewhere in the CSS or SCSS file or in a theme file. :bookmark_tabs:

Overall, this SCSS file is responsible for creating a responsive and visually appealing Navbar for the React application. :sparkling_heart:
 