<template>
    <nav class="navbar navbar-expand-lg">
        <div class="container-fluid">
        <router-link to="/" class="navbar-brand">Cocktails</router-link>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item">
                        <router-link to="/about" class="nav-link">
                            About-Us
                        </router-link>
                    </li>
                    <li class="nav-item">
                        <router-link to="/contacts" class="nav-link">
                            Contacts
                        </router-link>
                    </li>
                </ul>
                <!-- <div class="d-flex"> -->
                    <!-- <input class="form-control me-2" type="search" placeholder="Search by type..." aria-label="Search"> -->
                    <!-- <button class="btn" type="submit">Search</button> -->
                <!-- </div> -->
            </div>
        </div>
    </nav>
</template>
<script>
export default {
    name: 'AppHeader',
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
    .navbar {
        background: $background-color;
        font-family: 'Lora', serif;
        font-size: 1.5rem;
    }

    button {
        background: $button;

        &:hover {
            background: $button-hover;
        }
    }
</style>