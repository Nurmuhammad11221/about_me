<template>
  <div id="connection" class="main__container">
    <div class="main__top">
      <h1 class="main__title">Bog'lanish</h1>
    </div>

    <div class="main__bottom">
      <div class="main__bottom-item">
        <a
          class="main__link"
          target="_blank"
          href="https://yandex.uz/maps/10335/tashkent/?ll=69.279737%2C41.311151&z=12"
        >
          <img
            class="main__bottom-img"
            :src="require('@/assets/1.3.svg')"
            alt="Rasm tavsifi"
          />
          <p class="main__text">Toshkent shahri</p>
        </a>
      </div>

      <div class="main__bottom-item">
        <img
          class="main__bottom-img"
          :src="require('@/assets/1.4.svg')"
          alt="Rasm tavsifi"
        />
        <p>+998917987700</p> <!-- Telefon raqami -->
      </div>

      <div class="main__bottom-item">
        <a target="_blank" href="https://t.me/Anf_707">
          <img
            class="main__bottom-img"
            :src="require('@/assets/1.5.svg')"
            alt="Rasm tavsifi"
          /><br />
          707
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Contact",
};
</script>

<style scoped>
/* Umumiy sozlamalar */
.main__container {
  padding: 50px 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.main__title {
  text-align: center;
  color: blue;
  font-size: 38px;
  margin-bottom: 30px;
}

.main__bottom {
  display: grid;
  grid-template-columns: repeat(3, 1fr); /* 3 ta ustunli grid */
  gap: 30px; /* Elementlar orasidagi masofa */
  width: 80%; /* Karta kengligi */
  max-width: 1200px; /* Maksimal kenglik */
  margin: 0 auto; /* O'rtaga joylashtirish */
}

.main__bottom-item {
  background-color: white;
  box-shadow: 10px 1px 30px;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 40px; /* Karta ichki masofa */
  transition: transform 0.3s ease;
  height: 200px; /* Karta balandligi */
}

.main__bottom-item:hover {
  transform: scale(1.05);
}

.main__bottom-img {
  width: 70px; /* Kattaroq tasvir */
  height: 70px;
  margin-bottom: 15px;
  transition: transform 0.3s ease;
}

.main__bottom-img:hover {
  transform: scale(1.2);
}

.main__text {
  color: purple;
  margin-top: 10px;
  font-size: 18px; /* Katta matn */
}

/* Media query - Desktop versiyasi */
@media (min-width: 1024px) {
  .main__bottom {
    grid-template-columns: repeat(3, 1fr); /* 3 ta ustunli grid */
  }

  .main__bottom-item {
    padding: 50px; /* Kartalar orasidagi bo'shliq va kattalik */
    box-shadow: 15px 5px 40px rgba(0, 0, 0, 0.2);
    height: 250px; /* Katta balandlik */
  }

  .main__bottom-img {
    width: 90px; /* Tasvirlarni kattalashtirish */
    height: 90px;
  }

  .main__title {
    font-size: 48px; /* Katta ekran uchun sarlavha o'lchamini kattalashtirish */
  }
}

/* Media query - mobil versiya */
@media (max-width: 768px) {
  .main__bottom {
    grid-template-columns: repeat(1, 1fr); /* Mobilda bitta ustun */
    gap: 20px; /* Elementlar orasidagi bo'shliq */
    width: 90%; /* Kenglikni biroz kichiklashtirish */
  }

  .main__bottom-item {
    padding: 30px; /* Mobilda kichikroq kartalar */
    height: 180px; /* Kartalar balandligini kichiklashtirish */
  }

  .main__bottom-img {
    width: 60px; /* Tasvirlarni kichikroq qilish */
    height: 60px;
  }

  .main__title {
    font-size: 30px; /* Mobilda kichikroq sarlavha */
  }

  /* Telefon raqami kartasi o‘lchamini kichiklashtirish */
  .main__bottom-item p {
    font-size: 16px;
  }
}
</style>
