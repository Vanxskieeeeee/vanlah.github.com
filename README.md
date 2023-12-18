<!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <!--==================== UNICONS ====================-->
        <link rel="stylesheet" href="https://unicons.iconscout.com/release/v4.0.0/css/line.css">
        
        <!--==================== SWIPER CSS ====================-->
        <link rel="stylesheet" href="assets/css/swiper-bundle.min.css">
        
        <!--==================== CSS ====================-->
        <link rel="stylesheet" href="assets/css/styles.css">
        <title>Responsive Portfolio Website</title>
    </head>
    <body>
      <style>
        /*==================== GOOGLE FONTS ====================*/
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600&display=swap");
/*==================== VARIABLES CSS ====================*/
:root {
    --header-height: 4.5rem;
    /*========== Colors ==========*/
    /* Change favorite color */
    --hue-color: 217; /*Purple 250 - Green 158 - Blue 217 - Pink 340*/
    /* HSL color mode */
    --first-color: hsl(var(--hue-color), 69%, 61%);
    --first-color-second: hsl(var(--hue-color), 69%, 61%);
    --first-color-alt: hsl(var(--hue-color), 57%, 53%);
    --first-color-lighter: hsl(var(--hue-color), 92%, 85%);
    --title-color: hsl(var(--hue-color), 8%, 15%);
    --text-color: hsl(var(--hue-color), 8%, 45%);
    --text-color-light: hsl(var(--hue-color), 8%, 65%);
    --input-color: hsl(var(--hue-color), 70%, 96%);
    --body-color: hsl(var(--hue-color), 60%, 99%);
    --container-color: #fff;
    --scroll-bar-color: hsl(var(--hue-color), 12%, 90%);
    --scroll-thumb-color: hsl(var(--hue-color), 12%, 80%);
    /*========== Font and typography ==========*/
    --body-font: 'Poppins', sans-serif;
    /* .5rem = 8px, 1rem = 16px, 1.5rem = 24px ... */
    --big-font-size: 2.25rem;
    --h1-font-size: 1.75rem;
    --h2-font-size: 1.5rem;
    --h3-font-size: 1.25rem;
    --normal-font-size: 1rem;
    --small-font-size: .938rem;
    --smaller-font-size: .813rem;
    /*========== OLD FONT SIZE ==========*/
      /*=====
        --big-font-size: 2rem;
        --h1-font-size: 1.5rem;
        --h2-font-size: 1.25rem;
        --h3-font-size: 1.125rem;
        --normal-font-size: .938rem;
        --small-font-size: .813rem;
        --smaller-font-size: .75rem;
        ====*/
    /*========== Font weight ==========*/
    --font-medium: 500;
    --font-semi-bold: 600;
    /*========== Margenes Bottom ==========*/
    /* .25rem = 4px, .5rem = 8px, .75rem = 12px ... */
    --mb-0-25: .25rem;
    --mb-0-5: .5rem;
    --mb-0-75: .75rem;
    --mb-1: 1rem;
    --mb-1-5: 1.5rem;
    --mb-2: 2rem;
    --mb-2-5: 2.5rem;
    --mb-3: 3rem;
    /*========== z index ==========*/
    --z-tooltip: 10;
    --z-fixed: 100;
    --z-modal: 1000;
}
/* Font size for large devices */
@media screen and (min-width: 968px) {
    :root {
        --big-font-size: 3rem;
        --h1-font-size: 2.25rem;
        --h2-font-size: 1.5rem;
        --h3-font-size: 1.25rem;
        --normal-font-size: 1rem;
        --small-font-size: .875rem;
        --smaller-font-size: .813rem;
    }
}
/*========== Variables Dark theme ==========*/
body.dark-theme{
      /* HSL color mode */
      --first-color-second: hsl(var(--hue-color), 30%, 8%);
      --title-color: hsl(var(--hue-color), 8%, 95%);
      --text-color: hsl(var(--hue-color), 8%, 75%);
      --input-color: hsl(var(--hue-color), 29%, 16%);
      --body-color: hsl(var(--hue-color), 28%, 12%);
      --container-color: hsl(var(--hue-color), 29%, 26% );
      --scroll-bar-color: hsl(var(--hue-color), 12%, 48%);
      --scroll-thumb-color: hsl(var(--hue-color), 12%, 36%);
}
/*========== Button Dark/Light ==========*/
.nav__btns{
  display: flex;
  align-items: center;
}
.change-theme{
  font-size: 1.25rem;
  color: var(#0000);
  margin-right: var(--mb-1);
  cursor: pointer;
}
.change-theme:hover{
  color: var(--first-color);
}
/*==================== BASE ====================*/
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
header{
  margin-top: 0.5rem;
}
html {
  scroll-behavior: smooth;
}
body {
  margin: 0 0 var(--header-height) 0;
  font-family: var(--body-font);
  font-size: var(--normal-font-size);
  background-color: var(--body-color);
  color: var(--text-color);
}
h1, h2, h3, h4 {
  color: var(--title-color);
  font-weight: var(--font-semi-bold);
}
ul {
  list-style: none;
}
a {
  text-decoration: none;
}
img {
  max-width: 100%;
  height: auto;
}
/*==================== REUSABLE CSS CLASSES ====================*/
.section {
  padding: 2rem 0 4rem;
}
.section__title {
  font-size: var(--h1-font-size);
  color: var(--title-color);
}
.section__subtitle {
  display: block;
  font-size: var(--small-font-size);
  margin-bottom: var(--mb-3);
}
.section__title, 
.section__subtitle {
  text-align: center;
}
/*==================== LAYOUT ====================*/
.container {
  max-width: 950px;
  margin-left: var(--mb-1-5);
  margin-right: var(--mb-1-5);
}
.grid {
  display: grid;
  gap: 1.5rem;
}
.header {
  width: 100%;
  position: fixed;
  bottom: 0;
  left: 0;
  z-index: var(--z-fixed);
  background-color: var(--body-color);
}
/*==================== NAV ====================*/
.nav{
  max-width: 980px;
  height: var(--header-height);
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.nav__logo,
.nav__toggle{
  color: var(--title-color);
  font-weight: var(--font-medium);
}
.nav__logo:hover{
  color: var(--first-color);
}
.nav__toggle{
  font-size: 1.1rem;
  cursor: pointer;
}
.nav__toggle:hover{
  color: var(--first-color);
}
@media  screen and (max-width: 767px) {
  .nav__menu{
    position: fixed;
    bottom: -100%;
    left: 0;
    width: 100%;
    background-color: var(--body-color);
    padding: 2rem 1.5rem 4rem;
    box-shadow: 0 -1px 4px rgba(0, 0, 0, .15);
    border-radius: 1.5rem 1.5rem 0 0;
    transition: .3seg;
  }
}
.nav__list{
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
}
.nav__link{
  display: flex;
  flex-direction: column;
  align-items: center;
  font-size: var(--small-font-size);
  color: var(--title-color);
  font-weight: var(--font-medium);
}
.nav__link:hover{
  color: var(--first-color);
}
.nav__icon{
  font-size: 1.2rem;
}
.nav__close{
  position: absolute;
  right: 1.3rem;
  bottom: .5rem;
  font-size: 1.5rem;
  cursor: pointer;
  color: var(--first-color);
}
.nav__close:hover{
  color: var(--first-color-alt);
}
/* show menu */
.show-menu{
  bottom: 0;
}
/* Active link */
.active-link{
  color: var(--first-color);
}
/* Change background header */
.scroll-header{
  box-shadow: 0 -1px 4px rgba(0, 0, 0, .15);
}
/*==================== HOME ====================*/
.home__container{
  gap: 1rem;
}
.home__content{
  grid-template-columns: .5fr 3fr;
  padding-top: 3.5rem;
  align-items: center;
}
.home__social{
  display: grid;
  grid-template-columns: max-content;
  row-gap: 1rem;
}
.home__social-icon{
  font-size: 1.25rem;
  color: var(--first-color);
}
.home__social-icon:hover{
  color: var(--first-color-alt);
}
.home__blob{
  width: 200px;
  fill: var(--first-color);
}
.home__blob-img{
  width: 170px;
}
.home__data{
  grid-column: 1/3;
}
.home__title{
  font-size: var(--big-font-size);
}
.home__subtitle{
  font-size: var(--h3-font-size);
  color: var(--text-color);
  font-weight: var(--font-medium);
  margin-bottom: var(--mb-0-75);
}
.home__description{
  margin-bottom: var(--mb-2);
}
.home__scroll{
  /* display: none; */
}
.home__scroll-button{
  color: var(--first-color);
  transition: .3s;
}
.home__scroll-button:hover{
  transform: translateY(0.25rem);
}
.home__scroll-mouse{
  font-size: 2rem;
}
.home__scroll-name{
  font-size: var(--small-font-size);
  color: var(--title-color);
  font-weight: var(--font-medium);
  margin-right: var(--mb-0-25);
}
.home__scroll-arrow{
  font-size: 1.25rem;
}
/*==================== BUTTONS ====================*/
.button{
  display: inline-block;
  background-color: var(--first-color);
  color: #fff;
  padding: 1rem;
  border-radius: .5rem;
  font-weight: var(--font-medium);
  border-color: var(--first-color);
}
.button:hover{
  background-color: var(--first-color-alt);
}
.button__icon{
  font-size: 1.25rem;
  margin-left: var(--mb-0-5);
  transition: .3s;
}
.button--white{
  background-color: #FFF;
  color: var(--first-color);
  margin-bottom: 1rem;
}
.button--white:hover{
  background-color: #FFF;
}
.button--flex{
  display: inline-flex;
  align-items: center;
}
.button--small{
  padding: .75rem 1rem;
}
.button--link{
  padding: 0;
  background-color: transparent;
  color: var(--first-color);
}
.button--link:hover{
  background-color: transparent;
  color: var(--first-color-alt);
}
/*==================== ABOUT ====================*/
.about__img{
  width: 200px;
  border-radius: .5rem;
  justify-self: center;
  align-self: center;
}
.about__description{
  text-align: center;
  margin-bottom: var(--mb-2-5);
}
.about__info{
  display: flex;
  justify-content: space-evenly;
  margin-bottom: var(--mb-2-5);
}
.about__info-title{
  font-size: var(--h2-font-size);
  font-weight: var(--font-semi-bold);
  color: var(--title-color);
}
.about__info-name{
  font-size: var(--smaller-font-size);
}
.about__info-title,
.about__info-name{
  display: block;
  text-align: center;
}
.about__buttons{
  display: flex;
  justify-content: center;
}
/*==================== SKILLS ====================*/
.skills__container{
  row-gap: 0;
}
.skills__header{
  display: flex;
  align-items: center;
  margin-bottom: var(--mb-2-5);
  cursor: pointer;
}
.skills__icon,
.skills__arrow{
  font-size: 2rem;
  color: var(--first-color);
}
.skills__icon{
  margin-right: var(--mb-0-75);
}
.skills__title{
  font-size: var(--h3-font-size);
}
.skills__subtitle{
  font-size: var(--small-font-size);
}
.skills__arrow{
  margin-left: auto;
  transition: .4s;
}
.skills__list{
  row-gap: 1.5rem;
  padding-left: 2.7rem;
}
.skills__titles{
  display: flex;
  justify-content: space-between;
  margin-bottom: var(--mb-0-5);
}
.skills__name{
  font-size: var(--normal-font-size);
  font-weight: var(--font-medium);
}
.skills__bar,
.skills__percentage{
  height: 5px;
  border-radius: .25rem;
}
.skills__bar{
  background-color: var(--first-color-lighter);
}
.skills__percentage{
  display: block;
  background-color: var(--first-color);
}
.skills__html{
  width: 90%;
}
.skills__css{
  width: 85%;
}
.skills__js{
  width: 65%;
}
.skills__ruby{
  width: 80%;
}
.skills__node{
  width: 70%;
}
.skills__firebase{
  width: 90%;
}
.skills__phyton{
  width: 50%;
}
.skills__swift{
  width: 95%;
}
.skills__kotlin{
  width: 75%;
}
.skills__android{
  width: 90%;
}
.skills__objective-c{
  width: 65%;
}
.skills__close .skills__list{
  height: 0;
  overflow: hidden;
}
.skills__open .skills__list{
  height: max-content;
  margin-bottom: var(--mb-2-5);
}
.skills__open .skills__arrow{
  transform: rotate(-180deg);
}
/*==================== QUALIFICATION ====================*/
.qualification__tabs{
  display: flex;
  justify-content: space-evenly;
  margin-bottom: var(--mb-2);
}
.qualification__button{
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);
  cursor: pointer;
}
.qualification__button:hover{
  color: var(--first-color);
}
.qualification__icon{
  font-size: 1.8rem;
  margin-right: var(--mb-0-25);
}
.qualification__data{
  display: grid;
  grid-template-columns: 1fr max-content 1fr;
  column-gap: 2rem;
  max-width: 800px;
}
.qualification__title{
  font-size: var(--normal-font-size);
}
.qualification__subtitle{
  display: inline-block;
  font-size: var(--small-font-size);
  margin-bottom: var(--mb-1);
}
.qualification__calendar{
  font-size: var(--small-font-size);
  color: var(--text-color-light);
}
.qualification__rounder{
  display: inline-block;
  width: 13px;
  height: 13px;
  background-color: var(--first-color);
  border-radius: 50%;
}
.qualification__line{
  display: block;
  width: 1px;
  height: 100%;
  background-color: var(--first-color);
  transform: translate(6px, -7px);
}
.qualification [data-content]{
  display: none;
}
.qualification__active[data-content]{
  display: block;
}
.qualification__button.qualification__active{
  color: var(--first-color);
}
/*==================== SERVICES ====================*/
.services__container{
  gap: 1.5rem;
  grid-template-columns: repeat(2, 1fr);
}
.services__content{
  position: relative;
  background-color: var(--container-color);
  padding: 3.5rem .5rem 1.25rem 1.5rem;
  border-radius: .25rem;
  box-shadow: 0 2px 4px rgba(0, 0, 0, .15);
  transition: .3s;
}
.services__content:hover{
  box-shadow: 0 4px 8px rgba(0, 0, 0, .15);
}
.services__icon{
  display: block;
  font-size: 1.5rem;
  color: var(--first-color);
  margin-bottom: var(--mb-1);
}
.service__title{
  font-size: var(--h3-font-size);
  margin-bottom: var(--mb-1);
  font-weight: var(--font-medium);
}
.services__button{
  cursor: pointer;
  font-size: var(--small-font-size);
}
.services__button:hover .button__icon{
  transform: translateX(.25rem);
}
.services__modal{
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0, 0, 0, .5);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0 1rem;
  z-index: var(--z-modal);
  opacity: 0;
  visibility: hidden;
  transition: .3s;
}
.services__modal-content{
  position: relative;
  background-color: var(--container-color);
  padding: 1.5rem;
  border-radius: .5rem;
}
.services__modal-services{
  row-gap: 1rem;
}
.services__modal-service{
  display: flex;
}
.service__modal-title{
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);
  margin-bottom: var(--mb-1-5);
}
.services__modal-close{
  position: absolute;
  top: 1rem;
  right: 1rem;
  font-size: 1.5rem;
  color: var(--first-color);
  cursor: pointer;
}
.services__modal-icon{
  color: var(--first-color);
  margin-right: var(--mb-0-25);
}
/* Active Modal */
.active-modal{
  opacity: 1;
  visibility: visible;
}
/*==================== PORTFOLIO ====================*/
.portfolio__container{
  overflow: initial;
}
.portfolio__content{
  padding: 0 1.5rem;
}
.portfolio__img{
  width: 265px;
  border-radius: .5rem;
  justify-self: center;
}
.portfolio__title{
  font-size: var(--h3-font-size);
  margin-bottom: var(--mb-0-5);
}
.portfolio__description{
  margin-bottom: var(--mb-0-75);
}

