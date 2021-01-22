<template>
<div>
    <div>
        <input v-model="name" type="text" placeholder="Masukkan Nama">
        <input v-model="review_comment" type="text" placeholder="Masukkan Comment Reviews">
    </div>
    <div style="display: flex">
        <div v-for="(star, starId) in starsNumber" :key="starId" >
            <img @click="choosedRating = starId+1" v-if="starId+1 <= choosedRating" src="/images/star-filled.png" alt="" style="max-width: 30px">
            <img @click="choosedRating = starId+1" v-else src="/images/star-empty.png" alt="" style="max-width: 30px">
        </div>
    </div>
    <button @click="sendData">SUBMIT</button>
    <br>
    <br>
    <br>
    <div>
        <div v-for="(review, id) in dataReviews" :key="id" class="card">
            <div style="display: flex">
                <div v-for="(img, imgId) in review.image" :key="imgId">
                    <img :src="`data:image/png;base64, ${img.b64}`" :alt="img.originalName">
                </div>
            </div>
            <div style="display: flex">
                <div v-for="(star, starId) in starsNumber" :key="starId" >
                    <img v-if="starId+1 <= review.review_star" src="/images/star-filled.png" alt="" style="max-width: 30px">
                    <img v-else src="/images/star-empty.png" alt="" style="max-width: 30px">
                </div>
            </div>
            <div>{{ review.name }}</div>
            <div>{{ review.review_comment }}</div>
            <div>{{ convertToDate(review.updated_at) }}</div>
            <br>
            <br>
        </div>
    </div>
</div>
</template>

<script>
import moment from 'moment' 
import axios from 'axios'
export default {
    data() {
        return {
            starsNumber: 5,
            choosedRating: 0,
            dataReviews: [],
            name: '',
            review_comment: ''
        }
    },
    created() {
        moment.locale('id')
    },
    mounted() {
        this.getData()
    },  
    methods: {
        convertToDate(value) {
            return moment(value).format('LL')
        },
        getData() {
            axios.get('https://review-backend.herokuapp.com/api/v1/review')
            .then(res => {
                console.log(res.data);
                this.dataReviews = res.data.data
            })
            .catch(err => {
                console.log(err);
            })
        },
        sendData() {
            let payload = {
                name: this.name,
                review_star: this.choosedRating,
                review_comment: this.review_comment,
            }
            console.log(payload);
        }
    }
}
</script>

<style>
.card {
    padding: 16px;
    border: 1px solid black;
}
</style>