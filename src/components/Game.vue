<template>
    <div id="connection" class="main__container">
      <!-- Yuqori qism -->
      <div class="main__top">
        <h1 class="main__title">O'yinlarim</h1>
      </div>
  
      <!-- Pastki qism (O'yin kartalari) -->
      <div class="main__bottom">
        <!-- Drum Game Card -->
        <div class="main__card">
          <img class="main__card-img" :src="require('@/assets/drum.png')" alt="Drum Game Image" />
          <h3 class="main__card-title">Doira O'yini</h3>
          <p class="main__card-text">Bu o'yin haqida: Unda doira chalsa bo'ladi. Uni bosganingizda turli xil tovushlar eshitiladi.</p>
          <button class="main__card-button" @click="goToDrumGame">O'yinni boshlash</button>
        </div>
  
        <!-- Dice Game Card -->
        <div class="main__card">
          <img class="main__card-img" :src="require('@/assets/dance.png')" alt="Dice Game Image" />
          <h3 class="main__card-title">Qur'a O'yini</h3>
          <p class="main__card-text">Bu o'yinda o'rtog'ingiz bilan o'ynang. Kimga katta son tushsa, u yutadi. Mazza qilib o'ynang!</p>
          <button class="main__card-button" @click="goToDiceGame">O'yinni boshlash</button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      goToDrumGame() {
        window.location.href = "https://drums-game.netlify.app";
      },
      goToDiceGame() {
        window.location.href = "https://diiceee.netlify.app";
      },
    },
  };
  </script>
  
  <style scoped>
  /* Asosiy konteyner */
  .main__container {
    padding: 20px;
    text-align: center;
    background-color: #f5f5f5;
  }
  
  /* Sarlavha */
  .main__title {
    font-size: 2em;
    color: #333;
    margin-bottom: 20px;
  }
  
  /* Kartalar uchun konteyner */
  .main__bottom {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
  }
  
  /* Karta dizayni */
  .main__card {
    width: 300px;
    background-color: #fff;
    border-radius: 15px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
    padding: 20px;
    text-align: center;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  
  .main__card:hover {
    transform: scale(1.05);
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
  }
  
  /* Karta rasmi */
  .main__card-img {
    width: 100px;
    height: 100px;
    object-fit: cover;
    margin-bottom: 15px;
    border-radius: 50%;
    transition: transform 0.3s ease;
  }
  
  .main__card-img:hover {
    transform: scale(1.1);
  }
  
  /* Karta sarlavhasi */
  .main__card-title {
    font-size: 1.5em;
    color: #3f51b5;
    margin-bottom: 10px;
  }
  
  /* Karta matni */
  .main__card-text {
    font-size: 1em;
    color: #555;
    margin-bottom: 20px;
    line-height: 1.5;
  }
  
  /* Karta tugmasi */
  .main__card-button {
    padding: 10px 20px;
    font-size: 1em;
    background-color: #42a5f5;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }
  
  .main__card-button:hover {
    background-color: #66bb6a;
  }
  
  /* Moslashuvchan dizayn */
  @media (max-width: 768px) {
    .main__bottom {
      gap: 15px;
    }
  
    .main__card {
      width: 90%;
    }
  }
  
  @media (max-width: 480px) {
    .main__title {
      font-size: 1.5em;
    }
  
    .main__card-title {
      font-size: 1.3em;
    }
  
    .main__card-text {
      font-size: 0.9em;
    }
  
    .main__card-button {
      font-size: 0.9em;
    }
  }
  </style>
  