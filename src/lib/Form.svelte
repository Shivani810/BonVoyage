
<!-- Subscription Newsletter Section -->

<script>

export let section = "Subscribe to Our Newsletter"

</script>

<div class="subscription-section">
    <h2>{section}</h2>
    <p>Stay updated with the latest travel news and offers.</p>
    <input type="email" placeholder="Enter your email address" required>
    <button>Subscribe</button>
</div>

<style>
    /* CSS for the subscription newsletter section */
        .subscription-section {
            background-color: #fadd06;
            padding: 40px;
            text-align: center;
        }

        .subscription-section h2 {
            color: teal;
        }

        .subscription-section p {
            color: #555;
            font-size: 16px;
            margin-top: 10px;
        }

        .subscription-section input[type="email"] {
            width: 300px;
            padding: 10px;
            margin-top: 10px;
            border: none;
            border-radius: 4px;
            font-size: 16px;
        }

        .subscription-section button {
            background-color: teal;
            color: #fadd06;
            border: none;
            padding: 10px 20px;
            margin-top: 10px;
            border-radius: 4px;
            font-size: 16px;
            cursor: pointer;
        }

        .subscription-section button:hover  {
        background-color: #ddd;
        }
</style>        
