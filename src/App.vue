<script setup lang="ts">
import { ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue'
import ArmourCard from './components/ArmourCard.vue'

let showHeaders = ref<boolean>(true)

//  объявление переменных
let dsf = 12
let sdf = 11
let dsd = dsf + sdf
dsd = dsd + 2
window.console.log(dsd)


//  условия
let a = 1
let b = 2

if (a > b + 22) {
  window.console.log('dsd больше sdf')
} else {
  window.console.log('dsd меньше sdf')
}


// a ++
// // a = a + 1
// window.console.log(a)

// циклы
window.console.log("вывод цикла for")
for (let i = 0; i < 10; i++) {
  window.console.log(i)
}

window.console.log("вывод цикла while")
let i = 100
while (i >= 2) {
  i = i / 2
  window.console.log(i)
}



let asd = null
window.console.log(asd)

// null -> false
// undefined -> false
// number -> 0: false, (все остальное): true
// str -> '': false, (все остальное): true
window.console.log("конвертация в логическую пременную")

asd = null
if (asd) {
  window.console.log("тут лежит: " + asd)
}
// undefined -> false
asd = undefined
if (asd) {
  window.console.log("тут лежит: " + asd)
}
// number -> 0: false, (все остальное): true
asd = 0
if (asd) {
  window.console.log("тут лежит: " + asd)
}
asd = 1
if (asd) {
  window.console.log("тут лежит: " + asd)
}
// str -> '': false, (все остальное): true
asd = ''
if (asd) {
  window.console.log("тут лежит: " + asd)
}
asd = 'some text'
if (asd) {
  window.console.log("тут лежит: " + asd)
}

let header = 'арпрарп'


// list - лист (аля массив)
window.console.log("листы")
let some_list = [123, 1233, 123, 12423, 232323, 23344]
window.console.log(some_list)
window.console.log(some_list[4])
some_list.push(69)
window.console.log(some_list)

some_list.forEach((i) => {
  window.console.log(i)
})


// объекты
window.console.log("объекты")
let car = {
  "maxSpeed": 100,
  "seats": 4,
  "bar": [2, 2.1, 1.9, 1],
}
window.console.log(car.bar[1])
window.console.log(car.seats)
window.console.log(car.sdafasdf)
car.seats = 2
window.console.log(car.seats)


let cars = ref(
  [
    {
      "brand": "porshe",
      "price": "10000$",
      "customers": 12,
    },
    {
      "brand": "toyota",
      "price": "100000$",
      "customers": 100,
    },
    {
      "brand": "bently",
      "price": "100000000$",
      "customers": 1,
    }
  ]
)



// function incrementCustomers(carNumber) {
//   cars.value[carNumber].customers++
// }

// incrementCustomers(1)
// incrementCustomers(2)
// incrementCustomers(0)
// incrementCustomers(2)
// incrementCustomers(2)


// function incrementCustomers(car) {
//   car.customers++
// }

// function addCar() {
//   cars.value.push(
//     {
//       "brand": "lada",
//       "price": "-100$",
//       "customers": 100000000,
//     }
//   )
// }

</script>

<template>
  <v-row>
    <ArmourCard 
      title="Легендарка" 
      price="9000" 
      rare="leg" 
      image="https://i.pinimg.com/originals/b8/d7/cb/b8d7cbd2cb64a6469e2f98f57f82cbdd.jpg"
    ></ArmourCard>
    <ArmourCard 
      title="Рарка" 
      price="700" 
      rare="epic" 
      image="https://steamuserimages-a.akamaihd.net/ugc/2173609908980279956/49D9BB59532CCCAB1D4E0A89505115C1AE526ED1/?imw=5000&amp;imh=5000&amp;ima=fit&amp;impolicy=Letterbox&amp;imcolor=%23000000&amp;letterbox=false"
    ></ArmourCard>
    <ArmourCard 
      title="Обычная" 
      price="70"
      image="https://i.pinimg.com/originals/7f/e2/c3/7fe2c36b3b66608fecf9ced51ef6b172.jpg"
    ></ArmourCard>

  </v-row>
  <!-- <p v-for="i in cars">
    {{ i }}
  </p> -->

  <!-- <div class="car-card padding-margine" v-for="i in cars">
    <p class="padding-margine">
      {{ i.brand }}
    </p>
    <p>
      {{ i.price }}
    </p>
    <p>
      {{ "Покупателей: " + i.customers }}
    </p>
    {{ "Цена:" + i.price }}
    <p>
      <v-btn @click="incrementCustomers(i)">Новый покупатель</v-btn>
    </p>
  </div>
  <p>
    <v-btn @click="addCar()">Новая машина</v-btn>
  </p> -->

  <!-- <h1 v-if="header">
    {{ "header: " + header }}
  </h1>
  <h1 v-if="!header">
    {{ "header еще не подгрузиился" }}
  </h1>
  <v-btn v-for="i in some_list">
    {{ 'Кнопка ' + i }}
  </v-btn>
  {{ showHeaders }}
  {{ dsd }}
  <h1 
    v-if="showHeaders" 
    class="h1"
  >asdasd</h1>
  <v-btn @click="showHeaders = !showHeaders">
    Button
  </v-btn> -->
  <!-- <HelloWorld msg="Vite + Vue" /> -->
</template>

<style scoped>
.car-card {
  background-color: rgba(102, 102, 62, 0.565);
  border-radius: 5px;
}

.padding-margine {
  padding: 5px;
  margin: 30px;
}
</style>
