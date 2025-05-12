# Formygirlsalsa
Untuk kekasihku salsa, ❤️❤️


<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pesan Manis buat Cayankk</title>
  <style>
    body {
      background: #fff0f5;
      font-family: 'Comic Sans MS', cursive;
      text-align: center;
      padding: 50px;
      overflow: hidden;
      margin: 0;
      font-size: 20px; /* Ukuran font default */
    }
     h1 {
      color: #ff1493;
      font-size: 4vw; /* Responsif berdasarkan lebar layar */
      animation: fadeIn 2s ease-in-out forwards;
    }
 #gombal {
      font-size: 1.8em; /* Ukuran font lebih besar */
      color: #cc0066;
      margin: 30px auto;
      max-width: 700px;
      line-height: 2em;
      opacity: 0;
      transition: opacity 0.5s ease;
 } 
    #gombal.show {
      opacity: 1;
    }
    button {
      padding: 14px 28px;
      background: #ff69b4;
      border: none;
      border-radius: 12px;
      color: white;
      font-size: 1.2em;
      cursor: pointer;
      transition: 0.3s ease;
    }
 button:hover {
      background: #ff1493;
      transform: scale(1.1);
    }
 .heart {
      position: fixed;
      color: red;
      animation: floatUp 4s linear forwards;
      font-size: 24px;
      pointer-events: none;
    }
  @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }
 @keyframes floatUp {
      0% { transform: translateY(0); opacity: 1; }
      100% { transform: translateY(-100vh); opacity: 0; }
    }
@media (max-width: 600px) {
      h1 { font-size: 6vw; } /* Ukuran font lebih besar di perangkat mobile */
      #gombal { font-size: 1.5em; } /* Ukuran font lebih besar */
    }
  </style>
</head>
<body>

  <h1>Pesan Manis buat Cayankkuu</h1>
  <div id="gombal" class="show">
    Klik tombol di bawah yaa buat baca pesanku~
  </div>
  <br>
  <button id="btnGombal" onclick="tampilkanGombal()">Selanjutnya</button>

  <!-- Musik Otomatis -->
  <audio id="bgMusic" autoplay loop>
    <source src="https://example.com/surat-cinta-starla-tiktok.mp3" type="audio/mpeg">
    Browser kamu tidak mendukung audio HTML5.
  </audio>

  <audio id="btnSound" src="https://example.com/klik-sound.mp3" preload="auto"></audio>

  <script>
    const gombalan = [
      "Kamu tau kenapa bulan selalu mengitari bumi? Karena bulan tidak ingin jauh dari bumi...",
      "Dan begitu pula aku... yang tidak mau jauh dari cayankku ❤️❤️❤️",
      "Aku tak mau membuat cayankk sedih dan khawatir.",
      "Jadi cayankk jangan terlalu mikirin apa yang aku alami...",
      "aku tidak ingin cayankku yang cantik ini sedih❤️❤️❤️❤️",
      "aku hanya ingin cayankk selalu bahagia❤️❤️❤️",
      "Cukup cayankk selalu mencintaiku, itu udah lebih dari cukup.",
      "kita jalani seperti dulu ya, dimana tidak ada air mata yang tumpah",
      "hehe aku sangat sayang kepada cayankku salsa❤️❤️❤️",
      "i love you cayankku tercinta salsa❤️❤️❤️",
      "Terimakasih yaa selama ini udah nemenin aku, aku bersyukur banget punya kamu!"
    ];

    let index = 0;

    // Pengaturan volume musik
    const bgMusic = document.getElementById("bgMusic");
    bgMusic.volume = 0.7; // Menyetel volume menjadi sekitar 70%

    function tampilkanGombal() {
      const gombalDiv = document.getElementById("gombal");
      const tombol = document.getElementById("btnGombal");
      const btnSound = document.getElementById("btnSound");

      // Putar suara tombol
      btnSound.play();

      gombalDiv.classList.remove("show");

      setTimeout(() => {
        if (index < gombalan.length) {
          gombalDiv.innerText = gombalan[index];
          index++;
          munculinHati();
        } else {
          gombalDiv.innerText = "Udah selesai~ Tapi cintaku ke kamu nggak akan pernah selesai~\n\nSalam dari kekasihmu Aidilan atau Sijen.";
          tombol.style.display = "none";
        }
        gombalDiv.classList.add("show");
      }, 200);
    }

    function munculinHati() {
      const heart = document.createElement("div");
      heart.classList.add("heart");
      heart.style.left = Math.random() * 100 + "vw";
      heart.innerText = "❤️";
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 4000);
    }

    setInterval(munculinHati, 1500);

    // Autoplay trigger workaround
    document.addEventListener("click", function () {
      if (bgMusic.paused) {
        bgMusic.play();
      }
    });
  </script>

</body>
</html>
