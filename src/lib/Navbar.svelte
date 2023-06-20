<script>

export let title = "BonVoyage"

</script>

<div class="navbar">
    <a class="title" href="/">{title}</a>
    <a class="logo" href="/">
        <img src="/icons8-wedding-travel-48.png" alt="Logo">
    </a>    
    <a href="/ourhistory">Our History</a>
    <a href="/ourservices">Our Services</a>
    <a href="/subscribe">Subscribe</a>
    <a href="/socialmedia">Social Media</a>
</div>

<style>
        /* CSS for the navigation bar */
        .navbar {
        background-color: teal;
        overflow: hidden;
        margin: 0;
        padding: 0;
        }
    
        .navbar a {
            float: left;
            display: block;
            color: #fadd06;
            text-align: center;
            padding: 14px 16px;
            text-decoration: none;
            font-size: 20px;
           
        }
        
        .navbar a:hover {           
            transform: scale(1.2);
        }
        
        .navbar .title{
            float: left;
            padding: 14px 16px;
            font-size: 20px;            
        }

        .navbar .logo img {
        float: left;
        height: 22.5px; 
        margin-right: 0px; 
    }

    .navbar .logo:hover {
        background-color: initial; /* Reset the background color */
        transform: scale(1.2);
    }

   </style>