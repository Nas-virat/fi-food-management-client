<script>
export default{
    name: 'Table',
    props: {
        items: {
            type: Array,
            required: true
        },
        columns: {
            type: Array,
            required: true
        },
        moredetails: {
            type: Boolean,
            default: false
        },
        namepage:{
            type: String,
            required: false
        },
    },
}
</script>


<template>
    <main>
        <br/>
       <table class="table">
            <thead>
                <tr>
                    <th scope="col">#</th>
                    <th scope="col" v-for="key in columns">
                        {{key}}
                    </th>
                    <th scope="col" v-if="moredetails">More Details</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(item,index) in items">
                    <th scope="row">{{index}}</th>
                    <td v-for="key in columns">
                        {{item[key]}}
                    </td>
                    <td v-if="moredetails">
                        <router-link :to="{name: 'ProductView', params: {id: item.id}}">
                            <button class="btn">More Details</button>
                        </router-link>
                    </td>
                </tr>
            </tbody>
       </table>
       
    </main>
</template>