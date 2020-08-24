<template>
    <div class="center">
        <table class="center">
            <tr>
                <td>Block Height</td>
                <td>Age [h:m:s]</td>
                <td>Size [kB]</td>
                <td>Transaction Hash</td>
                <td>Fee</td>
                <td>Outputs</td>
                <td>In/Out</td>
                <td>Tx Size [kB]</td>
                <td></td>
            </tr>
            <Block v-bind:block="block" v-bind:key="block.height" v-for="block in blocks" />
        </table>
    </div>
</template>

<script>
import Block from './Block';
export default {
    name: 'Blocks',
    components: {
        Block
    },
    data () {
        return {
            blocks: [
                {
                    height: 1,
                    age: '00:00:01',
                    size: 1.21,
                    txHash: 'hasdhjqwoeoiqwe',
                    fee: 1.21,
                    outputs: 500,
                    out: 1,
                    in: 1,
                    txSize: 5.15,
                    txExtra: '<div title="Top Up" class=""></div>'
                }
            ]
        }
    }
}
</script>
