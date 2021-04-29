<template>
    <div class="container">
        <div class="row row-cols-1 row-cols-md-4 g-4">
            <div class="col">
                <Card imgSrc="https://thispersondoesnotexist.com/image" title="Card 1" text="Text for card 1" />
            </div>
            <div class="col">
                <Card imgSrc="https://thispersondoesnotexist.com/image" title="Card 2" text="Text for card 2" />
            </div>
            <div class="col">
                <Card imgSrc="https://thispersondoesnotexist.com/image" title="Card 3" text="Text for card 3" />
            </div>
            <div class="col">
                <Card imgSrc="https://thispersondoesnotexist.com/image" title="Card 4" text="Text for card 4" />          
            </div>
        </div>
    </div>
</template>

<script>
import Card from './Card'

export default {
    components: {
        Card
    }
}
</script>

<style>

</style>