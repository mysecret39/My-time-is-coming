<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>🔒 الكود السري</title>
  <style>
    body {
      font-family: sans-serif;
      text-align: center;
      margin-top: 100px;
      background: #f8f8f8;
    }
    #secret {
      font-size: 1.5em;
      color: #444;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <h2>⏳ الكود محمي بالوقت</h2>
  <p id="secret">🚫 الكود غير متاح حتى 15/12/2025 16:00</p>

  <script>
    const unlockDate = new Date("2025-12-15T16:00:00");
    const now = new Date();

    // الكود مشفّر base64
    const encrypted = "NyA0IHggNiB4eCAxIDMgNSB4IDIgOSB4IDAgOCA2IDI="; // الكود الأصلي: 7 4 x 6 xx 1 3 5 x 2 9 x 0 8 6 2

    if (now >= unlockDate) {
      const secret = atob(encrypted);
      document.getElementById("secret").innerText = `✅ الكود: ${secret}`;
    }
  </script>
</body>
</html>