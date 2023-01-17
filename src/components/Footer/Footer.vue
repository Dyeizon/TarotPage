<script></script>
<template>
    <footer>
        <p>Dyeizon Procopiuk</p>
        <div class="social">
            <a href="https://github.com/Dyeizon" target="_blank"><ion-icon name="logo-github" size="large"></ion-icon></a>
            <a href="https://www.linkedin.com/in/dyeizon-procopiuk-da-silva-2337bb145/" target="_blank"><ion-icon name="logo-linkedin" size="large"></ion-icon></a>
        </div>
    </footer>
</template>
<style scoped>
    footer {
        background-color: #7a36be;
        width: 100%;
        height: 50px;
        display: flex;
        justify-content: center;
        align-items: center;
        border-top: 1px solid rgba(0, 0, 0, 0.2);
        box-shadow: 0px 0px 5px 3px rgba(0, 0, 0, 0.2);
    }

    p {
        margin: 0;
        color: white;
    }

    .social {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    a {
        text-decoration: none;
        /* color: #f9d366; */
        color: white;
        display: flex;
        align-items: center;
    }

    a:hover {
        color: white;
    }

    a {
        margin-left: 10px;
    }
</style>