<template>
    <card title="Simple example">

        <date-picker v-model="date" class="hasTagDatepicker" :clearable="true" :tagData="[{1547411400: 5}, {1545510600:18}]" :disable="['1397/10/23']" @changeMonth="changeMonths($event)"></date-picker>
        <br/>
        <date-picker v-model="datetime" type="datetime"></date-picker>
        <br/>
        <date-picker v-model="time" type="time"></date-picker>
        <br/>
        <date-picker v-model="year" type="year" min="1350" max="1410"></date-picker>
        <br/>
        <date-picker v-model="month" type="month"></date-picker>

        <template slot="code">
            <highlight-code lang="html" v-pre>
                &lt;date-picker v-model="date" :clearable="true"&gt;&lt;/date-picker&gt;
            </highlight-code>
            <highlight-code lang="html" v-pre>
                &lt;date-picker v-model="datetime" type="datetime"&gt;&lt;/date-picker&gt;
            </highlight-code>
            <highlight-code lang="html" v-pre>
                &lt;date-picker v-model="time" type="time"&gt;&lt;/date-picker&gt;
            </highlight-code>
            <highlight-code lang="html" v-pre>
                &lt;date-picker v-model="year" type="year"&gt;&lt;/date-picker&gt;
            </highlight-code>
            <highlight-code lang="html" v-pre>
                &lt;date-picker v-model="month" type="month"&gt;&lt;/date-picker&gt;
            </highlight-code>
        </template>
    </card>
</template>

<script>
import utils from './../../picker/modules/utils';
const moment = utils.moment;
    export default {
        data() {
            return {
                date: '',
                time: '',
                datetime: '',
                year: '',
                month: '',
            }
        },
        methods:{
            changeMonths:function(_data){
                console.log(_data.format('jM'))
            }
        }
    }
</script>