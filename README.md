<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Flow Website</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f8f8f8;
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    header {
      background: #ff6b6b;
      color: white;
      width: 100%;
      padding: 20px;
      text-align: center;
      font-size: 24px;
    }

    nav {
      margin: 20px 0;
    }

    nav button {
      padding: 10px 20px;
      margin: 0 10px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-size: 16px;
      background-color: #4a90e2;
      color: white;
      transition: 0.3s;
    }

    nav button:hover {
      background-color: #357abd;
    }

    .page {
      display: none;
      width: 80%;
      max-width: 600px;
      padding: 20px;
      background: white;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      margin-bottom: 40px;
    }

    .page.active {
      display: block;
    }
  </style>
</head>
<body>

  <header>My Flow Website</header>

  <nav>
    <button onclick="showPage('photo')">Photo</button>
    <button onclick="showPage('message')">Message</button>
    <button onclick="showPage('love')">Love</button>
  </nav>

  <div id="photo" class="page active">
    <h2>Photo Page</h2>
    <p>This is the photo section.</p>
    <img src="https://via.placeholder.com/400x200" alt="Photo Example">
  </div>

  <div id="message" class="page">
    <h2>Message Page</h2>
    <p>This is the message section.</p>
  </div>

  <div id="love" class="page">
    <h2>Love Page</h2>
    <p>This is the love section.</p>
  </div>

  <script>
    function showPage(pageId) {
      const pages = document.querySelectorAll('.page');
      pages.forEach(page => page.classList.remove('active')); // hide all
      document.getElementById(pageId).classList.add('active'); // show selected
    }
  </script>

</body>
</html>
