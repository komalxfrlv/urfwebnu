<template>
    <section class="container">
        <article class="product grid">
            <section>
                <header>
                    <h3>Brand</h3>
                    <h1>Homebrand Kitten</h1>
                    <b class="product-price">$39.95</b>
                </header>

                <button class="product-add">Add to cart</button>

                <button class="product-description-toggle" hidden>Read description</button>
                <div class="product-description">
                    <p>The word "kitten" derives from the Middle English word kitoun, which in turn came from the Old French
                        chitoun or cheton. Juvenile big cats are called "cubs" rather than kittens; either term (but usually
                        more commonly "kitten") may be used for the young of smaller wild felids, such as ocelots, caracals
                        and
                        lynxes.</p>

                    <p>A feline litter usually consists of two to five kittens born after a gestation lasting between 64 and
                        67
                        days, with an average length of 66 days, but from one to more than ten are known. Kittens emerge in
                        a
                        sac called the amnion, which is bitten off and eaten by the mother cat.</p>
                </div>
            </section>

            <section>
                <figure class="product-img">
                    <a href=""><img src="https://placekitten.com/g/650/650" alt="" height="600" width="600"></a>
                </figure>
                <ul class="product-thumbs grid">
                    <li><a href="https://placekitten.com/g/500/500"><img src="https://placekitten.com/g/500/500" alt=""
                                height="600" width="600"></a></li>
                    <li><a href="https://placekitten.com/g/400/400"><img src="https://placekitten.com/g/400/400" alt=""
                                height="600" width="600"></a></li>
                    <li><a href="https://placekitten.com/g/300/300"><img src="https://placekitten.com/g/300/300" alt=""
                                height="600" width="600"></a></li>
                </ul>
            </section>

        </article>

        <section class="product-related">
            <ul class="grid">
                <li>
                    <a href="" title="">
                        <figure><img src="https://placehold.it/600x400/ddd/ddd" alt="" /></figure>
                        <h4>Another item</h4>
                        <b>$24.95</b>
                    </a>
                </li>
                <li>
                    <a href="" title="">
                        <figure><img src="https://placehold.it/600x400/ddd/ddd" alt="" /></figure>
                        <h4>Another item</h4>
                        <b>$24.95</b>
                    </a>
                </li>
                <li>
                    <a href="" title="">
                        <figure><img src="https://placehold.it/600x400/ddd/ddd" alt="" /></figure>
                        <h4>Another item</h4>
                        <b>$24.95</b>
                    </a>
                </li>
            </ul>
        </section>
    </section>
</template>
<script>
export default {
    name: 'ProductDetail',
}
</script>
<style scoped lang="scss">
button {
    font-size: inherit;
}

/* Basic flex grid */
.grid {
    display: flex;
    flex-wrap: wrap;
    margin: -0.5em;

    >* {
        flex: 1 0 7em;
        margin: 0.5em;
    }
}

figure {
    margin: 0;

    img {
        height: inherit;
        width: 100%;
    }
}

/* Product layout - essential flexbox classes */
.product {
    margin-top: 20px;
    margin-bottom: 20px;
    align-items: center;

    section {
        p:first-child {
            margin-top: 0;
        }

        &:nth-child(0) {
            order: 2;
        }

        &:nth-child(1) {
            order: 1;
        }
    }

    .product-img {
        img {
            object-fit: cover;
        }
    }

    .product-thumbs {
        list-style: none;
        margin-top: 0.5rem;
        padding: 0;
        text-align: center;

        button {
            margin: 0;
        }

        img {
            height: inherit;
            width: 100%;
        }
    }

    button {
        all: inherit;
    }
}

button.product-description-toggle {
    display: none;
}

.product-related {
    ul {
        list-style: none;
        padding: 0;

        li {
            flex: 1 0 10em;

            * {
                margin: 0;
                font-weight: normal;
            }
        }
    }
}

/* Product styling - theme it here */
.product {

    h3,
    h1,
    .product-price {
        font-weight: normal;
        margin: 0;
    }

    h1 {
        font-size: 2rem;
        line-height: 1.3;
    }

    h3 {
        font-size: inherit;
        opacity: 0.6;
        line-height: 1;
    }

    .product-price {
        font-size: 1.25rem;
    }

    button {
        &.product-add {
            color: #fff;
            background: blue;
            display: inline-block;
            letter-spacing: 0.03em;
            line-height: 1;
            margin: 1rem 0;
            padding: 1rem;
            text-transform: uppercase;

            &:hover,
            &:focus {
                background-color: blue;
            }

            &:active {
                background-color: navy;
            }
        }
    }
}

.product-related {
    margin-top: 2rem;
    padding-top: 2rem;

    a {
        text-decoration: none;
        color: inherit;
    }

    h4 {
        font-size: 1.25rem;
    }
}


@media (max-width: 600px) {
    .product {
        display: block;
    }

    // Toggle description on mobile
    button.product-description-toggle {
        display: block;
        text-decoration: underline;
        margin-left: 0;

        &:focus+div,
        &:active+div {
            display: block;
        }
    }

    .product-description {
        display: none;

        &:focus {
            display: block;
        }
    }
}</style>