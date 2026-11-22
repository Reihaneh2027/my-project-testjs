
<script setup>
import { ref } from 'vue'

// مقدار اولیه شمارنده
const count = ref(0)

// افزایش شمارنده
function increase() {
  count.value++
}

// کاهش شمارنده
function decrease() {
  count.value--
}

// صفر کردن شمارنده
function reset() {
  count.value = 0
}
</script>

<template>
  <div class="counter-container">
    <h1>شمارنده من</h1>

    <div class="counter-box">
      {{ count }}
    </div>

    <div class="buttons">
      <button @click="increase" class="increase">
        +
      </button>

      <button @click="decrease" class="decrease">
        -
      </button>

      <button @click="reset" class="reset">
        Reset
      </button>
    </div>

    <p>به شمارنده خوش آمدید!</p>
  </div>
</template>

<style scoped>
.counter-container {
  text-align: center;
  margin: 80px auto;
  padding: 30px;
  max-width: 400px;
  background: #FCE7F3;
  border-radius: 20px;
  font-family: Arial, sans-serif;
  box-shadow: 0 5px 20px #00000015;
}

h1 {
  color: #9D174D;
}

.counter-box {
  font-size: 55px;
  font-weight: bold;
  color: #DB2777;
  margin: 25px;
}

.buttons {
  display: flex;
  justify-content: center;
  gap: 12px;
}

button {
  padding: 12px 22px;
  border: none;
  border-radius: 10px;
  color: white;
  font-size: 20px;
  cursor: pointer;
}

.increase {
  background: #DB2777;
}

.decrease {
  background: #C084FC;
}

.reset {
  background: #BE8BA8;
  font-size: 15px;
}

button:hover {
  opacity: 0.8;
}

p {
  color: #831843; 
  margin-top: 25px;
}
</style>
