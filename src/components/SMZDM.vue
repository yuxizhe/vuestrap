<template>
    <div>
        <table class="table table-hover">
            <thead>
            </thead>
            <tbody v-for="movie in movies">
                <tr>
                    <td>{{movie.title}}</td>
                    <!-- <td>{{user.message}}</td> -->
                </tr>
            </tbody>
        </table>
    </div>
</template>
<script>
import {
    firebaseData
} from './request.js'
//import {download} from './request.js'
//import Vue from "vue"

var usersRef = firebaseData('SMZDM');

export default {

    data() {
            return {
                movies: {}
            }
        },

        created() {
            var a = [];
            var aa;
            var _this = this;
            var keys;

            usersRef.on('value', snapshot => {
                a = snapshot.val();
                if (a == null) return;
                _this.movies = a;
                for (aa = 0; aa < a.length; aa++) {
                    _this.movies[aa].key = aa;
                    //console.log(_this.movies[aa])
                }
            });
        },

        methods: {

        }
}
</script>
<style>
</style>
