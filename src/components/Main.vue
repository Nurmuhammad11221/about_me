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
        <p>+998917987700</p>
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
export default {};
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
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); /* 200px dan kichik bo'lmagan elementlar */
  gap: 20px; /* Elementlar orasidagi masofa */
  width: 100%;
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
  padding: 20px;
  transition: transform 0.3s ease;
}

.main__bottom-item:hover {
  transform: scale(1.05);
}

.main__bottom-img {
  width: 50px;
  height: 50px;
  margin-bottom: 10px;
  transition: transform 0.3s ease;
}

.main__bottom-img:hover {
  transform: scale(1.2);
}

.main__button {
  height: 50px;
  background-color: blue;
  color: white;
  border-radius: 15px;
  width: 100px;
  border: 1px solid blue;
  transition: 0.2s;
}

.main__button:hover {
  background-color: black;
  box-shadow: 10px 10px 10px 10px;
  border: 1px solid black;
}

.main__text {
  color: purple;
  margin-top: 10px;
}
</style>

