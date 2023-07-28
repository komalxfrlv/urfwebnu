<template>
    <section class="contacts">
        <h1>Контакты</h1>
        <div class="container">
            <div class="row">
                <div class="col">
                    <div class="contacts-icons">
                        <font-awesome-icon :icon="['fas', 'phone-volume']" />
                    </div>
                    <h3>Телефон</h3>
                    <span class="phone-number">8 (982) 600-72-33</span>
                </div>
                <div class="col">
                    <div class="contacts-icons">
                        <font-awesome-icon :icon="['fas', 'envelope-open-text']" />
                    </div>
                    <h3>Почта</h3>
                    <span class="phone-number">product@urfu.ru</span>
                </div>
                <div class="col">
                    <div class="contacts-icons">
                        <font-awesome-icon :icon="['fas', 'map-location-dot']" />
                    </div>
                    <h3>Адрес</h3>
                    <span class="phone-number">Екатеринбург, ул. Мира, д. 32 </span>
                </div>
            </div>
        </div>
        <h2>Карта</h2>
        <iframe
            src="https://yandex.ru/map-widget/v1/?um=constructor%3A870f0369d70f9ad8ab09fd40c55005d449ed579508bfeb7a0ab6e7e3584651f4&amp;source=constructor"
            width="100%" height="500" frameborder="0">
        </iframe>
    </section>
</template>
<style lang="scss" scoped>
.contacts {
    h1 {
        margin-top: 90px;
        margin-bottom: 90px;
        text-align: center;
        font-weight: 300;
    }

    h2 {
        text-align: center;
        font-weight: 300;
        margin-bottom: 40px;
    }

    .container {
        margin-bottom: 90px;
        .row {
            .col {
                text-align: center;
                .contacts-icons {
                    font-size: 36px;
                }

                h3 {
                    font-weight: 300;
                }
            }
        }
    }
}
</style>