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
        filterKey: String
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
                </tr>
            </thead>
            <tbody>
                <tr v-for="(item,index) in items">
                    <th scope="row">{{index}}</th>
                    <td v-for="key in columns">
                        {{item[key]}}
                    </td>
                </tr>
            </tbody>
       </table>
       
    </main>
</template>