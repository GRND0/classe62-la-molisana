<template>
  <footer class="footer">
    <div class="container footer__container">
        <div class="footer__col">
            <img class="footer__img" src="../assets/img/la-molisana-logo.png" alt="">
        </div>
        <div class="footer__col">
            <h3>Pastificio</h3>
            <ul class="footer__menu">
                <li>
                    <a href="">Footer link</a>
                </li>
                <li>
                    <a href="">Footer link</a>
                </li>
                <li>
                    <a href="">Footer link</a>
                </li>
                <li>
                    <a href="">Footer link</a>
                </li>
                <li>
                    <a href="">Footer link</a>
                </li>
            </ul>
        </div>
        <div class="footer__col">
            <h3>Prodotti</h3>
             <ul class="footer__menu">
                <li>
                    <a href="">Footer link</a>
                </li>
                <li>
                    <a href="">Footer link</a>
                </li>
                <li>
                    <a href="">Footer link</a>
                </li>
                <li>
                    <a href="">Footer link</a>
                </li>
                <li>
                    <a href="">Footer link</a>
                </li>
            </ul>
        </div>
    </div>
  </footer>
</template>

<script>
export default {
    name: "AppFooter"
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.footer {
    &__container {
        display: flex;
    } 

    &__col {
        width: calc(100% / 3);
        padding: 3rem 1rem;

        h3 {
            color: $brand-primary-color;
            text-transform: uppercase;
            margin-bottom: 1rem;
        }
    }

    &__img {
        width: 70%;
    }

    &__menu {

        li {
            a {
                color: $text-color;
                font-weight: 300;
                font-size: .8rem;
            }
        }
    }
}

</style>