<template>
    <form>
        <div class="mb-3">
            <label for="exampleInputEmail1" class="form-label">Email address</label>
            <input type="email" class="form-control" id="exampleInputEmail1" v-model="userData.email">
        </div>
        <div class="mb-3">
            <label for="exampleInputPassword1" class="form-label">Password</label>
            <input type="password" class="form-control" id="exampleInputPassword1" v-model="userData.password">
        </div>
        <div class="mb-3">
            <label for="exampleInputPassword1" class="form-label">Message</label>
            <textarea class="form-control" id="exampleInputPassword1" v-model="Message"></textarea>
        </div>
        <div class="mb-3">
            <label for="Reshi" class="me-3">
                Reshi <input type="checkbox" id="Reshi" v-model="FL_Name" value="Reshi">
            </label>
            <label for="kesh">
                kesh <input type="checkbox" id="kesh" v-model="FL_Name" value="kesh">
            </label>
        </div>
        <div class="mb-3">
            <label for="male" class="me-3">
                male <input type="radio" id="male" v-model="gender" value="male">
            </label>
            <label for="female">
                female <input type="radio" id="female" v-model="gender" value="female">
            </label>
        </div>
        <div class="mb-3">
            <p>Country</p>
            <select v-model="selectedCountry" class="form-select">
                <option v-for="country in countrys" :key="country">{{ country }}</option>
            </select>
        </div>
        <button type="submit" class="btn btn-primary" v-on:click.prevent="submited">Submit</button>
    </form>
    <div v-if="isSubmited">
        <h2>E-mail: {{ userData.email }}</h2>
        <h2>Password: {{ userData.password }}</h2>
        <p style="white-space: pre-line">Message: {{ Message }}</p>
        <ul>
            Full Name:
            <li v-for="names in FL_Name" :key="names">{{ names }}</li>
        </ul>
        <p>Gender: {{ gender }}</p>
        <p>Country: {{ selectedCountry }}</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            userData: {
                email: "",
                password: "",
            },
            Message: "",
            FL_Name: [],
            gender: "male",
            selectedCountry: "india",
            countrys: ['bd', 'india', 'us', 'uk'],
            isSubmited: false,
        }
    },
    methods: {
        submited() {
            this.isSubmited = true
        }
    }
}
</script>