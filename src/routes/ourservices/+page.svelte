<!-- this is our services page -->


<script>
import Navbar from "../../lib/Navbar.svelte";
</script>

<Navbar/> <!-- Directly imported component from lib -->

<div class="header">
	<h1>BonVoyage</h1>
  </div>
 
  <div class="intro">
	<p>THE AFFORDABLE AND INNOVATIVE SERVICE PROVIDING DIVERSE, AFFORDABLE AND CUSTOMISED VISITS FOR TOURISTS</p>
	<p>PARIS / Expanding in ÎLE-DE-FRANCE and LYON AREA</p>
  </div>
 
  <div class="services">
	<div class="service">
  	<img src="https://www.unjourdeplusaparis.com/wp-content/uploads/2012/04/sainte-chapelle-paris1.jpg" alt="Historical Monuments">
  	<h2>Historical Monuments</h2>
	</div>
	
	<div class="service">
  	<img src="https://www.perledoree.fr/wp-content/uploads/2022/12/f11115-preparation-macaron-sans-gluten-a.jpg" alt="Culinary Experiences" width="250" height="167">
  	<h2>Culinary Experiences</h2>
	</div>
	
	<div class="service">
  	<img src="https://lp-cms-production.imgix.net/2021-03/shutterstockRF_703650337.jpg?auto=format&q=75&w=1920" alt="Parks and Gardens">
  	<h2>Parks and Gardens</h2>
	</div>
	
	<div class="service">
  	<img src="https://www.transilien.com/sites/transilien/files/styles/manual_crop/public/2021-12/Mus%C3%A9e%20d%27Orsay.jpg?h=f87dcf60&itok=38D2pZhA" alt="Museums">
  	<h2>Museums</h2>
	</div>
	
	<div class="service">
  	<img src="https://dynamic-media-cdn.tripadvisor.com/media/photo-o/26/92/e4/97/disneyland-paris.jpg?w=1200&h=1200&s=1" alt="Other">
  	<h2>Other</h2>
	</div>
  </div>


  <style>	
	
	.header {
  	background-color: #f9e076;
  	padding: 20px;
  	text-align: center;
	}
	
	.header h1 {
  	margin: 0;
  	font-size: 28px;
  	color: teal;
	}
	
	.intro {
  	background-color: #ffffff;
  	padding: 20px;
  	text-align: center;
	}
	
	.services {
  	display: flex;
  	flex-wrap: wrap;
  	justify-content: space-around;
  	padding: 20px;
	}
	
	.service {
  	background-color: #fff;
  	border-radius: 8px;
  	box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  	margin: 10px;
  	padding: 20px;
  	text-align: center;
  	width: 250px;
	}
	
	.service h2 {
  	font-size: 18px;
  	margin-top: 0;
	}
	
	.service img {
  	max-width: 100%;
  	border-radius: 8px;
  	margin-bottom: 10px;
	}
  </style>


  