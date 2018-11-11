<template>
    <div>
        <Hero />
        <About />
        <Gallery />
        <Amenities />
        <Contact />
        <Testomonials />
    </div>
</template>

<style lang="scss" scoped>

</style>


<script>
import Hero from "~/components/Hero/Hero"
import About from "~/components/About/About"
import Amenities from "~/components/Amenities/Amenities"
import Gallery from "~/components/Gallery/Gallery"
import Contact from "~/components/Contact/Contact"
import Testomonials from "~/components/Testomonials/Testomonials"
export default {
    components: {
        Hero,
        About,
        Amenities,
        Gallery,
        Contact,
        Testomonials
    }
}
</script>
