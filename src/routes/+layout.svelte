<script>
 import NavBar from "../components/NavBar.svelte";

</script>

<head>
  <title>Blog</title>
  <link rel="stylesheet" href="../style.css">
  <!-- <link rel="stylesheet" href="../normalize.css"> -->
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
</head>

<body>
  <NavBar></NavBar>
  <div class="spacing">

 <slot>hello</slot> 
  </div>
</body>
<style>
  /* Box sizing rules */
*,
*::before,
*::after {
  box-sizing: border-box;
}

@font-face {
	font-family: 'Mulish';
	src: url('/static/fonts/Mulish-VariableFont_wght.ttf');
	src: url('/static/fonts/Mulish-VariableFont_wght.ttf.eot?#iefix') format('embedded-opentype'),
		 url('/static/fonts/Mulish-VariableFont_wght.ttf.woff') format('woff'),
		 url('/static/fonts/Mulish-VariableFont_wght.ttf.ttf') format('truetype'),
		 url('/static/fonts/Mulish-VariableFont_wght.ttf.svg#Mulish') format('svg');
	font-style: normal;
	font-weight: normal;
	font-display: swap;
}


/* Remove default margin */
body,
h1,
h2,
h3,
h4,
p,
figure,
blockquote,
dl,
dd {
  margin: 0;
}

/* Remove list styles on ul, ol elements with a list role, which suggests default styling will be removed */
ul[role="list"],
ol[role="list"] {
  list-style: none;
}

/* Set core root defaults */
html:focus-within {
  scroll-behavior: smooth;
}

/* Set core body defaults */
body {
  font-family: 'Mulish', Arial, sans-serif;
  min-height: 100vh;
  font-size: clamp(1rem, calc(1.25rem + 0.9vw), 1.46rem);
  text-rendering: optimizeSpeed;
  line-height: 1.5;
}
dt,dd{
    all: unset;
  }
/* A elements that don't have a class get default styles */
a:not([class]) {
  text-decoration-skip-ink: auto;
}

/* Make images easier to work with */
img,
picture {
  max-width: 100%;
  display: block;
}

/* Inherit fonts for inputs and buttons */
input,
button,
textarea,
select {
  font: inherit;
}

/* Remove all animations and transitions for people that prefer not to see them */
@media (prefers-reduced-motion: reduce) {
  html:focus-within {
   scroll-behavior: auto;
  }
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}

.spacing{
    padding-inline: min(1.3em, 1.5rem);
  }
@media (min-width: 500px){
    .spacing  {
      padding-inline: 4.2rem;
    }
  }

  </style>
