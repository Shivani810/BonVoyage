<!-- this is the subscribe page -->

<script>
    import Navbar from "../../lib/Navbar.svelte";
    import { createClient } from '@supabase/supabase-js'; // Import the createClient function  
        
   
      // Initialize Supabase client
        const supabaseUrl = "https://gxemhqnvpdlgvcakouvz.supabase.co";
        const supabaseKey = "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Imd4ZW1ocW52cGRsZ3ZjYWtvdXZ6Iiwicm9sZSI6ImFub24iLCJpYXQiOjE2ODU5NTQ1MDYsImV4cCI6MjAwMTUzMDUwNn0.yvJf6YoQaW3dLdVVwHjlY1b4PiIBhWFEWrEP4nCbY0s";
        const supabase = createClient(supabaseUrl, supabaseKey, {
  persistSession: false,});


        // Function to handle form submission
  async function sendMessage(event) {
    event.preventDefault();

    const nameInput = document.getElementById('name-input');
    const emailInput = document.getElementById('email-input');
    const messageInput = document.getElementById('message-input');

    const name = nameInput.value;
    const email = emailInput.value;
    const message = messageInput.value;

        // Insert the data into the "contact" table
        const { data, error } = await supabase.from('contact').insert([
        { name, email, message },
        ]);

        if (error) {
        console.error('Error inserting data:', error);
        } else {
        console.log('Data inserted successfully:', data);
        // Reset form inputs after successful submission
        nameInput.value = '';
        emailInput.value = '';
        messageInput.value = '';
        }
    }



</script>

<Navbar/> <!-- Directly imported component from lib -->

<div class="form-container">
    <h2>Newsletter Subscription</h2>
    <form>
        <input type="email" placeholder="Your Email" required>
        <button type="submit">Subscribe</button>
    </form>
</div>

<div class="form-container">
    <h2>Contact Us</h2>
    <form on:submit={sendMessage}>
        <input type="text" id="name-input" placeholder="Your Name" required>
        <input type="email" id="email-input" placeholder="Your Email" required>
        <textarea id="message-input" placeholder="Message" rows="4" required></textarea>
        <button type="submit">Send Message</button>
    </form>
</div>



<style>

    /* CSS styles for the background section */
        .form-container {
            max-width: 500px;
            margin: 20px auto;
            padding: 16px;
            background-color: #f2f2f2;
        }

        .form-container h2{
            color:teal;
        }

        .form-container input[type=text], 
        .form-container input[type=email],
        .form-container textarea {
            width: 100%;
            padding: 12px 20px;
            margin: 8px 0;
            display: inline-block;
            border: 1px solid #ccc;
            box-sizing: border-box;
        }

        .form-container button[type=submit] {
            background-color: teal;
            color: white;
            padding: 12px 20px;
            border: none;
            cursor: pointer;
            width: 100%;
        }

        .form-container button[type=submit]:hover {
            background-color: #45a049;
        }

</style>