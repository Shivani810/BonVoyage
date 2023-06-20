<!-- this is the home page -->

<style>
     
     /* CSS styles for the background section */
     .background-section {
        background-image: url('https://wallpaperaccess.com/full/1168014.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center center;
        height: 400px; 
        width: 100%;
        position: relative;
    }  
   
    /* CSS for the banners */
    
    .landmark-section{
        display: flex;
        text-align: center; /* Center align the banners */
        padding: 0 120px; 
        overflow-x: scroll; /* Enabling horizontal scrolling */
    }
    
    .banner {
        width: 300px;
        margin: 20px 10px;
        border: 0.5px solid teal;
        padding: 0;
        padding-bottom: 10px;
        text-align: center;
        display: inline-block;
        vertical-align: top;
    }

     /* CSS for the images in banners */
    
    .banner img {
    width: 100%;
    height: 250px; 
    margin: 0;
    object-fit: cover;
    cursor: pointer;
    }

    .banner img {
    transition: transform 0.3s ease-in-out;
    }

    .banner img:hover {
    transform: scale(1.1);
    }
    
    .banner h3 {
        color: teal;
    }
    
    .banner .description {
        margin: 10px;
    }
    
    .banner .duration {
        font-weight: bold;
    }
    
    .banner .separator {
        border: none;
        border-top: 1px solid teal;
        margin: 10px;
    }
    
    .banner .price {
        font-weight: bold;
        color: teal;
    }
    
    .banner .book-btn {
        display: inline-block;
        background-color: teal;
        color: #fadd06;
        border: none;
        padding: 8px 16px;
        text-align: center;
        text-decoration: none;
        font-size: 16px;
        border-radius: 4px;
        cursor: pointer;
        transition: background-color 0.3s;
        margin-top: 10px;
    }
    
    .banner .book-btn:hover {
        background-color: #ddd;
    }  


</style>
  
<Navbar/>  <!-- Directly imported component from lib -->

<div class = "background-section"></div>

<div class="landmark-section">
    <div class="scroll-triangle left"></div>
    <div class="landmark-images">
        <div class="banner">
            <img src="https://img2.goodfon.com/wallpaper/nbig/b/c6/arc-de-triomphe-paris-france-6630.jpg" alt="Eiffel Tower" onclick="openPopup('https://img2.goodfon.com/wallpaper/nbig/b/c6/arc-de-triomphe-paris-france-6630.jpg', 'Eiffel Tower', 'Description of Eiffel Tower', '2 hrs', '8 Euros')">
            <h3>Arc de Triomphe</h3>
            <p class="description">"Marvel at the iconic Arc de Triomphe, a monumental triumphal arch in Paris. Learn about its historical significance and architectural grandeur."</p>
            <hr class="separator">
            <p class="duration">Duration 2 hrs</p>
            <p class="price">Price 20 Euros</p>
            <button class="book-btn" on:click={() => redirectToPage("/booking","Arc de Triomphe",{description1})}>Book</button>
            
        </div>
        
        <div class="banner">
            <img src="https://www.planetware.com/photos-large/F/eiffel-tower.jpg" alt="Eiffel Tower" onclick="openPopup('https://www.planetware.com/photos-large/F/eiffel-tower.jpg', 'Eiffel Tower', 'Description of Eiffel Tower', '2 hrs', '8 Euros')">
            <h3>Eiffel Tower</h3>
            <p class="description">"Experience the awe-inspiring Eiffel Tower, an architectural masterpiece and symbol of Paris. Enjoy breathtaking views of the city from its observation decks."</p>
            <hr class="separator">
            <p class="duration">Duration 2 hrs</p>
            <p class="price">Price 20 Euros</p>
            <button class="book-btn" on:click={() => redirectToPage("/booking","Eiffel Tower",{description2})}>Book</button>
        </div>
    
        <div class="banner">
            <img src="https://images.pexels.com/photos/1460145/pexels-photo-1460145.jpeg?cs=srgb&dl=pexels-adrienn-1460145.jpg&fm=jpg" alt="Notre Dame Cathedral" onclick="openPopup('https://images.pexels.com/photos/1460145/pexels-photo-1460145.jpeg?cs=srgb&dl=pexels-adrienn-1460145.jpg&fm=jpg', 'Notre Dame Cathedral', 'Description of Notre Dame Cathedral', '1 hr', '5 Euros')">
            <h3>Notre Dame Cathedral</h3>
            <p class="description">"Explore the magnificent Notre Dame Cathedral, a Gothic masterpiece known for its stunning stained glass windows and rich history."</p>
            <hr class="separator">
            <p class="duration">Duration 1 hr</p>
            <p class="price">Price 10 Euros</p>
            <button class="book-btn" on:click={() => redirectToPage("/booking","Notre Dame Cathedral",{description3})}>Book</button>
        </div>
    
        <div class="banner">
            <img src="https://t3.ftcdn.net/jpg/02/46/24/14/360_F_246241441_TK86KqjTH5Z3XaZ3NAbeiSkmZbGBDfuW.jpg" alt="Invalides" onclick="openPopup('https://t3.ftcdn.net/jpg/02/46/24/14/360_F_246241441_TK86KqjTH5Z3XaZ3NAbeiSkmZbGBDfuW.jpg', 'Invalides', 'Description of Invalides', '1 hr 30 min', '7 Euros')">
            <h3>Invalides</h3>
            <p class="description">"Discover the splendor of Invalides, a complex of museums and monuments housing Napoleon's tomb. Immerse yourself in French military history and art.</p>
            <hr class="separator">
            <p class="duration">Duration 1 hr 30 min</p>
            <p class="price">Price 15 Euros</p>
            <button class="book-btn" on:click={() => redirectToPage("/booking","Invalides",{description4})}>Book</button>
        </div>
    
        <div class="banner">
            <img src="https://c0.wallpaperflare.com/preview/821/777/259/paris-france-the-centre-pompidou-centre-pompidou.jpg" alt="Centre Pompidou" onclick="openPopup('https://c0.wallpaperflare.com/preview/821/777/259/paris-france-the-centre-pompidou-centre-pompidou.jpg', 'Centre Pompidou', 'Description of Centre Pompidou', '2 hrs', '9 Euros')">
            <h3>Centre Pompidou</h3>
            <p class="description">"Visit the vibrant Centre Pompidou, a modern art museum showcasing a diverse collection of contemporary artworks and innovative exhibitions."</p>
            <hr class="separator">
            <p class="duration">Duration 2 hrs</p>
            <p class="price">Price 20 Euros</p>
            <button class="book-btn" on:click={() => redirectToPage("/booking","Centre Pompidou",{description5})}>Book</button>
        </div>
    
        <div class="banner">
            <img src="https://facnh.com/wp-content/uploads/2021/09/Luxembourg-Gardens-2.jpg" alt="Jardins du Luxembourg" onclick="openPopup('https://facnh.com/wp-content/uploads/2021/09/Luxembourg-Gardens-2.jpg', 'Jardins du Luxembourg', 'Description of Jardins du Luxembourg', '1 hr', '4 Euros')">
            <h3>Jardins du Luxembourg</h3>
            <p class="description">"Stroll through the beautiful Jardins du Luxembourg, a serene park with meticulously manicured gardens, ornate fountains, and a sense of tranquility."</p>
            <hr class="separator">
            <p class="duration">Duration 1 hr</p>
            <p class="price">Price 10 Euros</p>
            <button class="book-btn" on:click={() => redirectToPage("/booking","Jardins du Luxembourg",{description6})}>Book</button>
        </div>
    
        <div class="banner">
            <img src="https://smapse.com/storage/2020/06/converted/895_0_sakre-ker-smapse1.jpg" alt="Montmartre" onclick="openPopup('https://smapse.com/storage/2020/06/converted/895_0_sakre-ker-smapse1.jpg', 'Montmartre', 'Description of Montmartre', '2 hrs', '10 Euros')">
            <h3>Montmartre</h3>
            <p class="description">"Experience the bohemian charm of Montmartre, an artistic neighborhood famous for its picturesque streets, historic cafes, and the iconic Sacré-Cœur Basilica."</p>
            <hr class="separator">
            <p class="duration">Duration 2 hrs</p>
            <p class="price">Price 20 Euros</p>
            <button class="book-btn" on:click={() => redirectToPage("/booking","Montmartre",{description7})}>Book</button>
        </div>
    </div>
    <div class="scroll-triangle right"></div>
</div>

<Form/> <!-- Directly imported component from lib -->

<script>

    import Navbar from "../lib/Navbar.svelte";
    import Form from "../lib/Form.svelte";

    let description1 = "Marvel at the iconic Arc de Triomphe, a monumental triumphal arch in Paris. Learn about its historical significance and architectural grandeur.";
    let description2 ="Experience the awe-inspiring Eiffel Tower, an architectural masterpiece and symbol of Paris. Enjoy breathtaking views of the city from its observation decks.";
    let description3= "Explore the magnificent Notre Dame Cathedral, a Gothic masterpiece known for its stunning stained glass windows and rich history.";
    let description4 = "Discover the splendor of Invalides, a complex of museums and monuments housing Napoleon's tomb. Immerse yourself in French military history and art.";
    let description5 ="Visit the vibrant Centre Pompidou, a modern art museum showcasing a diverse collection of contemporary artworks and innovative exhibitions.";
    let description6= "Stroll through the beautiful Jardins du Luxembourg, a serene park with meticulously manicured gardens, ornate fountains, and a sense of tranquility.";
    let description7 = "Experience the bohemian charm of Montmartre, an artistic neighborhood famous for its picturesque streets, historic cafes, and the iconic Sacré-Cœur Basilica.";


    function redirectToPage(url, title, description) {   

    // Store the title in local storage brfore redirecting
     localStorage.setItem('bannerTitle', title);
     localStorage.setItem('bannerDescription', JSON.stringify(description));
  
    // Redirect to the desired page
    window.location.href = url;
    }

</script>
  