<template>
    <h1>Hello user id : {{ $route.params.id }}</h1>
</template>

<script>
export default {
     validate(data){ //nuxt function check data pass to this route
        return /^\d+$/.test(data.params.id)
    },
    layout: 'users'
}
</script>

<style>

</style>
