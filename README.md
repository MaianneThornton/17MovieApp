# 50 Projects in 50 Days - Movie App

This is a code along project in the [50 Projects In 50 Days - HTML, CSS & JavaScript Udemy Course](https://www.udemy.com/course/50-projects-50-days/). Sharpen your skills by building 50 quick, unique & fun mini projects.

## Table of contents 😌

- [Overview](#overview)
  - [The project](#the-project)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Code snippets](#im-really-proud-of-these-code-snippets%EF%B8%8F)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview👋🏾

Welcome to the 17<sup>th</sup> mini-project of the course!

### The project😥

In this project users will be able to:

- Build a movie app by accessing a third-party API.

### Screenshot🌇

![](./screenshot.png)

### Links👩🏾‍💻

- Live Site URL: (https://maiannne-movieapp.netlify.app/)

## My process💭

I started by creating the UI for the project by marking out initial classes and id's in HTML to be later used for styling. (I later removed these and re-added them dynamically using JavaScript.) Next I styled the CSS by styling the main, movie, movie-info, and overview sections. I then added functionality by way of JavaScript to access the moviedb API and display the movie information. I then added search functionality so that users can access the API's information by entering a query in the search bar. I also added pagination, where users can click anywhere on the movie card and go to the moviedb page dedicated to the movie.

### Built with👷🏾‍♀️

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- JavaScript
- Asynchronous API

### What I learned👩🏾‍🏫

I learned the logic behind making a movie app functional. I will be applying this to future projects where needed.

### Continued development🔮

In the future I plan on continuing to practice accessing different API endpoints to make calls and display in different apps.

I plan on continuing to practice using transition & and transform properties to make my sites look more exciting.

I also plan on continuing to practice using event listeners to make my pages more functional.

I also plan on continuing to learn the best ways to phrase git commits, so that future viewers can fully understand the changes that have occurred.

### I'm really proud of these code snippets✂️

```css
.overview {
  background-color: #fff;
  padding: 2rem;
  position: absolute;
  left: 0;
  bottom: 0;
  right: 0;
  max-height: 100%;
  transform: translateY(101%);
  transition: transform 0.3s ease-in;
}

.movie:hover .overview {
  transform: translateY(0);
  overflow: scroll;
}
```

```js
function showMovies(movies) {
  main.innerHTML = '';

  movies.forEach((movie) => {
    const { title, poster_path, vote_average, overview, id } = movie;

    const movieEl = document.createElement('div');
    movieEl.classList.add('movie');

    movieEl.innerHTML = `
        <a href='${MOVIE_PAGE + id}'>
            <img
                src="${IMG_PATH + poster_path}"
                alt="${title}"/>
        <div class="movie-info">
          <h3>${title}</h3>
          <span class="${getClassByRate(vote_average)}">${vote_average}</span>
        </div>
        <div class="overview">
          <h3>Overview</h3>
          ${overview}
        </div>
        </a>
      </div>
    `;
    main.appendChild(movieEl);
  });
}
```

### Useful resources📖

- [Resource](https://www.freecodecamp.org/news/how-to-write-better-git-commit-messages/) - This is an amazing article which helped me write better commit messages. I'd recommend it to anyone still learning this concept.

## Author🔎

- Website - [Portfolio Site](https://www.maiannethornton.com/Portfolio/index.html)
- Frontend Mentor - [@MaianneThornton](https://www.frontendmentor.io/profile/MaianneThornton)
- GitHub - [@MaianneThornton](GitHub.com/MaianneThornton)
- Twitter - [@MaianneThornton](https://twitter.com/MaianneThornton)
- LinkedIn - [@MaianneThornton](https://www.linkedin.com/in/maiannethornton/)

## Acknowledgments🙏🏾

Special Thanks go to [Brad Traversy](http://www.traversymedia.com/) and [Florin Pop](http://www.florin-pop.com/) creating the course and making reviewing concepts fun 😊.
