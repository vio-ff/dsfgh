<template>
    <div :class="'armour-card ' + rare">
        <v-img 
            class="image-class ma-0 pa-0" 
            cover 
            :src="image"
            :width="300"
            aspect-ratio="1"
        ></v-img>
        <p class="card-title">
            {{ title + " (" + price + "$)" }}
        </p>
    </div>
</template>



<script setup lang="ts">

const props = defineProps({
  title: {
    type: String,
    default: null,
  },
  price: {
    type: Number,
    default: null,
  },
  rare: {
    type: String,
    default: null,
  },
  image: {
    type: String,
    default: null
  }

})

// const imgurl = "https://i.pinimg.com/originals/b8/d7/cb/b8d7cbd2cb64a6469e2f98f57f82cbdd.jpg"
// https://steamuserimages-a.akamaihd.net/ugc/2173609908980279956/49D9BB59532CCCAB1D4E0A89505115C1AE526ED1/?imw=5000&amp;imh=5000&amp;ima=fit&amp;impolicy=Letterbox&amp;imcolor=%23000000&amp;letterbox=false

// https://i.pinimg.com/736x/06/86/71/068671953deddfc6b6fb49c41878e1da.jpg

</script>

<style scoped>
.armour-card {
    background-color: #C4C4C4;
    border-radius: 24px;
    padding: 8px;
    margin: 16px;
    transition: 0.3s
}

.armour-card:hover {
    background-color: #E6E6E6;
    scale: 1.1;
}

.leg {
    outline: 4px solid #EB9318;
    background-color: #e9bc7d;
}

.leg:hover {
    outline: 6px solid #EB9318;
    background-color: #ead1b0;
}

.epic {
    outline: 4px solid #b318eb;
    background-color: #e4aaff;
}

.epic:hover {
    outline: 6px solid #b318eb;
    background-color: #f3d9ff;
}



.image-class {
    border-radius: 24px;
}


.image-class:hover {
    background-size: fill;
    background-position: top center;
}

.card-title {
    font-size: 2em;
}

</style>