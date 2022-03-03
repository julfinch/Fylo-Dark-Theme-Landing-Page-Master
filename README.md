# Frontend Mentor - Fylo dark theme landing page solution

This is a solution to the [Fylo dark theme landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/fylo-dark-theme-landing-page-5ca5f2d21e82137ec91a50fd). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)


## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page

### Screenshot

![](./screenshot.png)

### Links

- Solution URL: [https://www.frontendmentor.io/solutions/responsive-fylo-landing-page-using-flexbox-and-css-grid-Krge9PRCB](https://www.frontendmentor.io/solutions/responsive-fylo-landing-page-using-flexbox-and-css-grid-Krge9PRCB)
- Live Site URL: [https://julfinch.github.io/Fylo-Dark-Theme-Landing-Page-Master/](https://julfinch.github.io/Fylo-Dark-Theme-Landing-Page-Master/)

## My process

1. Create the Header where the logo and the links will stay.
2. Next is to create and Intro Section where we will put the Intro Illustration first and right after it is the Intro Comments and the Get Started button.
3. I applied the bg-curvy illustration as background image in this section so that it will overlap its top part just below the Intro Illustration on mobile layout later on as shown in the design specification of this challenge (mobile-design under the folder named "design").
4. In the Grid Section, I used CSS Grid to form the 2x2 layout where the features are shown.
5. Next is the Productive Section where I created a wrapper for the 2 div boxes, the left one for the image and the right one for the paragraphs.
6. For the Testimonial Section, I used the Flex property with a value of 1 so that the three testimonial cards will have the same layout. I created a wrapper for the 3 cards and I positioned the quote image at the top left of this box and to constrict its position just right the the top left corner of the first testimonial card whenever the layout changes to a smaller screen.
7. Under the Footer Section, I created the "Early Access Card" and positioned it so that the upper half will protrude above the top border of the Footer.
8. I finished the project by completing the details in the Footer where I used Flexbox.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Javascript

### What I learned

1. This is my first time using CSS Grid because I always use Flexbox to my projects for the mobile responsiveness layout. I applied it in the Grid Section, the one after the Intro, where I decided to give it a try since the layout is a 2x2 grid boxes and I know Grids are meant for this kind of arrangement.

2. In the Testimonial Section, to apply the same layout and size on three cards, I used for the first time the Flexbox property of flex with a value of 1 as shown in the code below:
```css
.card {
    display: flex;
    flex-wrap: wrap;
    flex: 1;
```
3. Learning and looking for a way for validating emails is what make me took longer to finish this project since I am trying to create a code in javascript that will do just what I wanted as a result. This coding challenge wants the email validation message to appear right below the input text of the form. For this to be achieved, I created a blank paragraph tag in the forms section with an ID "emailValidationMessage" and message should appear in it during the process after targeting it. 

```html
<form name="form1" action="#" onload='document.form1.text1.focus()'>
  <input type="text" id="email" name="text1" placeholder="email@example.com" required>
  <input type="button" id="submit" value="Get Started For Free" onclick="ValidateEmail(document.form1.text1)">
</form>

<p id="emailValidationMessage">
</p>
```
I already provided a link below for this topic, feel free to check it. The code provided on it uses an alert that will popup after validating the email, something that is not what I wanted because I want the message to appear in the blank p tag instead. To solve this, I changed it and used HTML DOM where we target the blank p tag using getElementById and have the Javascript put our message on it. The resulting code is shown below: 

```js
function ValidateEmail(inputText)
{
var mailformat = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/;
if(inputText.value.match(mailformat))
{
document.getElementById("emailValidationMessage").innerHTML = "Success!";
document.form1.text1.focus();
return true;
}
else
{
document.getElementById("emailValidationMessage").innerHTML = "Please enter a valid email address";
document.form1.text1.focus();
return false;
}
} 
```

### Continued development

I took this Junior Challenge with a Javascript because I wanted to solve JS-related problem right away and get my hands dirty with it because that is how I learn fast than just reading books about it. Javascript is relatively new to me because I only create static webpages before using HTML and CSS. Thanks to this project for this has sparked an enthusiasm in me to learn more about JS. Learning more about JS is what I currently working on.

### Useful resources

- [HTML DOM](https://www.w3schools.com/js/js_htmldom_html.asp) - This helped me understand the concept of DOM which allows me to change the content of the blank paragraph tag in the forms section so that the messages after email validation will appear just right below the email input bar.
- [Email Validation](https://www.w3resource.com/javascript/form/email-validation.php) - This is an amazing article which helped me understand the concept of validating an email by filtering the inputted text in the form using the correct email format. There are other articles out there with the same concept but I'd recommend this one since it has a proper instruction in applying the code.

## Author

- Frontend Mentor - [@julfinch](https://www.frontendmentor.io/profile/julfinch)
- Twitter - [@julfinch](https://www.twitter.com/julfinch)
