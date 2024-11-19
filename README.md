body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background: linear-gradient(to right, #ff7e5f, #feb47b);
    color: #333;
  }
  
  .container {
    text-align: center;
    padding: 50px 20px;
  }
  
  h1 {
    font-size: 2.5rem;
    color: #fff;
    margin-bottom: 30px;
  }
  
  .names {
    margin-bottom: 30px;
  }
  
  .name-button {
    background: #ff6f61;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    margin: 0 10px;
    font-size: 1rem;
    cursor: pointer;
    transition: transform 0.3s ease, background-color 0.3s ease;
  }
  
  .name-button:hover {
    transform: scale(1.1);
    background-color: #e55b50;
  }
  
  .hobbies {
    margin-top: 30px;
  }
  
  .hobby {
    display: none;
    animation: fadeIn 0.5s ease-in-out forwards;
    border: 2px solid white;
    padding: 20px;
    background-color: rgba(255, 255, 255, 0.9);
    border-radius: 10px;
    margin: 20px auto;
    max-width: 600px;
  }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(-20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hobi Mereka</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="container">
    <h1>Hobi Kami</h1>
    <div class="names">
      <button class="name-button" data-target="feri">Feri</button>
      <button class="name-button" data-target="ixal">Ixal</button>
      <button class="name-button" data-target="himawan">Himawan</button>
    </div>
    <div class="hobbies">
      <div id="feri" class="hobby">
        <h2>Hobi Feri</h2>
        <p>Feri suka bermain gitar, mendaki gunung, dan fotografi.</p>
      </div>
      <div id="ixal" class="hobby">
        <h2>Hobi Ixal</h2>
        <p>Ixal gemar bermain sepak bola, membaca novel, dan memasak.</p>
      </div>
      <div id="himawan" class="hobby">
        <h2>Hobi Himawan</h2>
        <p>Himawan senang berenang, melukis, dan berkebun.</p>
      </div>
    </div>
  </div>
  <script src="script.js"></script>
</body>
</html>


document.addEventListener("DOMContentLoaded", () => {
  const buttons = document.querySelectorAll(".name-button");
  const hobbies = document.querySelectorAll(".hobby");

  buttons.forEach(button => {
    button.addEventListener("click", () => {
      hobbies.forEach(hobby => {
        hobby.style.display = "none"; // Sembunyikan semua hobi
      });

      const targetId = button.getAttribute("data-target");
      const target = document.getElementById(targetId);
      if (target) {
        target.style.display = "block"; // Tampilkan hobi yang dipilih
      }
    });
  });
});

# jusalpukat
