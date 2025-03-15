<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ebb+Tress | Sign Up for Free Hair Emergency Guide</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Lato:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Lato', sans-serif;
      background-color: #ffffff;
      color: #185228;
      margin: 0;
      padding: 20px;
      line-height: 1.6;
      text-align: center;
    }
    .container {
      max-width: 600px;
      margin: 0 auto;
      padding: 20px;
    }
    h1 {
      font-family: 'Playfair Display', serif;
      font-size: 28px;
      color: #185228;
      margin-bottom: 20px;
      line-height: 0.3;
    }
    p {
      text-align: center;
    }
    .form-group {
      margin-bottom: 15px;
    }
    label {
      font-size: 16px;
      display: block;
      margin-bottom: 5px;
    }
    input[type="text"],
    input[type="email"] {
      width: 100%;
      max-width: 300px;
      padding: 10px;
      font-size: 16px;
      border: 1px solid #D4AF37;
      border-radius: 5px;
    }
    button {
      font-family: 'Lato', sans-serif;
      font-size: 16px;
      padding: 10px 20px;
      background-color: #185228;
      color: #ffffff;
      border: none;
      cursor: pointer;
      border-radius: 5px;
    }
    button:hover {
      background-color: #D4AF37;
      color: #185228;
    }
    #success-message {
      display: none;
      margin-top: 20px;
      padding: 15px;
      background-color: #185228;
      color: #ffffff;
      border-radius: 5px;
    }
    .footer {
      font-size: 12px;
      text-align: center;
      margin-top: 20px;
      color: #666;
    }
    @media (max-width: 600px) {
      h1 { font-size: 24px; }
      label { font-size: 14px; }
      button { font-size: 14px; }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Ebb+Tress</h1>
    <h1>Sign Up for Your Free Hair Emergency Guide</h1>
    <p>Enter your details to unlock expert hair care solutions!</p>

    <form id="signup-form">
      <div class="form-group">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required>
      </div>
      <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
      </div>
      <button type="submit">Get Your Free Guide</button>
    </form>

    <div id="success-message">
      <p>Thank you for signing up! <a href="https://sites.google.com/view/ebbandtress/hair-emergency-guide/free-hair-emergency-guide?authuser=0" style="color: #D4AF37;">Click here</a> to access your Free Hair Emergency Guide. You’ll also receive a PDF version in your email shortly.</p>
    </div>

    <div class="footer">© 2025 Ebb+Tress | You Deserve Healthy Hair!</div>
  </div>

  <script>
    document.getElementById('signup-form').addEventListener('submit', async function(event) {
      event.preventDefault();
      
      const name = document.getElementById('name').value;
      const email = document.getElementById('email').value;
      const data = { name, email };

      try {
        const response = await fetch('https://script.google.com/macros/s/AKfycbybtmqVQm-aQixhTAeFuGp24_mIFM0boeLwJDAxxpM4xjy_HfDzxhVxfULFxGnM2MFxYg/exec', {
          method: 'POST',
          body: JSON.stringify(data),
          headers: { 'Content-Type': 'application/json' }
        });
        const result = await response.json();

        if (result.status === 'success') {
          document.getElementById('signup-form').style.display = 'none';
          document.getElementById('success-message').style.display = 'block';
        } else {
          alert('There was an error submitting your form. Please try again. Error: ' + result.message);
        }
      } catch (error) {
        alert('Error: ' + error.message);
      }
    });
  </script>
</body>
</html># ebbandtress-signup
