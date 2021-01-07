<template>
    <div>
        <b-table-simple hover small caption-top responsive class="pt-3">

        <colgroup><col><col></colgroup>
        <colgroup><col><col><col></colgroup>
        <colgroup><col><col></colgroup>

        <b-thead head-variant="dark">
            <b-tr>
            <b-th>Имя застройщика</b-th>
            <b-th>Название фирмы</b-th>
            <b-th class="text-center">Общая цена построек</b-th>
            <b-th class="text-center">Кол-во проектов</b-th>
            <b-th></b-th>
            </b-tr>
        </b-thead>

        <b-tbody v-for="product in products" :key="product.id">

            <b-tr>

            <b-th>{{ product.user_name }}</b-th>
            <b-th rowspan="3">{{ product.name }}</b-th>
            <b-th class="text-center">{{ product.sail_price }}</b-th>
            <b-th class="text-center">{{ product.amount }}</b-th>

            <b-th>  
                <div class="text-right">

                    <b-button 
                        size="sm" 
                        variant="primary" 
                        class="mr-2" 
                        v-b-tooltip.hover.bottom 
                        title="Edit"
                    >
                        <b-icon icon="eye"></b-icon>
                    </b-button>

                </div>
            </b-th>   

            </b-tr>

        </b-tbody>

        <b-tfoot>
            <b-tr>
            <b-td colspan="7" variant="secondary" class="text-right">
                Кол-во товаров: <b>{{ products.length }}</b>
            </b-td>
            </b-tr>
        </b-tfoot>

        </b-table-simple>
    </div>
</template>

<script>
export default {
    data() {
        return {
            products: [
                {   
                    id: 1,
                    name: "GROSS AI",
                    user_name: "Морозов Эдуард Артёмович",
                    sail_price: "850 млн",
                    amount: "3"
                },
                {   
                    id: 2,
                    name: "Poluscana",
                    user_name: "Богданов Арсений Германович",
                    sail_price: "1,5 млрд",
                    amount: "5"
                },
                {   
                    id: 3,
                    name: "Mddconsult",
                    user_name: "Авдеев Севастьян Всеволодович",
                    sail_price: "980 млн",
                    amount: "4"
                },
                {   
                    id: 4,
                    name: "IT Architect Janet",
                    user_name: "Рябов Абрам Проклович",
                    sail_price: "2 млрд",
                    amount: "20"
                }
            ]
        }
    }
}
</script>