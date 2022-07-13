<template>
    <v-app id="inspire">
        <v-app-bar app elevation="0">
            <v-subheader><h1 class="green--text">Lucien<span class="pink--text">.Portfolio</span></h1></v-subheader>
            <v-tabs center-active right background-color="transparent" active-class="active-tab">
                <v-tab href="#home">Accueil</v-tab>
                <v-tab href="#about">A propos</v-tab>
                <v-tab href="#portfolio">Portfolio</v-tab>
                <v-tab href="#blog">Blog</v-tab>
                <v-tab href="#contact">Contact</v-tab>
            </v-tabs>
            <v-btn large color="green" class="white--text ml-10">Envoyer moi des emails</v-btn>
        </v-app-bar>
        <v-main style="background-color: #F5F5F5">
            <section class="intro-section" id="home">
                <v-row class="align-center px-10" style="height: 690px">
                    <v-col lg="6" cols="6" class="pa-6 font-weight-bold py-16">
                        <h2 class="display-3">Developper<span class="green--text">web</span> & <span class="pink--text">Web</span>
                            Designer</h2>
                        <v-subheader>Lucien ANDRIAMIHAJA, se concentrer sur la création d'expériences émotionnelles.</v-subheader>
                        <br>
                        <br>
                        <v-btn large elevation="5" color="green" class="white--text mt-10 px-10 py-5">Engagement Moi</v-btn>
                        <v-btn large elevation="5" color="pink" class="white--text mt-10 ml-10 px-10 py-5">Contact
                        </v-btn>
                        <v-row class="mt-16">
                            <v-chip class="px-4 ma-3" color="primary">
                                <v-icon left size="20">mdi-facebook</v-icon>
                                Lucien Andriamihaja Burton
                            </v-chip>
                            <v-chip class="px-4 ma-3 white--text" color="#01ff56">
                                <v-icon left size="20">mdi-whatsapp</v-icon>
                                +261345105083
                            </v-chip>
                            <v-chip class="px-4 ma-3" color="info">
                                <v-icon left size="20">mdi-skype</v-icon>
                                live:lucienandriamihaja11
                            </v-chip>
                            <v-chip class="px-4 ma-3" color="dark">
                                <v-icon left size="20">mdi-github</v-icon>
                                lucgiovan2302
                            </v-chip>
                        </v-row>
                    </v-col>
                    <v-col lg="6" cols="6">
                        <v-img src="https://i.postimg.cc/K8PFKYwN/img14.png" width="900"></v-img>
                    </v-col>
                </v-row>
            </section>
            <section class="about-me" id="about">
                <v-img class="pa-10" height="400" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                       src="https://designshack.net/wp-content/uploads/Home-office.jpg">
                    <v-row justify="center" class="align-center">
                        <v-col lg="6" cols="6">
                            <v-card class="text-center pa-6 rounded-lg" color="#e1e0e0c9" elevation="6">
                                <v-card-subtitle class="green--text">QUI-SUIS JE</v-card-subtitle>
                                <h2 class="display-1 font-weight-regular">
                                    Développeur web & application web, Php, CMS (Wordpress, Drupal, Magento)  & UI/UX Designer, webdesigner..
                                </h2>
                                <v-btn large elevation="5" color="pink" class="white--text mt-10 px-10 py-5">Télécharger 
                                    Mon CV
                                <v-icon>mdi-download</v-icon>
                                </v-btn>
                            </v-card>
                        </v-col>
                        <v-col lg="6" cols="6">
                            <v-card class="pa-6 rounded-lg" color="#e1e0e0c9" elevation="6">
                                <div class="py-1" v-for="(item,index) in items" :key="index">
                                    <label>{{ item.title }}</label>
                                    <v-progress-linear
                                            :color="item.color"
                                            height="10"
                                            :value="item.value"
                                    ></v-progress-linear>
                                </div>
                            </v-card>
                        </v-col>
                    </v-row>
                </v-img>
            </section>
            <section class="education py-6">
                <v-container>
                    <h4 class="display-2 text-center">Education</h4>
                    <v-row class="py-8">
                        <v-col cols="12" lg="6">
                            <v-card class="pa-6 rounded-xl " elevation="5">
                                <div class="d-flex align-center justify-space-between">
                                    <div class="">
                                        <h2>Développeur web, application, génie logiciel</h2>
                                        <span>Février 2005 - Décembre 2009</span>
                                    </div>
                                    <a class="green--text">ENI Fianarantsoa <v-icon color="green">mdi-link</v-icon></a>
                                </div>
                                <v-card-text>
                                    créer des logiciel sur mesure. Avec des outils simples et efficaces, 
                                    développer des logiciels en quelques clics sous Windows que ce soit 
                                    à des fins personnelles, éducatives ou professionnelles.
                                </v-card-text>
                            </v-card>
                        </v-col>
                        <v-col cols="12" lg="6">
                            <v-card class="pa-6 rounded-xl " elevation="5">
                                <div class="d-flex align-center justify-space-between">
                                    <div class="">
                                        <h2>LTP BERAVINA FIANARANTSOA</h2>
                                        <span>2002 - 2005</span>
                                    </div>
                                    <a class="green--text">LTP BERAVINA FIANARANTSOA<v-icon color="green">mdi-link</v-icon></a>
                                </div>
                                <v-card-text>
                                    Formation technologie Générale Industrielle
                                </v-card-text>
                            </v-card>
                        </v-col>
                    </v-row>
                </v-container>
            </section>
            <section class="experiance py-6">
                <v-img class="pa-10" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                       src="https://designshack.net/wp-content/uploads/Home-office.jpg">
                    <v-container>
                        <h4 class="display-2 text-center">Experience</h4>
                        <v-timeline>
                            <v-timeline-item v-for="(exper,index) in experience" :key="index"
                                             :color="index % 2 === 0 ?'pink':'green'">
                                <v-card class="rounded-xl">
                                    <v-card-title :color="index % 2 === 0 ?'pink':'green'">
                                        {{exper.title}}
                                    </v-card-title>
                                    <v-card-text>
                                        <b>{{exper.date}}</b><br>
                                        <b>@{{exper.institute}}</b><br>
                                        {{exper.decription}}
                                    </v-card-text>
                                </v-card>
                            </v-timeline-item>
                        </v-timeline>
                    </v-container>
                </v-img>

            </section>
            <section id="anchor-name" class="portfolio">
                <h4 class="display-2 text-center">Portfolio</h4>
                <v-slide-group
                        class="pa-4"
                        active-class="success"
                        show-arrows
                >
                    <v-slide-item v-for="(slider,index) in sliders" :key="index">
                        <v-card height="250" width="250" class="mx-2">
                            <img height="100%" width="100%" :src="slider" alt="">
                        </v-card>
                    </v-slide-item>
                </v-slide-group>
            </section>
            <section class="contact-us pt-10">
                <v-img class="pt-10" gradient="to bottom, rgb(166 199 156), rgb(227 227 227 / 86%)" src="https://i.postimg.cc/NfRqYrQb/contact-us.png">
                    <v-container>
                        <h4 class="display-1 text-center mb-5">
                            Je suis Développeur et designer, basé à TANANARIVE. Actuellement, je travaille en local/freelance. 
                        </h4>
                        <v-divider />
                        <br>
                        <v-row>
                            <v-col cols="12" lg="6">
                                <v-card-title>VOUS AVEZ DES PROJETS ? CONTACT-MOI</v-card-title>
                                <v-form>
                                    <v-text-field label="Nom et prénom" />
                                    <v-text-field label="Email" />
                                    <v-text-field label="Sujet" />
                                    <v-textarea label="Message" />
                                    <v-btn large color="green" class="white--text">Envoyer message</v-btn>
                                </v-form>
                            </v-col>
                            <v-col cols="12" lg="3" offset="2">
                                <v-card-title>CONTACT</v-card-title>
                                <v-card-text>
                                    Lot CM 34 BIS MANDROSOA ILAFY, TANANARIVE, MADAGASCAR <br>
                                    +261 34 51 050 83 <br>
                                    lucien.peterson@gmail.com <br>
                                </v-card-text>
                            </v-col>
                        </v-row>
                    </v-container>
                    <v-footer class="mt-4">
                        <v-col
                                class="text-center"
                                cols="12"
                        >
                            <strong>Copyright ©{{ new Date().getFullYear() }} Tous droits réservés | Ceci est fait par
                                <a href="" class="green--text">Lucien ANDRIAMIHAJA</a>
                            </strong>
                        </v-col>
                    </v-footer>
                </v-img>
            </section>
        </v-main>
    </v-app>
