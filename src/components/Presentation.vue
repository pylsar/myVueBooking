<template>
    <div class="container">
        <section class="presentation">
            <presentation-top />
        </section>
    </div>
</template>
<script>
import PresentationTop from '@/components/PresentationTop'
export default{
    name: 'Presentation',
    components: {
        PresentationTop,
    }
}
</script>
<style lang="scss">
@import '../main.scss';
</style>