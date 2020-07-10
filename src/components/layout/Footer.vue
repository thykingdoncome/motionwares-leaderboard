<template>
  <footer>
    <div class="footer-content">
      <div>
        <h4>Earn a Techdegree</h4>
        <div class="content-des">
          <img src="https://spng.pngfind.com/pngs/s/5-55682_treehouse-black-icon-treehouse-icon-hd-png-download.png" alt="footer" />
          <p>
            Get the skills you need tolaunch a career in tech with our
            structured certificate program
          </p>
        </div>
      </div>
      <div>
        <h4>Treehouse for Mobile</h4>
        <div class="content-des">
          <img src="https://spng.pngfind.com/pngs/s/5-55682_treehouse-black-icon-treehouse-icon-hd-png-download.png" alt="footer" />
          <p>
            Learn anytime and anywhere with Treehouse for iOS or Android. Download for free today
          </p>
        </div>
      </div>
      <div>
        <h4>Student Perks</h4>
        <div class="content-des">
          <img src="https://spng.pngfind.com/pngs/s/5-55682_treehouse-black-icon-treehouse-icon-hd-png-download.png" alt="footer" />
          <p>
              A collection of special discounts and exclusive offers available for Treehouse students
          </p>
        </div>
      </div>
    </div>

    <div class="socials">
        <div class="social-icons">
            <span><i class="fab fa-twitter"></i></span>
            <span><i class="fab fa-youtube"></i></span>
            <span><i class="fab fa-facebook-f"></i></span>
            <span><i class="fab fa-google-plus-g"></i></span>
            <span><i class="fab fa-instagram"></i></span>
            <span><i class="fab fa-linkedin-in"></i></span>
        </div>

        <div class="page-links"> 
            <span><a href="#">Treehouse Blog</a></span>
            <span><a href="#">About Treehouse</a></span>
            <span><a href="#">Privacy Policy</a></span>
            <span><a href="#">Terms & Conditions</a></span>
        </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
.footer-content {
    color:  #555555;
    margin-top: 2rem;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  column-gap: 1rem;
}

.content-des {
    padding: 1rem 0;
      display: grid;
  grid-template-columns: 50px auto;
}

.content-des img {
    display: inline-block;
}

.socials {
    display: flex;
    align-items: center;
    padding-top: 2rem;
}

.social-icons {
    display: flex;
    align-items: center;
    width: fit-content;
}

.social-icons span {
    background:  #555555;
    color: white;
    border-radius: 50%;
    margin-right: 1rem;
    text-align: center;
    cursor: pointer;
    transition: .4s;
    padding: .5rem;
}

.social-icons span:hover {
    background: lightslategrey;
}

.social-icons span:hover i {
    transform: scale(1.2, 1.2);
}

.social-icons span i {
    height: 15px;
    width: 15px;
    font-size: small;
}

.page-links span {
    margin-right: 1rem;
}

.page-links a {
  color:#555555;
  text-decoration: none;
  transition: .2s;
}

.page-links a:hover {
  color: black;
  padding-bottom: 2px;
  border-bottom: 1px solid black;
}

</style>
