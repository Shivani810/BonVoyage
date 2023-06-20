<!-- this is the our history page -->
<script>
    import Navbar from "../../lib/Navbar.svelte";
    import Form from "../../lib/Form.svelte";
</script>

<style>    
  
    /* CSS styles for the three sections */
    .section {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0;
        background-color: #f5f5f5;
        margin-bottom: 0; 
    }
  
    .section .image {
        flex: 0 0 50%;
        max-width: 50%;
        margin-right: 20px;
    }

    .section .image img {
        width: 100%;
        height: auto;
    }

    .section .image {
    transition: transform 0.3s ease-in-out;
    }

    .section .image:hover {
    transform: scale(1.02);    
    }
  
    .section .text {
        flex: 0 0 50%;
        max-width: 50%;
        text-align: center;
        padding: 0 80px; 
        box-sizing: border-box;         
    }
    
    .section h2 {
        font-size: 24px;
        margin-top: 0;
        color: teal;
    }
  
    .section p {
        margin-bottom: 0;
        color: teal;
    }

    .section .text h2:hover {
    transform: scale(1.3); 
    
    }
    .section .text p:hover {
        transform: scale(1.02);
        font-weight: bold;
        
    }

    .form-container {
      text-align: center;
      margin-top: 0px;
    }
</style>
  

<Navbar/> <!-- Directly imported component from lib -->

<div class="section">
    <div class="image">
        <img src="https://cdn.pixabay.com/photo/2013/04/11/19/46/building-102840_1280.jpg" alt="Not loaded">
    </div>
    <div class="text">
        <h2>How did we start?</h2>
        <p>At BonVoyage, our journey began with a simple idea: connecting travelers with knowledgeable student guides. We recognized the need for a more personalized and affordable travel experience, where tourists could explore their desired destinations with the help of local students. By leveraging the expertise and passion of students, we aimed to create unforgettable travel experiences that go beyond traditional tourist routes.

        </p>
    </div>
</div>

<div class="section">
    <div class="text">
        <h2>Why BonVoyage?</h2>
        <p>BonVoyage stands out from other travel platforms due to our unique approach. We believe that traveling should be accessible and affordable for everyone, which is why we offer our services at an incredibly affordable rate. For just 10 euros per hour, tourists can enjoy the expertise of our student partners who are not only passionate about their respective destinations but also eager to share their knowledge and insights with visitors. With BonVoyage, you can embark on a budget-friendly journey while gaining a deeper understanding of your chosen location.</p>
    </div>
    <div class="image">
        <img src="https://cdn-imgix.headout.com/blog-content/image/63f25c4682440fdf3bb659eb3246b06a-%C2%A9Disney%20(6).png" alt="Not loaded">
    </div>
</div>

<div class="section">
    <div class="image">
        <img src="https://www.civitatis.com/f/francia/paris/tour-misterios-opera-garnier-r32.jpg" alt="Not loaded">
    </div>
    <div class="text">
        <h2>Our Values</h2>
        <p>At BonVoyage, we hold strong values that guide everything we do. We are committed to fostering meaningful connections between travelers and student partners, enabling cultural exchange and promoting mutual understanding. Our platform values diversity, inclusivity, and respect for different perspectives. We strive to create a supportive environment where students can showcase their talents and build valuable skills while assisting tourists in making the most of their travel experiences. By upholding these values, we aim to create a positive impact on both travelers and student partners, enriching their journeys and creating lasting memories.</p>
    </div>
</div>


<div class="form-container">
    <Form/> <!-- Directly imported component from lib -->
</div>





