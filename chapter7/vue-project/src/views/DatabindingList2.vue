<template>
    <div>
        <table>
            <thead>
                <tr>
                    <td>제품명</td>
                    <td>가격</td>
                    <td>카테고리</td>
                    <td>배송료</td>
                </tr>
            </thead>
            <tbody>
                <tr :key="i" v-for="(product, i) in productList">
                    <td>{{product.product_name}}</td>
                    <td>{{product.price}}</td>
                    <td>{{product.category}}</td>
                    <td>{{product.delivery_price}}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>
<script>
/* eslint-disable */
    export default {
        data() {
            return {
                productList: []
            };
        },
        created() {
            this.getList();
        },
        methods: {
            async getList() {
                this.productList = await this.$api("https://54200929-5eb3-4774-8cc4-f29a7ea0d04f.mock.pstmn.io/list", "get");
            }
        }
    }
</script>
<style scoped>
    table {
        font-family: Arial, sans-serif;
        border-collapse: collapse;
        width: 100%;
    }
    td, th {
        border: 1px solid #dddddd;
        text-align: left;
        padding: 8px;
    }
</style>
