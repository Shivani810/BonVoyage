<!-- this is the subscribe page -->

<script>
    import Navbar from "../../lib/Navbar.svelte";
    import Form from "../../lib/Form.svelte";
</script>

<Navbar/>

<div class="form-container">
    <h2>Newsletter Subscription</h2>
    <form>
        <input type="email" placeholder="Your Email" required>
        <button type="submit">Subscribe</button>
    </form>
</div>

<div class="form-container">
    <h2>Contact Us</h2>
    <form>
        <input type="text" placeholder="Your Name" required>
        <input type="email" placeholder="Your Email" required>
        <textarea placeholder="Message" rows="4" required></textarea>
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