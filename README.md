<!DOCTYPE html>
<html>
    <head>
        <title>newsletter-sign-up-sucess-message</title>
        <link rel="stylesheet" href="style.css">
    </head>
<body>
    <section id="newsletter-section">
        <div id="form-container" class="container">
            <h1>Stay Updated!</h1>
            <p>Join 60,000+ product managers receiving monthly<br> updates on:</p>
            <p><img src="assets/icon-list.svg" alt=""> Product discovery and building what matters </p>
            <p> <img src="assets/icon-list.svg" alt=""> Measuring to ensure updates are a success </p>
            <p> <img src="assets/icon-list.svg" alt=""> And much more! </p>
            <form id="newsletter-form">
                <div class="one">
                    <label for="email">Email address</label>
                    <input type="email" id="email" name="email" placeholder="Email@company.com" required>
                </div>
                <br>
                <button type="submit">Subscribe to Monthly Newsletter</button>
            </form>
        </div>
        <br>
        <div class="container">
            <img src="assets/illustration-sign-up-desktop.svg" alt="Newsletter illustration">
        </div>
    </section>


    <script>
        document.getElementById("newsletter-form").addEventListener("submit", function(event) {
            event.preventDefault(); // Prevents the form from actually submitting
            
            let emailInput = document.getElementById("email").value;
            
            if (emailInput.trim() !== "") { // Ensures input is not empty
                document.getElementById("newsletter-section").innerHTML = `
                    <div style="text-align: center; padding: 20px;">
                        <h1>Thank you for subscribing!</h1>
                        <p>We have added <strong>${emailInput}</strong> to our mailing list.</p>
                        <p>Stay tuned for the latest updates!</p>
                    </div>
                `;
            }
        });
    </script>
</body>
</html>
