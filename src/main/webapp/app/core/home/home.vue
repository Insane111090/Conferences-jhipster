<template>
    <div class="home row">
        <div class="col-md-3">
            <span class="hipster img-fluid rounded"></span>
        </div>
        <div class="col-md-9">
            <h1 class="display-4">Добро пожаловать на главную страницу <br>сервиса конференций!</h1>
            <p class="lead">Выберете одно из действий:</p>

            <div>
                <div class="alert alert-success" v-if="authenticated">
                    <span v-if="username">You are logged in as user "{{username}}"</span>
                </div>

                <div class="alert alert-warning" v-if="!authenticated">
                    <!--<span>Войти в систему </span>-->
                    <a class="alert-link" v-on:click="openLogin()">Войти в систему</a>
                </div>
                <div class="alert alert-warning" v-if="!authenticated">
                    <span><b>Нет аккаунта?</b><br></span>
                    <router-link class="alert-link" to="/register">Зарегестрироваться</router-link>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts" src="./home.component.ts">
</script>
<style scoped>
   /* .alert-warning{
        width: 1000px;
    }*/
    .alert{
        border-radius: 2.25rem;
    }
</style>
