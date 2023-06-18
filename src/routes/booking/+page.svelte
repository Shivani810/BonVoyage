<!-- this is our booking page -->

<script>
    import Navbar from "../../lib/Navbar.svelte";
</script>

<style>    

    /* CSS for the booking page */
        .booking-section {
            font-family: Arial, sans-serif;
            color: #333;
            text-align: left;
            padding-left: 120px;
            padding-right: 400px;
        }

        .booking-section h2 {
            color: teal;
            font-size: 20px;
            margin-bottom: 10px;
            font-weight: bold;
        }

        .booking-section h3 {
            color: black;
            margin-bottom: 10px;
            font-weight: bold;
        }

        .booking-section .description {
            color: black;
            margin-bottom: 10px;
        }

        .booking-section .details {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
        }

        .booking-section .duration,
        .booking-section .price {
            margin-top: 10px;
        }

        .booking-section .separator {
            border: none;
            border-top: 1px solid teal;
            margin: 0;
        }

        .booking-section .green-tick {
            color: green;
            margin-left: 5px;
            font-size: 10px;
            line-height: 1;
        }

        .booking-section .red-cross {
            color: red;
            margin-left: 5px;
            font-size: 10px;
            line-height: 1;
        }
       

    /* Media Queries for Responsive Layout */
        @media (max-width: 768px) {
            .booking-section {
                padding: 0 10px;
            }
        

            .booking-section h2 {
                font-size: 30px;
            }
        }


        @media (max-width: 480px) {
            .booking-section {
                padding: 0 5px;
            }


            .booking-section h2 {
                font-size: 24px;
            }

            .booking-section h3 {
                font-size: 18px;
            }
        }
</style>

<Navbar/> <!-- Directly imported component from lib -->


<div class="booking-section">
    <h2 class= "title">Page Title</h2>
    <h3>About this activity</h3>
    <p class="description"></p>
    <hr class="separator">
    <div class="details">
    <p>Free cancellation <span class="green-tick">&#10004;</span></p>
    <p>Food and Drinks <span class="red-cross">&#10060;</span></p>
    <p class="duration"></p>
    <p class="price"></p>
</div>

<div class="booking-section2">
    <h3>Booking Options</h3>
    <div class="booking-option">
        <span>Number of adults:</span>
        <div class="quantity">
            <span class="subtract">-</span>
            <span class="count">0</span>
            <span class="add">+</span>
        </div>
    </div>
    <div class="booking-option">
        <span>Choose your date:</span>
        <div class="dropdown">
            <button class="dropdown-btn">Select date</button>
            <div class="dropdown-content">
                <!-- Calendar goes here -->
            </div>
        </div>
    </div>
</div>
</div>
