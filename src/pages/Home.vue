<template>
 <div>
    <navbar />
    <section class="home">

<div class="image">
    <img src="images/profile.png" alt="">
</div>

<div class="content">
    <h3>Hello, I'm Chinnapat Khemthong</h3>
    <span>"Nothing Happens Until Something Moves."</span>
    <p>Hello, My Name Is Chinnapat Khemthong. My Nickname Is Bom. Now I'm 19 Years Old. Now I'm Studying Multimedia & Entertainment Engineering At Bangkok University. I Lived With My Family In Nonthaburi. My Family Has 4 People, Father Mother Sister And Me. My Hobby Is Listening To Music And Play Game With My Friend. My Favorite Sport Is Football.</p>
    

</div>
<div class="content">
    <p> <span>name : </span> Chinnapat Khemthong </p>
    <p> <span>age : </span> 19 </p>
        <p> <span>email : </span> Chinnapat.khem@bumail.net </p>
            <p> <span>address : </span> Nontaburi, Thailand 11140 </p>
                        </div>

</section>
 </div>
</template>

<script>
import Navbar from '../components/Navbar.vue';
import axios from 'axios'


export default {
    components: { Navbar },
    methods: {
        async fetchExperience() {
            try {
                let res = await axios.get("https://633fc566e44b83bc73c0f545.mockapi.io/profile/v1/experiences")
                this.experience = res.data
            } catch (error) {
        
            }
        }
         
    },
    data() { 
        return { 
            experience: []
        }
    },
    beforeMount() {
        this.fetchExperience()
    }

            
    } 

</script>

<style>

</style>