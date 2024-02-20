<script>
export default {
    data() {
        return {
            description: "Made in Bergen.",
            copy: "This is copy. It's a string. Paragraph paragraph paragraph.",
        }
    }
}
</script>

<template>
    <div class="backgroundWithImage">
        <div class="description">
            <p>Careers</p>
            <h1>{{ description }}</h1>
        </div>
    </div>
    <div>
        {{ copy }}
    </div>
</template>

<style scoped>
.backgroundWithImage {
    height: calc(-100px + 100vh);
    background-size: 100%;
    background-repeat: no-repeat;
    background-image: url(https://cdn.sanity.io/images/n5wk68wz/production/595bc21a01381bc136773f148879fe9e84779e69-5760x3240.webp);
}

.description {
    color: var(--color-heading);
    display: flex;
    flex-direction: column;
    -webkit-box-pack: center;
    justify-content: center;
    max-width: min(80%, 940px);
    height: calc(-150px + 100vh);
}
.description * {
    margin: 0;
}
</style>