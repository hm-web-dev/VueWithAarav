<script>
import Header from '../Header.vue'
import Footer from '../Footer.vue'

</script>

  <style scoped>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f4f4f4;
      color: #333;
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
    }

    main {
      background-color: #fff;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      padding: 20px;
      border-radius: 8px;
      text-align: center;
    }

    .match {
        display: flex;
      margin-bottom: 20px;
    }

    .team {
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 10px 0;
    }

    .team img {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      margin-right: 10px;
    }

    h3 {
      margin: 0;
      font-size: 1.2em;
    }

    p {
      color: #888;
      margin: 5px 0;
    }
  </style>

<template>
    <div class="match">
      <div class="team">
        <img src="https://yt3.googleusercontent.com/LZq29V-hPkycwJDyK5uCnwRy90f-K4hnsn3JVH9V0Y9jbVTMxyBDY6hP6fBhC6xpzI9Emr4W=s900-c-k-c0x00ffffff-no-rj" alt="Team 1 Logo">
        <h3>Tottenham</h3>
      </div>
      <div class="team">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/e/eb/Manchester_City_FC_badge.svg/800px-Manchester_City_FC_badge.svg.png" alt="Team 2 Logo">
        <h3>Manchester City</h3>
      </div>
      <p>Date: March 10, 2024</p>
      <p>Time: 7:00 PM</p>
    </div>

    <div class="match">
      <div class="team">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/7/7a/Manchester_United_FC_crest.svg/1200px-Manchester_United_FC_crest.svg.png" alt="Team 3 Logo">
        <h3>Manchester United</h3>
      </div>
      <div class="team">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/2/2a/Brentford_FC_crest.svg/1200px-Brentford_FC_crest.svg.png" alt="Team 4 Logo">
        <h3>Brentford</h3>
      </div>
      <p>Date: March 12, 2024</p>
      <p>Time: 3:30 PM</p>
    </div>
</template>
