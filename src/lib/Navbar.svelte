<script>

export let logo = "BonVoyage"

</script>

<div class="navbar">
    <a class="logo" href="/">{logo}</a>
    <a href="/ourhistory">Our History</a>
    <a href="/ourservices">Our Services</a>
    <a href="/subscribe">Subscribe</a>
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
            font-size: 18px;
        }
        
        .navbar a:hover {
            background-color: #ddd;
        }
        
        .navbar .logo {
            float: left;
            padding: 14px 16px;
            font-size: 18px;
            font-weight: bold;
        }

   </style>