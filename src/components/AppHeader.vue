<script>
export default {
    name: 'AppHeader'
}
</script>

<template>
    <header>
        <nav class="container d-flex justify-content-between align-items-center py-3">
            <ul class="list-unstyled d-flex gap-2">
                <li class="dropdown-center">
                    <a class=" text-light text-decoration-none" type="" data-bs-toggle="dropdown" aria-expanded="false">
                        Uomo
                    </a>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="#">T-shirt</a></li>
                        <li><a class="dropdown-item" href="#">Jeans</a></li>
                        <li><a class="dropdown-item" href="#">Felpe</a></li>
                    </ul>
                </li>
                <li class="dropdown-center">
                    <a class=" text-light text-decoration-none" type="" data-bs-toggle="dropdown" aria-expanded="false">
                        Donna
                    </a>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="#">T-shirt</a></li>
                        <li><a class="dropdown-item" href="#">Jeans</a></li>
                        <li><a class="dropdown-item" href="#">Felpe</a></li>
                    </ul>
                </li>
                <li class="dropdown-center">
                    <a class=" text-light text-decoration-none" type="" data-bs-toggle="dropdown" aria-expanded="false">
                        Bambino
                    </a>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="#">T-shirt</a></li>
                        <li><a class="dropdown-item" href="#">Jeans</a></li>
                        <li><a class="dropdown-item" href="#">Felpe</a></li>
                    </ul>
                </li>
            </ul>
            <div class="logo">
                <img height="30px" src="/public/images/boolean-logo.png" alt="logo boolean">
            </div>
            <div class="d-flex gap-3">
                <a href=""><i class="fa-regular fa-user text-light"></i></a>
                <a href=""><i class="fa-regular fa-heart text-light"></i></a>
                <a href=""><i class="fa-solid fa-bag-shopping text-light"></i></a>
            </div>
        </nav>
    </header>
</template>

<style></style>