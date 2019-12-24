<template>
    <div>
        order
        <OrderHeader></OrderHeader>
        <router-view></router-view>
        <NavFooter></NavFooter>
    </div>
</template>
<script>
    import OrderHeader from '../components/OrderHeader'
    import NavFooter from '../components/NavFooter'
    export default {
        name: 'oeder',
        components: {
            OrderHeader,
            NavFooter
        }
    }
</script>