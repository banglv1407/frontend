<template>
    <div class="vue-tempalte">
        <form>
            <h3>Sign In</h3>

            <div class="form-group">
                <label>Email address</label>
                <input type="email" class="form-control form-control-lg" />
            </div>

            <div class="form-group">
                <label>Password</label>
                <input type="password" class="form-control form-control-lg" />
            </div>

            <button type="submit" class="btn btn-dark btn-lg btn-block">Sign In</button>

            <p class="forgot-password text-right mt-2 mb-4">
                <router-link to="/forgot-password">Forgot password ?</router-link>
            </p>

            <!-- <div class="social-icons">
                <ul>
                    <li><a href="#"><i class="fa fa-google"></i></a></li>
                    <li><a href="#"><i class="fa fa-facebook"></i></a></li>
                    <li><a href="#"><i class="fa fa-twitter"></i></a></li>
                </ul>
            </div> -->
            <!-- <ul v-if="posts && posts.length">
                <li v-for="post of posts" v-bind:key="post">
                <p><strong>{{post.title}}</strong></p>
                <p>{{post.body}}</p>
                </li>
            </ul>
            <ul v-if="errors && errors.length">
                <li v-for="error of errors" v-bind:key="error">
                {{error.message}}
                </li>
            </ul> -->
        </form>
    </div>
</template>

<script>
import axios from 'axios';
    export default {
        data() {
            return {
                posts: [],
                errors: []
            }
        },
        created() {
            axios.get(`http://jsonplaceholder.typicode.com/posts`)
            .then(response => {
            this.posts = response.data
            })
            .catch(e => {
            this.errors.push(e)
            })
        }
    }
</script>