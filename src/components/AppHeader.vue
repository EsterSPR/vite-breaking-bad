<script>
export default {
    
}
</script>

<template lang="">
    <header>
        <img src="http://vignette1.wikia.nocookie.net/yugiohenespanol/images/a/aa/Yugioh_anime_logo.jpg/revision/latest?cb=20130310042737&path-prefix=es" alt="logo">
        <h1>Yu-Gi-Oh Api</h1>
    </header>
</template>

<style lang="scss" scoped>

    @use '../styles/partials/variables' as *;
    header{
        padding: 10px 30px;
        display: flex;
        align-items: center;
        background-color: $ygo-white;
        width: 100vw;

        img[alt="logo"]{
            height: 30px;
            margin-right: 10px;
        }

        h1{
            font-size: 30pt;
            font-weight: 400;
        }
    }
</style>