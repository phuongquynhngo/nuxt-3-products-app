<template>
    <div>
<p>Product details for {{  id }}</p>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam quia magnam impedit minus repudiandae ad officiis quis eligendi facere quos, quod est recusandae enim omnis eaque. Molestias neque officia beatae.</p>
    </div>
</template>

<script setup>
const {id } = useRoute().params

definePageMeta({
    layout:'products'
});
</script>

<style scoped>

</style>