<template>
    <section class="projects-section">
        <v-container>
            <v-row>
                <v-col>
                    <h1>Projects</h1>
                </v-col>
            </v-row>
            <v-row class="justify-space-around m-10 mt-5">
                <v-card
                    v-for="project in projects"
                    :key="project.name"
                    class=""
                    max-width="300"
                >
                    <v-img
                    class="white--text align-end"
                    height="200px"
                    :src="project.image"
                    >
                    <v-card-title>{{project.name}}</v-card-title>
                    </v-img>

                    <v-card-text class="text--primary">
                    {{truncate(project.desc)}}
                    </v-card-text>

                    <v-card-actions>
                    <v-btn
                        color="orange"
                        text
                        href="project.github"
                    >
                        View Project
                    </v-btn>
                    </v-card-actions>
                </v-card>
            </v-row>
        </v-container>
    </section>
</template>

<script>
export default {
    data() {
        return {
            projects: [
                {
                    name: 'Vue.js',
                    desc: 'Vue project',
                    image: 'https://miro.medium.com/max/3920/1*oZqGznbYXJfBlvGp5gQlYQ.jpeg',
                    github: 'https://github.com/jakimovaivana'
                },
                {
                    name: 'Vanila Javascrpit',
                    desc: 'Vanila Javascropt Calculator App, Vanila Javascropt Calculator App, Vanila Javascropt Calculator AppVanila Javascropt Calculator AppVanila Javascropt Calculator App',
                    image: 'https://res.cloudinary.com/practicaldev/image/fetch/s--5nuecTWU--/c_imagga_scale,f_auto,fl_progressive,h_900,q_auto,w_1600/https://dev-to-uploads.s3.amazonaws.com/i/s46drgig8xugiyqt8zxp.png',
                    github: 'https://github.com/jakimovaivana'
                },
            ]
        }
    },
    methods: {
        truncate(str) {
            return str.length > 50 
            ?  str.slice(0,49) + '...'
            :  str
            // if(str.length > 50) {
            //     return str.slice(0,49) + '...'
            // }
            // return str
        }
    }
}
</script>

<style scoped>
.projects-section {
    background: #ffd563;
}
</style>