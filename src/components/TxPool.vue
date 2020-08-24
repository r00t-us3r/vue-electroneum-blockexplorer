<template>
    <div class="center">

        <h2 style="margin-bottom: 0px; font-size: 28px;">Transaction Pool</h2>
        <h4 style="font-size: 15px; font-weight: 100; margin-top: 0px">(Transactions waiting to be confirmed: 0 | Size: 0.00 kB)</h4>

        <table class="center">
            <tr>
                <th>Age [h:m:s]</th>
                <th>Transaction Hash</th>
                <th>Fee</th>
                <th>In/Out</th>
                <th>Tx Size [kB]</th>
            </tr>
            <TxItem v-bind:transaction="transaction" v-bind:key="transaction.hash" v-for="transaction in transactions" />
        </table>
    </div>
</template>

<script>
import axios from 'axios';
import TxItem from './TxItem';

export default {
    name: 'TxPool',
    components: {
        TxItem
    },
    data () {
        return {
            transactions: null
        }
    },
    created: function () {
       this.getTxPool();
    },
    methods: {
        getTxPool() {
            return [];
            // axios({
            //     method: 'get',
            //     url: 'http://localhost:26968/get_transaction_pool',
            //     withCredentials: false,
            //     headers:{'Access-Control-Allow-Headers': '*',Authorization:'Basic dXNlcm5hbWU6cGFzc3dvcmQ=',auth:{user:'useranme',pass:'password'}}
            // })
            // .then((res) => {
            //     console.log(res.data)
            // })
            // .catch((error) => {
            //     console.error(error)
            // });
        }
    }
}
</script>
