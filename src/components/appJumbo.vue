<template>
    <div class="jumbo">
        <img src="@/assets/img/jumbotron.jpg" alt="Jumbotron">
    </div>
</template>

<script>
export default {
    name:'appJumbo',
}

</script>

<style lang="scss">

    .jumbo {
        height: 350px;
        
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top;
        } 
    }

</style>