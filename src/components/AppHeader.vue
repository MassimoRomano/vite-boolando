<script>
export default {
    name: 'AppHeader'
}
</script>

<template>
    <header>
        <nav class="container d-flex justify-content-between align-items-center py-3">
            <ul class="list-unstyled d-flex gap-2">
                <li><a href="">Uomo</a></li>
                <li class="dropdown-center">
                    <a class="btn" type="button" data-bs-toggle="dropdown" aria-expanded="false">
                        Uomo
                    </a>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="#">T-shirt</a></li>
                        <li><a class="dropdown-item" href="#">Jeans</a></li>
                        <li><a class="dropdown-item" href="#">Felpe</a></li>
                    </ul>
                </li>


                <li><a href="">Donna</a></li>
                <li><a href="">Bambino</a></li>
            </ul>
            <div class="logo">
                <img height="30px" src="/public/images/boolean-logo.png" alt="logo boolean">
            </div>


        </nav>
    </header>
</template>

<style></style>