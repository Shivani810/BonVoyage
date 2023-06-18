<!-- this is our booking page -->

<script>

    import { onMount } from "svelte";
    import Navbar from "../../lib/Navbar.svelte"
    

    let selectedDate = "";
    let selectedTime = "";
    let bookingConfirmed = false;
    let title = "" ;
    let description = "" ;
   

    function handleDateChange(event) {
        selectedDate = event.target.value;
    }

    function handleTimeChange(event) {
        selectedTime = event.target.value;
    }

    function handleBookingConfirmation() {
        bookingConfirmed = true;
    }

    onMount(() => {
        console.log("Selected Date:", selectedDate);
        console.log("Selected Time:", selectedTime);


        // Retrieve the stored title from local storage
        title = localStorage.getItem('bannerTitle');
        console.log(title);

        // Retrieve the stored title from local storage
        description= localStorage.getItem('bannerDescription');
        console.log(description);
         
    })

        

   
    
</script>


<style>    

    /* CSS for the booking page */
        .Description-section {
            font-family: Arial, sans-serif;
            color: #333;
            text-align: left;
            padding-left: 120px;
            padding-right: 400px;
        }

        .Description-section h2 {
            color: teal;
            font-size: 20px;
            margin-bottom: 10px;
            font-weight: bold;
        }

        .Description-section h3 {
            color: black;
            margin-bottom: 10px;
            font-weight: bold;
        }

        .Description-section .description {
            color: black;
            margin-bottom: 10px;
        }

        .Description-section .details {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
        }

        .Description-section .duration,
        .Description-section .price {
            margin-top: 10px;
        }

        .Description-section .separator {
            border: none;
            border-top: 1px solid teal;
            margin: 0;
        }

        .Description-section .green-tick {
            color: green;
            margin-left: 5px;
            font-size: 10px;
            line-height: 1;
        }

        .Description-section .red-cross {
            color: red;
            margin-left: 5px;
            font-size: 10px;
            line-height: 1;
        } 
        
        .booking-section2 fieldset {
        width: 200px; /* Adjust the width value as desired */
        height: 50px;
        padding-left: 10px;
        padding-right: 20px;
        display: inline-block;
        }   

        #my-date-picker {
        background-color: teal;
        color: #fff;
        border: 1px solid #fff;
        padding: 5px;
        border-radius: 5px;
    }

    #my-time-picker {
        background-color: teal;
        color: #fff;
        border: 1px solid #fff;
        padding: 5px;
        border-radius: 5px;
    }

    /* Add the following styles to make the legend coherent with the navbar */
    legend {
        color: teal;
        font-size: 16px;
        font-weight: bold;
        margin-bottom: 10px;
    }

    .confirmation-message {
        margin-top: 20px;
        color: teal;
        font-weight: bold;
        padding-left: 120px; 
        padding-right: 400px; 
    }
   

    /* Media Queries for Responsive Layout */
        @media (max-width: 768px) {
            .Description-section {
                padding: 0 10px;
            }        

            .Description-section h2 {
                font-size: 30px;
            }
        }
        
        @media (max-width: 480px) {
            .Description-section {
                padding: 0 5px;
            }
            
            .Description-section h2 {
                font-size: 24px;
            }

            .Description-section h3 {
                font-size: 18px;
            }
        }

        .booking-details button {
        background-color: teal;
        color: #fff;
        padding: 10px 20px;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        font-weight: bold;
    }

</style>

<Navbar/> <!-- Directly imported component from lib -->


        <div class="Description-section">
                <h2 class= "title">{title}</h2>
                <h3>Activitythis activity</h3>
                <p class="description">{description}</p>
                <hr class="separator">
                
                <div class="details">
                <p>Free cancellation <span class="green-tick">&#10004;</span></p>
                <p>Food and Drinks <span class="red-cross">&#10060;</span></p>
                <p class="duration"></p>
                <p class="price"></p>
                </div>

                <div class="booking-section2">
                    <h3>Select a Date and Time</h3>
                    <hr class="separator">
                    <fieldset>
                        <legend>Pick Your Date</legend>
                        <label for="my-date-picker"> Date:
                            <input 
                                id= "my-date-picker"
                                type ="date" 
                                min="2022-05-31" 
                                max="2023-07-15"
                                name="selectedDate" 
                                bind:value={selectedDate}
                                >   
                                </label>
                    </fieldset> 
                    <fieldset>
                        <legend>Pick Your Time</legend>
                        <label for="my-time-picker"> Time:</label>
                            <input 
                                id= "my-time-picker"
                                type ="time" 
                                min="09:00" 
                                max="23:59"                       
                                name="selectedTime" 
                                bind:value={selectedTime}
                                >                                   
                    </fieldset> 
                    
                    <div class="booking-details">
                        <h3>Confirm your Choices</h3>
                        {#if selectedDate && selectedTime}
                            <h3>{selectedDate}</h3>
                            <h3>{selectedTime}</h3>
                            <button id="book-button" on:click={handleBookingConfirmation}>Book Your Request</button>
                        {:else}
                            <p>Please select a date and time.</p>
                        {/if}
                    </div>
                    
                    
                </div>             


        </div>

        {#if bookingConfirmed}
    <p class="confirmation-message">Your booking has been confirmed on {selectedDate} at {selectedTime}.</p>
{/if}
