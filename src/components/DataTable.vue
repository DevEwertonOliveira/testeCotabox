<template>
    <div>
        <table>
            <thead>
                <tr>
                    <th>firstName</th>
                    <th>lastName</th>
                    <th>Participation</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(entry, i) in participants" :key="i">
                    <td>{{ entry.firstName }}</td>
                    <td>{{ entry.lastName }}</td>
                    <td>{{ entry.participation }}</td>
                </tr>
                
            </tbody>
        </table>
    </div>
</template>

<script>
export default {
    name: "DataTable",
    props: ["participants"]
}
</script>


<style>
    
</style>