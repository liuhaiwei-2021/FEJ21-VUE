<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light shadow mb-4">
    <div class="container">
        <a class="navbar-brand" href="#">
            <img src="../assets/logo.png" alt="">
            {{ title }}
        </a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
            <ul v-if="signedIn" class="navbar-nav">
                <li class="nav-item">
                    <a class="nav-link active" aria-current="page" href="#">Home</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Features</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Pricing</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
                </li>
            </ul>
            <ul v-else class="navbar-nav">
                <li class="nav-item">
                    <a class="btn btn-secondary" aria-current="page" href="#">Sign In</a>
                </li>
            </ul>
        </div>
    </div>
  </nav>
</template>

<script>
export default {
    props: {
        title: String,
        signedIn: Boolean
    }
};
</script>

<style>
.navbar-brand img {
    height: 50px;
    margin-right: 1rem;
}
</style>