.portfolio__button{
  height: 50px;
}
.portfolio__button:hover .button__icon{
  transform: translateX(.25rem);
}
.swiper-button-prev::after,
.swiper-button-next::after{
  content: '';
}
.swiper-portfolio-icon{
  font-size: 2rem;
  color: var(--first-color);
}
.swiper-button-prev{
  left: -.5rem;
}
.swiper-buton-next{
  right: -.5rem;
}
.swiper-container-horizontal > .swiper-pagination-bullets{
  bottom: -2.5rem;
}
.swiper-pagination-bullet-active{
  background-color: var(--first-color);
}
.swiper-button-prev,
.swiper-button-next,
.swiper-pagination-bullet{
  outline: none;
}
/*==================== PROJECT IN MIND ====================*/
.project{
  text-align: center;
}
.project__bg{
  background-color: var(--first-color-second);
  padding-top: 3rem;
}
.project__title{
  font-size: var(--h2-font-size);
  margin-bottom: var(--mb-0-75);
}
.project__description{
  margin-bottom: var(--mb-1-5);
}
.project__title,
.project__description{
  color: #FFF;
}
.project__img{
  width: 232px;
  justify-self: center;
  border-radius: .5rem;
}
/*==================== TESTIMONIAL ====================*/
.testimonial__data,
.testimonial__header{
  display: flex; 
}
.testimonial__data{
  justify-content: space-between;
  margin-bottom: var(--mb-1);
}
.testimonial__img{
  width: 60px;
  height: 60px;
  border-radius: 50%;
  margin-right: var(--mb-0-75);
}
.testimonial__name{
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);
}
.testimonial__client{
  font-size: var(--small-font-size);
  color: var(--text-color-light);
}
.testimonial__description{
  margin-bottom: var(--mb-2-5);
}
.testimonial__icon-star{
  color: var(--first-color);
}
.swiper-container .swiper-pagination-testimonial{
  bottom: 0;
}
/*==================== CONTACT ME ====================*/
.contact__container{
  row-gap: 3rem;
}
.contact__information{
  display: flex;
  margin-bottom: var(--mb-2);
}
.contact__icon{
  font-size: 2rem;
  color: var(--first-color);
  margin-right: var(--mb-0-75);
}
.contact__title{
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);
}
.contact__subtitle{
  font-size: var(--small-font-size);
  color: var(--text-color-light);
}
.contact__content{
  background-color: var(--input-color);
  border-radius: .5rem;
  padding: .75rem 1rem .25rem;
}
.contact__label{
  font-size: var(--small-font-size);
  color: var(--title-color);
}
.contact__input{
  width: 100%;
  background-color: var(--input-color);
  color: var(--text-color);
  font-family: var(--body-font);
  font-size: var(--normal-font-size);
  border: none;
  outline: none;
  padding: .25rem .5rem .5rem 0;
}
/*==================== FOOTER ====================*/
.footer{
  padding-top: 2rem ;
}
.footer__container{
  row-gap: 3.5rem;
}
.footer__bg{
  background-color: var(--first-color-second);
  padding: 2rem 0 3rem;
}
.footer__title{
  font-size: var(--h1-font-size);
  margin-bottom: var(--mb-0-25);
}
.footer__subtitle{
  font-size: var(--small-font-size);
}
.footer__links{
  display: flex;
  flex-direction: column;
  row-gap: 1.5rem;
}
.footer__links:hover{
  columns: var(--first-color-lighter);
}
.footer__social{
  font-size: 1.25rem;
  margin-right: var(--mb-1-5);
}
.footer__social:hover{
  color: var(--first-color-lighter);
}
.footer__copy{
  font-size: var(--smaller-font-size);
  text-align: center;
  color: var(--text-color-light);
  margin-top: var(--mb-3);
}
.footer__title,
.footer__subtitle,
.footer__link,
.footer__social{
  color: #FFF;
}
/*========== SCROLL UP ==========*/
.scrollup{
  position: fixed;
  right: 1rem;
  bottom: -20%;
  background-color: var(--first-color);
  opacity: .8;
  padding: 0 .3rem;
  border-radius: .4rem;
  z-index: var(--z-tooltip);
  transition: .4s;
}
.scrollup:hover{
  background-color: var(--first-color-alt);
}
.scrollup__icon{
  font-size: 1.5rem;
  color: #FFF;
}
/* Show scroll */
.show-scroll{
  bottom: 5rem;
}
/*========== SCROLL BAR ==========*/
::-webkit-scrollbar{
  width: .60rem;
  background-color: var(--scroll-bar-color);
  border-radius: .5rem;
}
::-webkit-scrollbar-thumb{
  background-color: var(--scroll-thumb-color);
  border-radius:  .5rem;
}
::-webkit-slider-thumb:hover{
  background-color: var(--text-color-light);
}
/*==================== MEDIA QUERIES ====================*/
/* For small devices */
@media screen and (max-width: 350px) {
  .container{
    margin-left: var(--mb-1);
    margin-right: var(--mb-1);
  }
  .body{
    font-size: var(--smaller-font-size);
    justify-content: center;
  }
  .nav__menu{
    padding: 2rem .25rem 4rem;
  }
  .nav__list{
   column-gap: 0; 
  }
  .home__description{
    text-align: center;
  }
  .home__content{
    grid-template-columns: .25fr 3fr;
    text-align: center;
  }
  .home__blob{
    width: 180px;
  }
  .skills__title{
    font-size: var(--normal-font-size);
  }
  .qualification__data{
    gap: .5rem;
  }
  .services__container{
    grid-template-columns: max-content;
    justify-content: center;
  }
  .services__content{
    padding-right: 3.5rem;
  }
  .services__modal{
    padding: 0 .5rem;
  }
  .project__img{
    width: 200px;
  }
  .testimonial__data,
  .testimonial__header{
    flex-direction: column;
    align-items: center;
  }
  .testimonial__img{
    margin-right: 0;
    margin-bottom: var(--mb-0-25);
  }
  .testimonial__data,
  .testimonial__description{
    text-align: center;
  }
}
/* For medium devices */
@media screen and (min-width: 620px) {
  .home__content{
    grid-template-columns: max-content 1fr 1fr;
  }
  .home__data{
    grid-column: initial;
  }
  .home__img{
    order: 1;
    justify-self: center;
  }
  .about__container,
  .skills__container,
  .portfolio__content,
  .project__container,
  .contact__container,
  footer__container{
    grid-template-columns: repeat(2, 1fr);
  }
  .qualification__sections{
    display: grid;
    grid-template-columns: .6fr;
    justify-content: center;
  }
}
@media screen and (min-width: 768px) {
  .container{
    margin-left: auto;
    margin-right: auto;
  }
  body{
    margin: 0;
  }
  .section{
    padding: 6rem 0 2rem ;
  }
  .section__subtitle{
    margin-bottom: 4rem;
  }
  .header{
    top: 0;
    bottom: initial;
  }
  .header,
  .main,
  .footer__container{
    padding: 0 1rem;
  }
  .nav{
    height: calc(var(--header-height) + 1.5rem);
    column-gap: 1rem;
  }
  .nav__icon,
  .nav__close,
  .nav__toggle{
    display: none;
  }
  .nav__list{
    display: flex;
    column-gap: 2rem;
  }
  .nav__link{
    font-size: 1rem;
  }
  .nav__menu{
    margin-left: auto;
  }
  
  .change-theme{
    margin: 0;
  }
  .home__container{
    row-gap: 5rem;
  }
  .home__content{
    padding-top: 5.5rem;
    column-gap: 2rem;
  }
  .home__blob{
    width: 270px;
  }
  .home__scroll{
    display: block;
  }
  .home__scroll-button{
    margin-left: 3rem;
  }
  .about__container{
    column-gap: 5rem;
  }
  .about__img{
    width: 350px;
  }
  .about__description{
    text-align: initial;
  }
  .about__info{
    justify-content: space-between;
  }
  .about__buttons{
    justify-content: initial;
  }
  .qualification__tabs{
    justify-content: center;
  }
  .qualification__button{
    margin: var(--mb-1);
  }
  .qualification__sections{
    grid-template-columns: .5fr;
  }
  .services__container{
    grid-template-columns: repeat(3,218px);
    justify-content: center;
  }
  .services__icon{
    font-size: 2rem;
  }
  .services__content{
    padding: 6rem 0 2rem 2.5rem;
  }
  .services__modal-content{
    width: 450px;
  }
  .portfolio__img{
    width: 320px;
  }
  .portfolio__content{
    align-items: center;
  }
  .project{
    text-align: initial;
  }
  .project__bg{
    background: none;
  }
  .project__container{
    background-color: var(--first-color-second);
    border-radius: 1rem;
    padding: 3rem 2.5rem 0;
    grid-template-columns: 1fr max-content;
    column-gap: 3rem;
  }
  .project__data{
    padding-top: .8rem;
  }
  .footer__container{
    grid-template-columns: repeat(3, 1fr);
  }
  .footer__bg{
    padding: 3rem 0 3.5rem;
  }
  .footer__links{
    flex-direction: row;
    column-gap: 2rem;
  }
  .footer__socials{
    justify-self: flex-end;
  }
  .footer__copy{
    margin-top: 4.5rem;
  }
}
/* For large devices */
@media screen and (min-width: 1024px) {
  .header,
  .main,
  .footer__container{
    padding: 0;
    font-size: 1.2rem;
    text-align: center;
  }
  .home__blob{
    width: 320px;
  }
  .home__social{
    transform: translateX(-6rem);
  }
  .services__container{
    grid-template-columns: repeat(3, 250px);
    justify-content: center;
  }
  .services__title,
  .services__icon{
    text-align: left;
  }
  .portfolio__content{
    column-gap: 5rem;
  }
  .swiper-portfolio-icon{
    font-size: 3.5rem;
  }
  .swiper-button-prev{
    left: -3.5rem;
  }
  .swiper-button-next{
    right: -3.5rem;
  }
  .swiper-container-horizontal > .swiper-pagination-bullets{
    bottom: -4.5rem;
  }
  .contact__form{
    width: 460px;
  }
  .contact__inputs{
    grid-template-columns: repeat(2,1fr);
  }
}
/* Your existing styles */

