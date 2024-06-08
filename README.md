# Frontend Mentor - Launch countdown timer solution

This is a solution to the [Launch countdown timer challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/launch-countdown-timer-N0XkGfyz-). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Frontend Mentor - Launch countdown timer solution](#frontend-mentor---launch-countdown-timer-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
  - [Author](#author)
  - [Acknowledgments](#acknowledgments)
  - [Remaining Work](#remaining-work)


## Overview

### The challenge

Users should be able to:

- See hover states for all interactive elements on the page
- See a live countdown timer that ticks down every second (start the count at 14 days)
- **Bonus**: When a number changes, make the card flip from the middle

### Screenshot

![](./image.png)

### Links

- Solution URL: [Github](https://github.com/bhaskrr/launch-countdown-timer)
- Live Site URL: [Vercel](https://launch-countdown-timer-pink.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- [React](https://reactjs.org/) - JS library

### What I learned

```css
#root {
    background-image: linear-gradient(0deg, #1d1127 20%, #232022 100%), url('/images/bg-stars.svg');
    background-blend-mode: hue;
}
```
```js
function CountdownTimer({ duration }) {
  
  const [time, setTime] = useState(duration);

  useEffect(()=>{
    setTimeout(() => {
      setTime(time - 1000);
    }, 1000);
  }, [time]);

  const getFormattedTime = (miliseconds) => {
    let totalSeconds = parseInt(Math.floor(miliseconds / 1000));
    let totalMinutes = parseInt(Math.floor(totalSeconds / 60));
    let totalHours = parseInt(Math.floor(totalMinutes / 60));
    let totalDays = parseInt(Math.floor(totalHours / 24));

    let seconds = parseInt(totalSeconds % 60);
    let minutes = parseInt(totalMinutes % 60);
    let hours = parseInt(totalHours % 24);

    return {totalDays, hours, minutes, seconds};
  }
```

## Author

- Github - [Bhaskar](https://github.com/bhaskrr/)
- Frontend Mentor - [@bhaskrr](https://www.frontendmentor.io/profile/bhaskrr)

## Acknowledgments

[This](https://www.youtube.com/watch?v=7CQdoqP5qj0) video helped me to build the project.Thanks to the creator.

## Remaining Work

- Could not implement the bonus challange