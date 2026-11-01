# Designer-Website
First big project on VS Code/Github


Project Overview:
Designer-Antoni Gaudi
style-Modernisme
Purpose of website-To show and highlight Gaudi's best works and asthetical styles.

6 Design Choices:
1.) Navbar buttons with a non-polygon border that highlight when hovered.
    effect- Represents Gaudi's use of non-polygonical styles and shapes.

2.)Typography & Font choices:
    effect-Gives a more historical feel to the viewer, who might feel as if they are connected to the 19th century timeframe.

3.)Background image:
    effect: Evokes a sense of Catalan Modernisme as it is a representation of Gaudi's artistic styles.

4.)Biography section layout:
    effect: To give an underlying representation of Gaudi's curved line pattern.

5.) 3 column grid(style section):
    effect: Makes it easy for the viewer to look and read the information. Also looks very appealing and asthetical.

6.) Carousel on Info section:
    effect: Shows the viewer some of Gaudi's architecture and gives them a very basic understanding of his works.

AI Assistance:
Website was made using the help of predominantly Claude and Gemini.
Claude was used to make my ideas for the structure come to life. Gemini was used to write the Information needed.

AI Evidence:
Original prompt: my idea is that maybe if we had an image on the left side, then have text underneath so say about early life. Then diagnoally bottomed right from it on the right side we should have career with a picture and then text underneath it since I believe that I can kind of represent Gaudi's nonlinear style

Result provided: Your diagonal idea works well for Gaudí. A staggered zigzag layout breaks the usual straight rows, and you can name it as a design principle in your README (asymmetrical balance or movement). I’d shape the images with the same leaf-like corners as your navbar tiles so the two match.

HTML

Replace your current Biography section with this:

html
<section id="biography">
  <div class="container my-5 content-wrapper p-4 rounded shadow-sm">
    <h2 class="mb-4">Biography</h2>

    <div class="row">

      <!-- Early life: left, higher -->
      <div class="col-lg-5 bio-block bio-left">
        <figure class="bio-figure">
          <img src="img/gaudi-early-life.jpg"
               alt="Describe the image, e.g. a young Antoni Gaudí in a formal portrait"
               class="bio-img" width="600" height="450">
          <figcaption>Photo credit: add source and license here</figcaption>
        </figure>
        <h3 class="h4">Early Life</h3>
        <p>Write your early life text here: birth, family, and education.</p>
      </div>

      <!-- Career: right, lower -->
      <div class="col-lg-5 offset-lg-2 bio-block bio-right">
        <figure class="bio-figure">
          <img src="img/gaudi-career.jpg"
               alt="Describe the image, e.g. the Sagrada Família towers against the sky"
               class="bio-img" width="600" height="450">
          <figcaption>Photo credit: add source and license here</figcaption>
        </figure>
        <h3 class="h4">Career</h3>
        <p>Write your career text here: major projects and dates.</p>
      </div>

    </div>
  </div>
</section>
CSS
css
.bio-figure {
    margin: 0 0 1rem;
}

.bio-img {
    width: 100%;
    aspect-ratio: 4 / 3;
    object-fit: cover;
    border: 2px solid #e6c260;
    box-shadow: 0 6px 18px rgba(0, 0, 0, 0.5);
}

/* leaf-shaped corners, mirrored on the right block, echoing the navbar */
.bio-left .bio-img  { border-radius: 70px 12px 70px 12px; }
.bio-right .bio-img { border-radius: 12px 70px 12px 70px; }

.bio-figure figcaption {
    font-size: 0.8rem;
    color: #cfc8b8;
    margin-top: 0.4rem;
}

.bio-block h3 {
    color: #e6c260;
    font-family: 'Playfair Display', Georgia, serif;
}

/* desktop: push the right block down for the diagonal */
@media (min-width: 992px) {
    .bio-right {
        margin-top: 8rem;
    }
}

/* phones: stack, but keep a hint of the diagonal by shifting each block sideways */
@media (max-width: 991.98px) {
    .bio-left  { margin-right: 1.5rem; margin-bottom: 2rem; }
    .bio-right { margin-left: 1.5rem; }
}

modifications: Added an Influence block and took down the aspect ratio and picture clarity things Claude told me to use.

sources and credits:
https://whc.unesco.org/en/list/320- for an overview of Gaudi's works
https://sagradafamilia.org/en/antoni-gaudi- for a deeper understanding of his most famous work
https://www.casabatllo.es/en/antoni-gaudi/- For a deeper understanding of his artistic styles.