<template>
    <table class="products">
        <thead>
            <tr>
                <th>Nazwa</th>
                <th>Cena</th>
                <th></th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="p of products" :key="p.id">
                <td>{{ p.name }}</td>
                <td>{{ p.price }}</td>
                <td><button>+</button></td>
            </tr>
        </tbody>
    </table>
</template>

<script setup>
  import products from '../data.js'
</script>

<style>
    table.products {
        width: 100%;
        border-collapse: collapse;
    }
    table.products td, table.products th {
        padding: 0.5rem;
        border-bottom: 1px solid black;
    }
    table.products td:nth-child(1) {
        width: 100%;
    }
    table.products td:nth-child(2) {
        text-align: right;
    }
    table.products td:nth-child(3) {
        text-align: center;
    }
</style>