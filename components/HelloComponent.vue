
<template>
    <section class="hello-component background-image" :style="{ backgroundImage: `url(${backgroundImagePath})` }">
        <div class="container hello-text">
            <h1>Тестирование электроники</h1>
            <div class="hello-paragraph">
                <p>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore
                    et
                    dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
                    aliquip ex
                    ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore
                    eu fugiat
                    nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt
                    mollit
                    anim id est laborum.
                </p>
            </div>

            <div class="more-button">
                Узнать подробнее
            </div>
        </div>
    </section>
</template>

<script>
import backgroundImagePath from '~/assets/1529.jpg'
export default {
    data() {
        return { backgroundImagePath }
    }
}
</script>

<style scoped>
h1 {
    text-transform: uppercase;
    font-size: 48px;
}

p {
    margin-top: 18px;
    text-shadow: 3px 2px 2px rgb(0, 0, 0);
}

.hello-text {
    color: white;
    padding: 200px 0;
    text-align: center;
}
.hello-paragraph {
    padding: 0 38px;
    max-width: 800px;
    margin: 0 auto;
    font-size: 20px;
    font-weight: 300;
}

.more-button {
    margin: 65px auto;
    padding: 15px;
    max-width: 332px;
    background: none;
    border: 1px solid white;
    color: white;
    text-align: center;
    text-transform: uppercase;
    font-size: 22px;
    font-weight: 300;
    transition: 400ms;
    border-radius: 8px;
}

.more-button:hover {
    background: #ffffff;
    color: #212529;
}
</style>