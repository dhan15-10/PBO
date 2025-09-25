<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Portfolio — Adira Fatih Romadhan</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <h1>Adira Fatih Romadhan</h1>
    <nav>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#skills">Skills</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <main>
    <section id="about">
      <h2>About</h2>
      <p>Saya membuat situs web menggunakan HTML, CSS, dan JavaScript.</p>
    </section>

    <section id="projects">
      <h2>Projects</h2>
      <div class="project">
        <h3>Portfolio Website</h3>
        <p>Website sederhana menggunakan HTML dan CSS.</p>
      </div>
    </section>

    <section id="skills">
      <h2>Skills</h2>
      <p>HTML • CSS • JavaScript</p>
    </section>

    <section id="contact">
      <h2>Contact</h2>
      <form id="contact-form">
        <input id="name" placeholder="Nama" required />
        <input id="email" type="email" placeholder="Email" required />
        <textarea id="message" placeholder="Pesan" required></textarea>
        <button type="submit">Kirim</button>
      </form>
      <div id="form-result"></div>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Adira Fatih Romadhan</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>

-- CSS --
body {
  font-family: Arial, sans-serif;
  margin: 0;
  line-height: 1.6;
  background: #f8faff;
  color: #222;
}

header {
  background: #02215b; /* biru gelap */
  color: white;
  padding: 1rem;
  text-align: center;
}

header nav {
  margin-top: .5rem;
}

header nav a {
  color: white;
  margin: 0 .5rem;
  text-decoration: none;
}

header nav a:hover {
  text-decoration: underline;
}

main {
  padding: 1rem;
  max-width: 800px;
  margin: auto;
}

section {
  margin-bottom: 2rem;
}

.project {
  border: 1px solid #ccc;
  padding: .75rem;
  margin: .5rem 0;
  background: #fff;
  cursor: pointer;
  transition: background 0.2s;
}

.project:hover {
  background: #e9f0ff;
}

form input, form textarea {
  width: 100%;
  padding: .5rem;
  margin: .4rem 0;
  border: 1px solid #ccc;
  border-radius: 4px;
}

form button {
  background: #092c6c;
  color: white;
  padding: .5rem 1rem;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

form button:hover {
  background: #042469;
}

footer {
  text-align: center;
  padding: 1rem;
  background: #0a2a66;
  color: rgb(255, 245, 245);
  font-size: .9rem;
}

-- Js --
// klik project -> alert sederhana
document.querySelectorAll(".project").forEach(item => {
  item.addEventListener("click", () => {
    alert("Kamu membuka: " + item.querySelector("h3").textContent);
  });
});

// form kirim
document.getElementById("contact-form").addEventListener("submit", function(e){
  e.preventDefault();
  document.getElementById("form-result").textContent =
    "Terima kasih, pesan terkirim (simulasi).";
  this.reset();
});