body.light-theme {
    /* Styles for light theme */
    background-color: #ffffff;
    color: #000000;
}

body.dark-theme {
    /* Styles for dark theme */
    background-color: #1a1a1a;
    color: #ffffff;
}

      </style>
        <!--==================== HEADER ====================-->
        <header class="header" id="header">
            <nav class="nav container">
                <a href="#" class="nav__logo">Vanhardiansyah</a>
                <div class="nav__menu" id="nav-menu">
                    <ul class="nav__list grid">
                        <li class="nav__item">
                            <a href="#home" class="nav__link active-link">
                                <i class="uil uil-estate nav__icon"></i> Home
                            </a>
                        </li>
                        <li class="nav__item">
                            <a href="#about" class="nav__link">
                                <i class="uil uil-user nav__icon"></i>About
                            </a>
                        </li>
                        <li class="nav__item">
                            <a href="#skills" class="nav__link">
                                <i class="uil uil-file-alt nav__icon"></i>Skills
                            </a>
                        </li>
                        <li class="nav__item">
                            <a href="#services" class="nav__link">
                                <i class="uil uil-briefcase-alt nav__icon"></i>Services
                            </a>
                        </li>
                        <li class="nav__item">
                            <a href="#Mywork" class="nav__link">
                                <i class="uil uil-scenery nav__icon"></i>Mywork
                            </a>
                        </li>
                        <li class="nav__item">
                            <a href="#contact" class="nav__link">
                                <i class="uil uil-message nav__icon"></i> Contact me
                            </a>
                        </li>
                    </ul>
                    <i class="uil uil-times nav__close" id="nav-close"></i>
                </div>
                <div class="nav__btns">
                  <!-- Theme Change Button-->
                  <i class="uil uil-moon change-theme" id="theme-button"></i>
                  <div class="nav__toggle" id="nav-toggle">
                      <i class="uil uil-apps"></i>
                  </div>
                </div>
            </nav>
        </header>
        <!--==================== MAIN ====================-->
        <main class="main">
            <!--==================== HOME ====================-->
            <section class="home section" id="home">
                <div class="home__container container grid">
                    <div class="home__content grid">
                        <div class="home__social">
                            <a href="https://linkedin.com/" target="blank" class="home__social-icon">
                                <i class="uil uil-linkedin-alt"></i>
                            </a>
                            <a href="https://behance.net/" target="blank" class="home__social-icon">
                                <i class="uil uil-behance"></i>
                            </a>
                            <a href="https://github.com/" target="blank" class="home__social-icon">
                                <i class="uil uil-github-alt"></i>
                            </a>
                        </div>
                        <div class="home__img">
                            <svg class="home__blob" viewBox="0 0 200 187" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                                <mask id="mask0" mask-type="alpha">
                                    <path d="M190.312 36.4879C206.582 62.1187 201.309 102.826 182.328 134.186C163.346 165.547 
                                    130.807 187.559 100.226 186.353C69.6454 185.297 41.0228 161.023 21.7403 129.362C2.45775 
                                    97.8511 -7.48481 59.1033 6.67581 34.5279C20.9871 10.1032 59.7028 -0.149132 97.9666 
                                    0.00163737C136.23 0.303176 174.193 10.857 190.312 36.4879Z"/>
                                </mask>
                                <g mask="url(#mask0)">
                                    <path d="M190.312 36.4879C206.582 62.1187 201.309 102.826 182.328 134.186C163.346 
                                    165.547 130.807 187.559 100.226 186.353C69.6454 185.297 41.0228 161.023 21.7403 
                                    129.362C2.45775 97.8511 -7.48481 59.1033 6.67581 34.5279C20.9871 10.1032 59.7028 
                                    -0.149132 97.9666 0.00163737C136.23 0.303176 174.193 10.857 190.312 36.4879Z"/>
                                   <!--====Img Profile== UNCOMMENT AND ADD IMG -->
                                    <image class="home__blob-img" x='12' y='18' xlink:href="assets/img/perfil2.png"/>
                                </g>
                            </svg>
                        </div>

                        <div class="home__data">
                            <h1 class="home__title">Hi, I'm Ivan</h1>
                            <h3 class="home__subtitle">Full-Stack Developer</h3>
                            <p class="home__description">I am a beginner programmer, I am a bit rough. I am still in grade 11 of vocational school and I am majoring in SOFTWARE ENGINEERING. I am from Indonesia, Makassar, South Sulawesi. I became interested in coding when I was in grade 11 and that made me enthusiastic about learning. And not only that, I am also studying UI/UX Design. I hope that my portfolio can make me more enthusiastic about learning more..</p>
                            <a href="#contact" class="button button--flex">
                                Contact Me <i class="uil uil-message button__icon"></i>
                            </a>
                        </div>
                        
                    </div>
                    <!--==== Scroll Button
                    <div class="home__scroll">
                        <a href="#about" class="home__scroll-button button--flex">
                            <i class="uil uil-mouse-alt home__scroll-mouse"></i>
                            <span class="home__scroll-name">Scroll down</span>
                            <i class="uil uil-arrow-down home__scroll-arrow"></i>
                        </a>
                    </div>
                        -->
                </div>
                
            </section>
            <!--==================== ABOUT ====================-->
            <section class="about section" id="about">
                <h2 class="section__title"> About Me</h2>
                <span class="section__subtitle">My introduction</span>
                
                <div class="about__container container grid">
                    <img src="assets/img/about2.jpg" alt="" class="about__img">
                    <div class="about__data">
                        <p class="about__description">I focus on highly customizable, fast and optimized websites and mobile applications, 
                            clean lines, white space, and solid colors to create an aesthetic that is both modern and timeless. The websites are professionally
                             designed to increase conversion rates and sales. I can build a great E-commerce user friendly.</p>
                        <div class="about__info">
                            <div>
                                <span class="about__info-title">08+</span>
                                <span class="about__info-name">Years <br> experience</span>
                            </div>
                            <div>
                                <span class="about__info-title">20+</span>
                                <span class="about__info-name">Completed <br> projects</span>
                            </div>
                            <div>
                                <span class="about__info-title">05+</span>
                                <span class="about__info-name">Companies <br> worked</span>
                            </div>
                        </div>
                        <div class="about__buttons">
                            <a download="" href="assets/pdf/Andres-CV.pdf" class="button button--flex">
                                Download CV <i class="uil uil-download-alt button__icon"></i>
                            </a>
                        </div>
                    </div>
                </div>
            </section>
            <!--==================== SKILLS ====================-->
            <section class="skills section" id="skills">
                <h2 class="section__title">Skills</h2>
                <span class="section__subtitle ">My Technical level</span>
                <div class="skills__container container grid">
                    <div>
                         <!--==================== SKILLS 1 ====================-->
                         <div class="skills__content skills__open">
                            <div class="skills__header">
                                <i class="uil uil-brackets-curly skills__icon"></i>
                                <div>
                                    <h1 class="skills__title">Frontend Developer</h1>
                                    <span class="skills__subtitle">More than 7 years</span>
                                </div>
                                <i class="uil uil-angle-down skills__arrow"></i>
                            </div>
                            <div class="skills__list grid">
                                <div class="skills__data">
                                    <div class="skills__titles">
                                        <h3 class="skills__name">HTML</h3>
                                        <span class="skills__number">90%</span>
                                    </div>
                                    <div class="skills__bar">
                                        <span class="skills__percentage skills__html"></span>
                                    </div>
                                </div>
                                <div class="skills__data">
                                    <div class="skills__titles">
                                        <h3 class="skills__name">CSS</h3>
                                        <span class="skills__number">85%</span>
                                    </div>
                                    <div class="skills__bar">
                                        <span class="skills__percentage skills__css"></span>
                                    </div>
                                </div>
                                <div class="skills__data">
                                    <div class="skills__titles">
                                        <h3 class="skills__name">js</h3>
                                        <span class="skills__number">65%</span>
                                    </div>
                                    <div class="skills__bar">
                                        <span class="skills__percentage skills__js"></span>
                                    </div>
                                </div>
                                <div class="skills__data">
                                    <div class="skills__titles">
                                        <h3 class="skills__name">UI/UX</h3>
                                        <span class="skills__number">100%</span>
                                    </div>
                                    <div class="skills__bar">
                                        <span class="skills__percentage skills__react"></span>
                                    </div>
                                </div>
                            </div>
                         </div>
                        <!--==================== SKILLS 2 ====================-->
                         <div class="skills__content skills__close">
                            <div class="skills__header">
                                <i class="uil uil-server-network skills__icon"></i>
                                <div>
                                    <h1 class="skills__title">Backend Developer</h1>
                                    <span class="skills__subtitle">More than 4 years</span>
                                </div>
                                <i class="uil uil-angle-down skills__arrow"></i>
                            </div>
                            <div class="skills__list grid">
                                <div class="skills__data">
                                    <div class="skills__titles">
                                        <h3 class="skills__name">Ruby on Rails</h3>
                                        <span class="skills__number">80%</span>
                                    </div>
                                    <div class="skills__bar">
                                        <span class="skills__percentage skills__ruby"></span>
                                    </div>
                                </div>
                                <div class="skills__data">
                                    <div class="skills__titles">
                                        <h3 class="skills__name">Node Js</h3>
                                        <span class="skills__number">70%</span>
                                    </div>
                                    <div class="skills__bar">
                                        <span class="skills__percentage skills__node"></span>
                                    </div>
                                </div>
                                <div class="skills__data">
                                    <div class="skills__titles">
                                        <h3 class="skills__name">Firebase</h3>
                                        <span class="skills__number">90%</span>
                                    </div>
                                    <div class="skills__bar">
                                        <span class="skills__percentage skills__firebase"></span>
                                    </div>
                                </div>
                                <div class="skills__data">
                                    <div class="skills__titles">
                                        <h3 class="skills__name">Phyton</h3>
                                        <span class="skills__number">50%</span>
                                    </div>
                                    <div class="skills__bar">
                                        <span class="skills__percentage skills__phyton"></span>
                                    </div>
                                </div>
                            </div>
                         </div>
                    </div>
                    <div>
                         <!--==================== SKILLS 3 ====================-->
                         <div class="skills__content skills__close">
                            <div class="skills__header">
                             
                            
                                <i class="uil uil-angle-down skills__arrow"></i>
                            </div>
                            <div class="skills__list grid">
                                <div class="skills__data">
                                    <div class="skills__titles">
                                        <h3 class="skills__name">Swift</h3>
                                        <span class="skills__number">95%</span>
                                    </div>
                                    <div class="skills__bar">
                                        <span class="skills__percentage skills__swift"></span>
                                    </div>
                                </div>
                                <div class="skills__data">
                                    <div class="skills__titles">
                                        <h3 class="skills__name">Kotlin</h3>
                                        <span class="skills__number">75%</span>
                                    </div>
                                    <div class="skills__bar">
                                        <span class="skills__percentage skills__kotlin"></span>
                                    </div>
                                </div>
                                <div class="skills__data">
                                    <div class="skills__titles">
                                        <h3 class="skills__name">Android</h3>
                                        <span class="skills__number">95%</span>
                                    </div>
                                    <div class="skills__bar">
                                        <span class="skills__percentage skills__android"></span>
                                    </div>
                                </div>
                                <div class="skills__data">
                                    <div class="skills__titles">
                                        <h3 class="skills__name">Objective-C</h3>
                                        <span class="skills__number">65%</span>
                                    </div>
                                    <div class="skills__bar">
                                        <span class="skills__percentage skills__objective-c"></span>
                                    </div>
                                </div>
                            </div>
                         </div>
                    </div>
                </div>
            </section>
           
            <!--==================== SERVICES ====================-->
            <section class="services section" id="services">
                <h2 class="section__title">Services</h2>
                <span class="section__subtitle"> What i offer</span>
                <div class="services__container container grid">
                    <!--==================== SERVICES 1 ====================-->
                    <div class="services__content">
                        <div>
                            <i class="uil uil-web-grid services__icon"></i>
                            <h3 class="services__title">Ui/Ux <br> Designer</h3>
                        </div>
                        <span class="button button--flex button--small button--link services__button">
                            View more
                            <i class="uil uil-arrow-right button__icon"></i>
                        </span>
                        <div class="services__modal">
                            <div class="services__modal-content">
                                <h4 class="services__modal-title">Ui/Ux <br> Designer</h4>
                                <i class="uil uil-times services__modal-close"></i>
                                <ul class="services__modal-services grid">
                                    <li class="services__modal-service">
                                        <i class="uil uil-check-circle services__modal-icon"></i>
                                        <p> i develop the user inferface.</p>
                                    </li>
                                    <li class="services__modal-service">
                                        <i class="uil uil-check-circle services__modal-icon"></i>
                                        <p> Web page development.</p>
                                    </li>
                                    <li class="services__modal-service">
                                        <i class="uil uil-check-circle services__modal-icon"></i>
                                        <p> I create ux element interaction.</p>
                                    </li>
                                    <li class="services__modal-service">
                                        <i class="uil uil-check-circle services__modal-icon"></i>
                                        <p> I position your company brand.</p>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                    <!--==================== SERVICES 2 ====================-->
                    <div class="services__content">
                        <div>
                            <i class="uil uil-arrow services__icon"></i>
                            <h3 class="services__title">Frontend <br> Developer</h3>
                        </div>
                        <span class="button button--flex button--small button--link services__button">
                            View more
                            <i class="uil uil-arrow-right button__icon"></i>
                        </span>
                        <div class="services__modal">
                            <div class="services__modal-content">
                                <h4 class="services__modal-title">Ui/Ux <br> Designer</h4>
                                <i class="uil uil-times services__modal-close"></i>
                                <ul class="services__modal-services grid">
                                    <li class="services__modal-service">
                                        <i class="uil uil-check-circle services__modal-icon"></i>
                                        <p> i develop the user inferface.</p>
                                    </li>
                                    <li class="services__modal-service">
                                        <i class="uil uil-check-circle services__modal-icon"></i>
                                        <p> Web page development.</p>
                                    </li>
                                    <li class="services__modal-service">
                                        <i class="uil uil-check-circle services__modal-icon"></i>
                                        <p> I create ux element interaction.</p>
                                    </li>
                                    <li class="services__modal-service">
                                        <i class="uil uil-check-circle services__modal-icon"></i>
                                        <p> I position your company brand.</p>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                     <!--==================== SERVICES 3 ====================-->
                  
                        <div class="services__modal">
                            <div class="services__modal-content">
                                <h4 class="services__modal-title">Ui/Ux <br> Designer</h4>
                                <i class="uil uil-times services__modal-close"></i>
                                <ul class="services__modal-services grid">
                                    <li class="services__modal-service">
                                        <i class="uil uil-check-circle services__modal-icon"></i>
                                        <p> i develop the user inferface.</p>
                                    </li>
                                    <li class="services__modal-service">
                                        <i class="uil uil-check-circle services__modal-icon"></i>
                                        <p> Web page development.</p>
                                    </li>
                                    <li class="services__modal-service">
                                        <i class="uil uil-check-circle services__modal-icon"></i>
                                        <p> I create ux element interaction.</p>
                                    </li>
                                    <li class="services__modal-service">
                                        <i class="uil uil-check-circle services__modal-icon"></i>
                                        <p> I position your company brand.</p>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
            <!--==================== My work ====================-->
            <section class="Mywork section" id="Mywork">
              <h2 class="section__title">the results of my work</h2>
              <img src="van.png" alt="" width="390" height="410">
              <img src="image_processing20200702-18021-jnbiql.jpg" alt="" width="390" height="410">
              <!-- Change the values of width and height according to your requirements -->
              <h5></h5>
              <!-- Add Pagination-->
              <div class="swiper-pagination"></div>
          </section>
          
            <!--==================== PROJECT IN MIND ====================-->
            <section class="project section">
                <div class="project
                    <div class="project__container container grid">
                        <div class="project__data">
                            <h2 class="project__title">You have a new project</h2>
                            <p class="project__description">Contact me now to get a discount on your new project</p>
                            <a href="#contact" class="button button--flex button--white">
                                Contact Me
                                <i class="uil uil-message project__icon button__icon"></i>
                            </a>
                        </div>
                        <img src="assets/img/project3.jpg" alt="" class="project__img">
                </div>           
                    </div>
                </div>
            </section>
          
                                    
                            
                            
            </section>
            <!--==================== CONTACT ME ====================-->
            <section class="contact section" id="contact">
                <h2 class="section__title">Contact Me</h2>
                <span class="section__subtitle">Get in touch</span>
                <div class="contact__container container grid">
                    <div>
                        <div class="contact__information">
                            <i class="uil uil-phone contact__icon"></i>
                            <div>
                                <h3 class="contact__title">Call Me</h3>
                                <span class="contact__subtitle">081524376933</span>
                            </div>
                        </div>
                        <div class="contact__information">
                            <i class="uil uil-envelope contact__icon"></i>
                            <div>
                                <h3 class="contact__title">Email</h3>
                                <span class="contact__subtitle">mivanhardiansyah.com</span>
                            </div>
                        </div>
                        <div class="contact__information">
                            <i class="uil uil-map-marker contact__icon"></i>
                            <div>
                                <h3 class="contact__title">Location</h3>
                                <span class="contact__subtitle">Makassar,Sulawesi Selatan </span>
                            </div>
                        </div>
                    </div>
                    <form class="contact__form grid">
                        <div class="contact__inputs grid">
                            <div class="contact__content">
                                <label for="" class="contact__label">Name</label>
                                <input type="text" class="contact__input">
                            </div>
                            <div class="contact__content">
                                <label for="" class="contact__label">Email</label>
                                <input type="email" class="contact__input">
                            </div>
                        </div>
                        <div class="contact__content">
                            <label for="" class="contact__label">Project</label>
                            <input type="text" class="contact__input">
                        </div>
                        <div class="contact__content">
                            <label for="" class="contact__label">Message</label>
                            <textarea name="" id="" cols="0" rows="7" class="contact__input"></textarea>
                        </div>
                            <button class="button button--flex">
                                Send Message
                                <i class="uil uil-message button__icon"></i>
                            </button>
                       <!-- FORM SEND EMAIL
                        <div>
                            <a href="#" class="button button--flex">
                                Send Message
                                <i class="uil uil-message button__icon"></i>
                            </a>
                        </div>
                        -->
                    </form>
                </div> 
            </section>
        </main>
        <!--==================== FOOTER ====================-->
        <footer class="footer">
            <div class="footer__bg">
                <div class="footer__container container grid">
                    <div>
                        <h1 class="footer__title">Ivan</h1>
                        <span class="footer__subtitle">Full-Stack Developer</span>
                    </div>
                    <ul class="footer__links">
                        <li>
                            <a href="#services" class="footer__link">Services</a>
                        </li>
                        <li>
                            <a href="#Mywork" class="footer__link">My work</a>
                        </li>
                        <li>
                            <a href="#contact" class="footer__link">Contact Me</a>
                        </li>
                    </ul>
                    <div class="footer__socials">
                        <a href="081524376933" target="_blank" class="footer__social">
                            <i class="uil uil-whatsapp-alt"></i>
                        </a>
                        <a href="https://www.instagram.com/uiux.v4n/" target="_blank" class="footer__social">
                            <i class="uil uil-instagram" width="390" height="410"></i>
                        </a>
                        
                    </div>
                </div>
                <p class="footer__copy">&#169; Ivan hardiansyah, All right reserved</p>
            </div>
        </footer>
        
        <!--==================== SCROLL TOP ====================-->
        
        <a href="#" class="scrollup" id="scroll-up">
            <i class="uil uil-arrow-up scrollup__icon"></i>
        </a>
        <!--==================== SWIPER JS ====================-->
        <script src="assets/js/swiper-bundle.min.js"></script>
        <!--==================== MAIN JS ====================-->
        <script src="assets/js/main.js"></script>
        
        <!--==================== SEND MAILS SMTPJS ====================-->
        <script src="https://smtpjs.com/v3/smtp.js"></script>
    </body>
    <script>
      document.addEventListener('DOMContentLoaded', function () {
    const themeButton = document.getElementById('theme-button');
    const body = document.body;

    themeButton.addEventListener('click', function () {
        // Toggle between light and dark themes
        body.classList.toggle('dark-theme');

        // Save the user's preference in localStorage
        const isDarkTheme = body.classList.contains('dark-theme');
        localStorage.setItem('dark-theme', isDarkTheme);
    });

    // Check the user's preference from localStorage
    const isDarkTheme = localStorage.getItem('dark-theme') === 'true';
    if (isDarkTheme) {
        body.classList.add('dark-theme');
    }
});

    </script>
</html>
