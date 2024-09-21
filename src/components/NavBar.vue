<template>
    <v-app-bar app color="black" dark flast class="px-12">
        <v-btn>
            <v-icon color="red" left class="mr-2"> fas fa-signature</v-icon>NCCA
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn text @clik="scroll('home')" class="text-white"> Home</v-btn>
        <v-btn text @clik="scroll('about')" class="text-white"> About</v-btn>
        <v-btn text @clik="scroll('portfolio')" class="text-white">Portfolio</v-btn>
        <v-btn text @clik="scroll('services')" class="text-white"> Services</v-btn>
        <v-btn text @clik="scroll('biog')" class="text-white"> Biog</v-btn>
        <v-btn text @clik="scroll('blog')" class="text-white"> Blog</v-btn>
        <v-btn text @clik="scroll('contact')" class="text-white"> Contact</v-btn>
    </v-app-bar>
</template>

<script>

export default {
methods: {
    scroll(refName){ //refname es referencia
        const element =document.getElementById(refName)
        element.scrollIntoView({behavior: 'smooth'});
    }
}
}
</script>

<style>

</style>