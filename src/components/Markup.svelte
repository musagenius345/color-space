<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta http-equiv="X-UA-Compatible" content="ie=edge" />
  <link rel="stylesheet" href="dist/css/main.min.css" />
  <title>Musa Badru | Portfolio</title>
</head>

<body>
  <nav class="flex">
    <div class="logo__container">
      <!-- <h2 role="title">blackfrost</h2> -->
      <img src="assets/img/default-monochrome.svg" alt="Logo" class="logo">
    </div>
    <div class="menu"><img src="assets/img/menu.svg" alt=""></div>
    <ul class="flex nav-list">
      <li><a href="#bottom" aria-label="Home section">Home</a></li>
      <li>
        <a href="#experience" aria-label="Experience section">Experience</a>
      </li>
      <li><a href="#projects" aria-label="Projects section">Projects</a></li>
      <li><a href="#contact" aria-label="Contact section">Contact</a></li>
      <li><a href="#blog" aria-label="Blog section">Blog</a></li>
    </ul>
  </nav>

  <div class="u-container">
    <header class="hero u-grid" id="hero">


      <div class="bio">
        <h1>Hi! my name is Musa Badru Blackfrost</h1>
        <p>Experienced web developer with expertise in HTML, CSS, and JavaScript. Skilled in creating custom websites
          with enhance functionality, with the aim of delivering high-quality web solutions for diverse clients.</p>
        <button type="reset" href="#about" class="btn">More about me</button>
      </div>
    </header>

    <article id="about" class="about u-grid">
      <div class="personal-info">
        <h2>Personal Information</h2>
        <p><strong>First Name:</strong> Samuel</p>
        <p><strong>Freelance:</strong> Available</p>
        <p><strong>Email:</strong> samuel@example.com</p>
        <p><strong>Languages:</strong> English, Arabic, German, Kiswahili</p>
        <p><strong>Phone:</strong> +1 (555) 123-4567</p>
        <button><a href="/assets/docs/cv.pdf" download><img class="icon" src="assets/svg/file.svg"></img>
            <p>Download CV</p>
          </a></button>
      </div>


      <section class="stats">
        <div class="stats__tab loader ">
          <h4><sup class="stats__info">24</sup>HOURS</h4>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quaerat amet eaque fuga voluptas eos blanditiis
            atque.</p>
        </div>
        <div class="stats__tab loader">
          <h4><sup class="stats__info">365</sup>DAYS</h4>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quaerat amet eaque fuga voluptas eos blanditiis
            atque.</p>
        </div>
        <div class="stats__tab loader">
          <h4><sup class="stats__info">52</sup>WEEKS</h4>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quaerat amet eaque fuga voluptas eos blanditiis
            atque.</p>
        </div>
        <div class="stats__tab loader">
          <h4><sup class="stats__info">12</sup>months</h4>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quaerat amet eaque fuga voluptas eos blanditiis
            atque.</p>
        </div>
      </section>


    </article>

    <div class="experience__container u-grid">
      <h2>Experience and Education</h2>
      <!-- column-count of 2 here -->

      <div>
        <p class="duration">2010-2014</p>
        <h3>High School</h3>
        <p>Description of high school education</p>
      </div>
      <div>
        <p class="duration">2014-2018</p>
        <h3>Engineering at Oxford University</h3>
        <p>Description of engineering studies at Oxford University</p>
      </div>
      <div>
        <p class="duration">2018-2020</p>
        <h3>Designer at Adobe</h3>
        <p>Description of work as a designer at Adobe</p>
      </div>
      <div>
        <p class="duration">2020-2022</p>
        <h3>Consultant at YouTube</h3>
        <p>Description of work as a consultant at YouTube</p>
      </div>
      <div>
        <p class="duration">2022-2025</p>
        <h3>Senior Developer at Meta</h3>
        <p>Description of work as a senior developer at Meta</p>
      </div>
    </div>


    <section class="skill__section">
      <h2>Skills</h2>
      <div class="skill__container">
        <h4 class="skill">HTML</h4>
        <p class="skill__percentage">30%</p>
      </div>
      <div class="skill__container">
        <h4 class="skill">CSS</h4>
        <p class="skill__percentage">40%</p>
      </div>
      <div class="skill__container">
        <h4 class="skill">JavaScript</h4>
        <p class="skill__percentage">10%</p>
      </div>
      <div class="skill__container">
        <h4 class="skill">Sass</h4>
        <p class="skill__percentage"></p>
      </div>
      <div class="skill__container">
        <h4 class="skill">Bootstrap</h4>
        <p class="skill__percentage">20%</p>
      </div>
      <div class="skill__container">
        <h4 class="skill">React</h4>
        <p class="skill__percentage">55%</p>
      </div>
      <div class="skill__container">
        <h4 class="skill">Svelte</h4>
        <p class="skill__percentage">70%</p>
      </div>
      <div class="skill__container">
        <h4 class="skill">Python</h4>
        <p class="skill__percentage">86%</p>
      </div>
    </section>


    <section id="contact" class="contact">
      <h2 class="capitalize">Get in Touch</h2>
      <div class="contact__wrapper">
        <article class="author__detail">
          <h3 auto-capitalize>Don't be shy</h3>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ut exercitationem, dolore impedit incidunt sit
            earum nemo, sint pariatur nostrum consequatur reprehenderit labore animi culpa facere commodi molestiae,
            amet omnis officia. Vitae ipsam, nobis sequi.</p>
          <address class="address author__detail__info">
            <div class="author__address">
              <p class="author__heading capitalize">Address Point</p>
              <a href="Paris, Ohio" role="location">Paris, Ohio</a>
            </div>


            <div class="author__email">
              <p class="author__heading capitalize">Mail Me</p>
              <a href="mailto:johndoe@gmail.com">johndoe@gmail.com</a>
            </div>

            <div class="author__phone">
              <p class="author__heading capitalize">Call Me</p>
              <a href="tel:+12345678903">+12345678903</a>
            </div>
          </address>



        </article>

        <article class="contact__container">
          <form action="" class="contact__form">
            <fieldset>
              <input type="text" placeholder="your name" class="capitalize">
              <input type="email" placeholder="Email" class="capitalize">
              <input type="text" placeholder="Subject" class="capitalize">

            </fieldset>
            <textarea type="text" placeholder="Your Message" class="capitalize" id="textarea"></textarea>
            <div class="terms__wrapper">
              <input type="checkbox" name="TOC" id="" class="terms__agree" required><span class="terms__txt">I have read
                and agree to the the <a href="#TOC">Terms and Conditions</a></span>
            </div>

            <div class="terms__wrapper">
              <input type="checkbox" name="TOC" id="" class="terms__agree"><span class="terms__txt">I agree to sign up
                for the Weekly newsletter</span>

            </div>
          </form>

          <button class="capitalize">Send Message</button>
        </article>
      </div>
    </section>


    <section id="blog" class="blog">
      <h2>Blog</h2>
      <article>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatum est adipisci voluptatibus
        praesentium, aliquam quia culpa quasi reiciendis quidem possimus cupiditate consectetur voluptate distinctio,
        nisi, nobis amet. Obcaecati accusamus, quasi eligendi voluptatem pariatur tenetur eum quos officiis autem
        eveniet ex doloribus expedita suscipit molestiae amet temporibus perferendis nihil, fugit repudiandae nam quis.
        Similique consequuntur culpa expedita, incidunt est soluta, reiciendis ex, dolores deleniti dolore ipsam!
      </article>
      <article>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sed ratione dignissimos, veritatis, culpa minus
        accusantium cupiditate repellat cumque non dolor suscipit vero quo rem aliquam facilis adipisci facere hic
        laborum debitis, repudiandae, eaque! Assumenda, dolorem facere accusamus quae! Cupiditate explicabo temporibus
        incidunt, dolor laboriosam iste recusandae perspiciatis qui, placeat ea assumenda dolore vero pariatur saepe,
        quidem provident, voluptatum eum sequi.</article>
      <article>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Tempora nostrum mollitia eos eveniet rerum dolores
        esse totam incidunt omnis qui, consequuntur facilis iure quaerat. Accusantium deserunt nobis odit ad, cumque
        fugit facilis explicabo distinctio laborum quae officiis ullam consectetur dignissimos qui eius! Porro
        voluptatum, illum quo ratione corporis ad, perferendis, adipisci alias vero quos sequi vitae itaque labore
        excepturi quod suscipit aliquid expedita eaque. Commodi quas debitis placeat, assumenda explicabo, vitae itaque
        dignissimos totam perspiciatis, ipsum nulla, dolores harum corporis.
      </article>
      <article>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Veritatis pariatur aliquam libero neque autem,
        minus ab facilis, accusamus error modi adipisci magnam, earum molestiae quo dignissimos mollitia! In vero,
        asperiores possimus! Ea dolor libero delectus eaque quas natus quasi et quisquam totam voluptatem molestiae
        velit assumenda odio, repudiandae amet, dignissimos aperiam nesciunt! Qui sequi obcaecati reprehenderit
        molestiae id possimus dolorem ab, voluptatem voluptas temporibus in totam tempore, eius ipsa a doloribus
        consequuntur! Sapiente necessitatibus inventore tempore amet est accusamus illo rem eos quo iusto quas ducimus
        nemo, consequuntur nesciunt, cum perferendis officia rerum aliquid voluptatum dolor, velit? Cumque saepe fugit
        optio, error alias rerum, repellat illo, repellendus sint assumenda odio doloribus. Recusandae rerum cumque
        mollitia rem libero, dolorum praesentium sed.</article>
      <article>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ullam, labore saepe accusantium quis autem
        voluptatem, praesentium aut nobis dolorem nostrum et soluta tempora recusandae beatae magni! Aperiam itaque
        quisquam autem dolorem, tenetur ullam tempora, voluptate perspiciatis quis reprehenderit consequuntur
        repellendus nulla architecto, saepe enim impedit! Esse, commodi ab eaque, non vel ipsam! Suscipit rerum quisquam
        eos, architecto iure dolores consequatur in culpa aliquid ex ullam quod assumenda repellat sed itaque
        perspiciatis. Suscipit excepturi, corporis deleniti quidem rem temporibus quibusdam esse similique recusandae,
        explicabo, maiores odit ad minima. Pariatur.</article>

    </section>
    <section id="bottom"></section>

  </div>
  <footer class="footer">
    <p>Copyright &copy; 2023 John Doe</p>
  </footer>
  <script type="module" src="src/js/index.js"></script>
</body>

</html>
