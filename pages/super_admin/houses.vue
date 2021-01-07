<template>
    <div>
        <b-table-simple hover small caption-top responsive class="pt-3">

        <colgroup><col><col></colgroup>
        <colgroup><col><col><col></colgroup>
        <colgroup><col><col></colgroup>

        <b-thead head-variant="dark">
            <b-tr>
            <b-th>Название проекта</b-th>
            <b-th>Имя застройщика</b-th>
            <b-th>Цена постройки</b-th>
            <b-th>Кол-во квартир</b-th>
            <b-th></b-th>
            </b-tr>
        </b-thead>

        <b-tbody v-for="product in products" :key="product.id">

            <b-tr>

            <b-th rowspan="3">{{ product.name }}</b-th>
            <b-th>{{ product.user_name }}</b-th>
            <b-th>{{ product.sail_price }}</b-th>
            <b-th>{{ product.amount }}</b-th>

            <b-th>  
                <div class="text-right">

                    <b-button 
                        size="sm" 
                        variant="primary" 
                        class="mr-2" 
                        v-b-tooltip.hover.bottom 
                        title="Посмотреть проект"
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
                Кол-во проектов: <b>{{ products.length }}</b>
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
                    amount: "8 квартир"
                },
                {   
                    id: 2,
                    name: "Poluscana",
                    user_name: "Богданов Арсений Германович",
                    sail_price: "1,5 млрд",
                    amount: "124 квартиры"
                },
                {   
                    id: 3,
                    name: "Mddconsult",
                    user_name: "Авдеев Севастьян Всеволодович",
                    sail_price: "980 млн",
                    amount: "13 квартир"
                },
                {   
                    id: 4,
                    name: "IT Architect Janet",
                    user_name: "Рябов Абрам Проклович",
                    sail_price: "2 млрд",
                    amount: "223 квартир"
                },
                {   
                    id: 5,
                    name: "Jpentexcer",
                    user_name: "Морозов Эдуард Артёмович",
                    sail_price: "850 млн",
                    amount: "8 квартир"
                },
                {   
                    id: 6,
                    name: "Hankhard",
                    user_name: "Богданов Арсений Германович",
                    sail_price: "1,5 млрд",
                    amount: "124 квартиры"
                },
                {   
                    id: 7,
                    name: "Trtco",
                    user_name: "Авдеев Севастьян Всеволодович",
                    sail_price: "980 млн",
                    amount: "13 квартир"
                },
                {   
                    id: 8,
                    name: "Qitudi",
                    user_name: "Рябов Абрам Проклович",
                    sail_price: "3 млрд",
                    amount: "223 квартир"
                }
            ]
        }
    }
}
</script>