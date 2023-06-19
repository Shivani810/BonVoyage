<script>
	import Navbar from "../../lib/Navbar.svelte";
	import { onMount } from "svelte"; 


let slides;
let currentSlide = 0;

onMount(() => {
  const slideInterval = setInterval(nextSlide, 2000);

  function nextSlide() {
	slides[currentSlide].animate([{ opacity: 1 }, { opacity: 0 }], {
	  duration: 1000,
	  fill: "forwards",
	});
	currentSlide = (currentSlide + 1) % slides.length;
	slides[currentSlide].animate([{ opacity: 0 }, { opacity: 1 }], {
	  duration: 1000,
	  fill: "forwards",
	});
  }

  return () => {
	clearInterval(slideInterval);
  };
});
  </script>

<Navbar/>  <!-- Directly imported component from lib -->
  
  <div class="slideshow">
	<img class="slide" src="https://voyage-onirique.com/wp-content/uploads/2020/11/Le-Louvre-Paris.jpg" alt="Louvre Museum">
	<img class="slide" src="https://www.musee-armee.fr/fileadmin/user_upload/programmation-illustration/animations_pedagogiques_agenda/visites-commentees/Focus-Invalides-1h-1920.jpg" alt="Invalides">
	<img class="slide" src="https://uploads-ssl.webflow.com/6107ac893efb8524ac54eac1/6194da68d855799e36d63eec_Jardin%20de%20cluny%20_Notre-dame_%20city%20guide2%20(1).png" alt="Jardin de Cluny">
	<img class="slide" src="https://wallpapercave.com/wp/wp5594348.jpg" alt="Eiffel Tower">
	<img class="slide" src="https://media.timeout.com/images/105976901/image.jpg" alt="Notre-Dame Cathedral">
	<img class="slide" src="https://backend-shop.salon-du-chocolat.com/api/v1/image/4890" alt="Chocolate Shop">

  </div>
  
  <div class="social-links">
	<div class="social-links-title">Stay connected with us. Find us on social media:</div>
	<div class="social-link">
	  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4f/Facebook_circle_pictogram.svg/2048px-Facebook_circle_pictogram.svg.png" alt="Facebook">
	  <span><a href="https://www.facebook.com/" target="_blank">Facebook</a></span>
	</div>
	<div class="social-link">
	  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e8/Instagram_circle.svg/2048px-Instagram_circle.svg.png" alt="Instagram">
	  <span><a href="https://www.instagram.com/visitparisregion/?hl=en" target="_blank">Instagram</a></span>
	</div>
	<div class="social-link">
	  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/16/Youtube_circle.svg/2048px-Youtube_circle.svg.png" alt="YouTube">
	  <span><a href="https://www.youtube.com/@HungryPassport" target="_blank">YouTube</a></span>
	</div>
  </div>
  
  <style>
	/* Slideshow Styles */
	.slideshow {
	  position: fixed;
	  top: 0;
	  left: 0;
	  width: 100%;
	  height: 100%;
	  z-index: -1;
	  overflow: hidden;
	}
  
	.slide {
	  position: absolute;
	  top: 0;
	  left: 0;
	  width: 100%;
	  height: 100%;
	  opacity: 0;
	  transition: opacity 1s ease-in-out;
	}
  
	.slide:first-child {
	  opacity: 1;
	}
  
	/* Social Media Links Styles */
	.social-links {
	  width: 100%;
	  background-color: #f1f1f1;
	  padding: 20px;
	  text-align: center;
	  display: flex;
	  flex-direction: column;
	  align-items: center;
	}
  
	.social-links-title {
	  font-size: 18px;
	  font-weight: bold;
	  margin-bottom: 10px;
	}
  
	.social-link {
	  display: flex;
	  align-items: center;
	  margin-bottom: 10px;
	}
  
	.social-link img {
	  width: 50px;
	  height: 50px;
	  margin-right: 10px;
	}
  
	.social-link span {
	  font-size: 14px;
	  font-weight: bold;
	}
  </style>
  