</template>

<script>
    export default {
        name: 'App',

        data: () => ({
            drawer: null,
            items: [
                {title: 'HTML', value: 100, color: 'light-blue'},
                {title: 'CSS', value: 100, color: 'deep-orange'},
                {title: 'WORDPRESS', value: 95, color: 'deep-orange'},
                {title: 'Javascript', value: 70, color: 'light-green'},
                {title: 'Vuejs', value: 80, color: 'blue'},
                {title: 'Vuetify', value: 90, color: 'black'},
                {title: 'PHP', value: 100, color: 'red'},
            ],
            experience: [
                {
                    title: 'Infographiste',
                    date: 'Avril 2011 - Février 2013',
                    institute: 'SMARTONE ANKORONDRANO',
                    decription: 'Tâches efféctuées : Création des Affichages, brochures, magazines, flyers, plaquette graphiques,....,montage vidéo et audio : création mini publicité,Création des publications pour les réseaux sociaux, des offres d’emploi,Création des maquettes pour site web'
                },
                {
                    title: 'Développeur Freelance',
                    date: 'Avril 2013 - a nos jours',
                    institute: 'CODEUR.COM',
                    decription: 'Tâches efféctuées : Création des visuels pour les réseaux sociaux, création des flyers, brochures, des logos, x-banners, création des differentes, affiches, création maquette site web ,Création de site vitrine (Html,css, Wordpress, drupal, Joomla,...), Création et refonte site internet (Wordpress, php, mysql, sql, javascript,...), Création de site e-commerce (Prestashop, Woocommerce, Wordpress), application web, application mobile.Versoning (Github,. Gitlab,...)'
                },
                {
                    title: 'Technicien de maintenance informatique',
                    date: 'Octobre 2014 - Mars 2019',
                    institute: 'VIVETIC MADCOM ANDRAHARO',
                    decription: 'Accueil des demandes des utilisateurs suite à des dysfonctionnements.Enregistrement des incidents ou anomalies de fonctionnement signalés. Pré-qualification des dysfonctionnements pour orientation sur les supports ad hoc.Traitement ou déclenchement des actions de support correspondantes.Suivi des incidents : suivi du traitement des appels des clients.Exploitation de la base d’incidents : relances, consolidation, analyse de tendance.Demandes d’actions préventives de fond.Information des clients : alerte, information du client. Diffusion informations.'
                },
                {
                    title: 'Développeur web / Webdesigner',
                    date: 'AVRIL 2019 à Nos jours',
                    institute: 'STICA COSOURCING ANALAMAHINTSY',
                    decription: 'Tâches efféctuées : Création des visuels pour les réseaux sociaux, création des flyers, brochures, des logos, x-banners, création des differentes, affiches, création maquette site web ,Création de site vitrine (Html,css, Wordpress, drupal, Joomla,...), Création et refonte site internet (Wordpress, php, mysql, sql, javascript,...), Création de site e-commerce (Prestashop, Woocommerce, Wordpress), application web, application mobile.Versoning (Github,. Gitlab,...).'
                },
            ],
            sliders:[
                'https://i.postimg.cc/MHbNm6Q8/perfume-4.jpg',
                'https://i.postimg.cc/V5Pn9tCK/Affiche-boite.png',
                'https://i.postimg.cc/CzHRFfZQ/IMG-20210716-WA0013.jpg',
                'https://i.postimg.cc/Y4V9X6Vh/IMG-20210725-WA0005.jpg',
                'https://i.postimg.cc/DWm0djx9/IMG-20210725-WA0009.jpg',
                'https://i.postimg.cc/FY6JYkvg/upbeat-can.png',
                'https://i.postimg.cc/zHqysnw5/upbeatcan2.png',
                'https://i.postimg.cc/mPkHZNvg/Stand-Banner-Mockup-2.png',
                'https://i.postimg.cc/PP2d3bvT/Soda-Can-Mockup-3.png',
            ]
        }),
    }
</script>
<style>
    .v-tab.active-tab {
        color: #e91e63;
    }

    .v-tab.active-tab::before {
        background-color: #4caf50;
    }
</style>