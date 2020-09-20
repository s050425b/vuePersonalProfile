<template>
  <div id="app">
    <First />
    <Second />
  </div>
</template>

<script>

import First from './components/Try'
import Second from './components/Second'

export default {
  name: 'App',
  components: {
    First,
    Second
  }
}
</script>

<style>
  @font-face {
    font-family: 'Lato';
    font-style: normal;
    font-weight: 700;
    font-display: swap;
    src: local('Lato Bold'), local('Lato-Bold'), url(https://fonts.gstatic.com/s/lato/v16/S6u9w4BMUTPHh6UVSwiPGQ3q5d0.woff2) format('woff2');
    unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
  }

  @font-face {
    font-family: 'Lato';
    font-style: normal;
    font-weight: 400;
    font-display: swap;
    src: local('Lato Regular'), local('Lato-Regular'), url(https://fonts.gstatic.com/s/lato/v16/S6uyw4BMUTPHjx4wXiWtFCc.woff2) format('woff2');
    unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
  }


    html, body, div, span, applet, object, iframe,
  h1, h2, h3, h4, h5, h6, p, blockquote, pre,
  a, abbr, acronym, address, big, cite, code,
  del, dfn, em, img, ins, kbd, q, s, samp,
  small, strike, strong, sub, sup, tt, var,
  b, u, i, center,
  dl, dt, dd, ol, ul, li,
  fieldset, form, label, legend,
  table, caption, tbody, tfoot, thead, tr, th, td,
  article, aside, canvas, details, embed, 
  figure, figcaption, footer, header, hgroup, 
  menu, nav, output, ruby, section, summary,
  time, mark, audio, video {
      margin: 0;
      padding: 0;
      border: 0;
      font-size: 100%;
      font: inherit;
      vertical-align: baseline;
  }
  /* HTML5 display-role reset for older browsers */
  article, aside, details, figcaption, figure, 
  footer, header, hgroup, menu, nav, section {
      display: block;
  }
  body {
      line-height: 1;
  }
  
  blockquote, q {
      quotes: none;
  }
  blockquote:before, blockquote:after,
  q:before, q:after {
      content: '';
      content: none;
  }
  table {
      border-collapse: collapse;
      border-spacing: 0;
  }

  @media only screen and (max-width: 870px){

    #top-title h2{
        font-size:40px;
        
    }

    #flex{
        flex-direction: column;
    }

    #top #topRight #top-know{
        position: initial;
    }

    #topRight #top-info h2{
        font-size: 20px;
    }



    .info span{
        font-size:20px;
    }

    #topLeft{
        display:none;
    }

    #topRight{
        position: initial;
        width:100%;
    }

    .project{
        flex-direction: column;
    }

    .image{
        width:100%;
    }

    .description{
        width:100%;
        margin-top:8%;
    }

    .description span{
        text-align: center;
    }

    .description ul li{
        line-height: 30px;
        margin-top: 5%;
    }

    #project2-img{
        margin: 5% auto;
    }

    #project2-img img{
        width:100%;
    }
}
</style>
