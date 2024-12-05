<template>
  <div id="whatdid" class="container">
    <h1 class="page-title">Men qilgan saytlar</h1>

    <div class="card-container">
      <div 
        class="card" 
        @click="openLink('https://nurmuhammad11.pythonanywhere.com/')"
      >
        <div class="image-container">
          <img class="image" :src="require('@/assets/todo.jpg')" alt="Todo Website" />
        </div>
        <div class="content">
          <h2 class="title">Todo Sayt</h2>
          <p class="description">
            Ushbu sayt vazifalar ro'yxatini boshqarishga yordam beradi. Vazifalarni qo'shish, 
            o'chirish va bajarilganini belgilash imkoniyatini beradi.
          </p>
          <button class="btn" @click.stop="openLink('https://nurmuhammad11.pythonanywhere.com/')">Batafsil</button>
        </div>
      </div>

      <div 
        class="card" 
        @click="openLink('https://707anf.netlify.app/')"
      >
        <div class="image-container">
          <img class="image" :src="require('@/assets/portfolio.jpg')" alt="Portfolio Website" />
        </div>
        <div class="content">
          <h2 class="title">Portfolio Sayt</h2>
          <p class="description">
            Ushbu sayt shaxsiy portfolio sifatida yaratilgan bo'lib, mijozlar loyihalari 
            va tajribalarini taqdim etish uchun mo'ljallangan.
          </p>
          <button class="btn" @click.stop="openLink('https://707anf.netlify.app/')">Batafsil</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    openLink(url) {
      window.open(url, '_blank');
    }
  }
};
</script>

<style scoped>
.page-title {
  text-align: center;
  font-size: 2.5em;
  margin-bottom: 40px;
  color: #000;
}

.card-container {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
}

.card {
  width: 100%;
  max-width: 400px;
  height: 550px;
  background: #ffffff;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  cursor: pointer;
  text-align: center;
  margin-bottom: 20px;
}

.card:hover {
  transform: scale(1.05);
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
}

.image-container {
  width: 100%;
  height: 250px;
  overflow: hidden;
  position: relative;
}

.image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
}

.image-container:hover .image {
  transform: scale(1.1);
}

.content {
  padding: 20px;
  text-align: center;
  height: 250px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.title {
  font-size: 1.8em;
  color: #333;
  margin: 10px 0;
}

.description {
  font-size: 1em;
  line-height: 1.6;
  color: #000;
  margin-bottom: 20px;
}

.btn {
  background-color: #007BFF;
  color: white;
  font-size: 1.2em;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
  text-decoration: none;
  align-self: center;
  margin-top: 20px;
}

.btn:hover {
  background-color: #0056b3;
}

@media (max-width: 768px) {
  .card-container {
    flex-direction: column;
    align-items: center;
  }

  .card {
    max-width: 90%;
  }

  .page-title {
    font-size: 2em;
  }
} 
</style>
