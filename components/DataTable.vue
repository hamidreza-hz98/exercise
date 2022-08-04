<template>
    <div>
        <v-data-table dark :headers="headers" :items="items" :search="search" :items-per-page="5" class="elevation-1">
            <template v-slot:top>
                <v-text-field v-model="search" class="mx-4" append-icon="mdi-magnify" label="Search" single-line
                    hide-details>
                </v-text-field>
            </template>
            <template v-slot:body.append>
                <tr>
                    <td></td>
                    <td></td>
                    <td colspan="2"></td>
                    <td>
                        <v-text-field v-model="country" label="country...">
                        </v-text-field>
                    </td>
                </tr>
            </template>
        </v-data-table>
    </div>
</template>

<script>
export default {
    data() {
        return {
            search: '',
            country: '',
            items: [
                {
                    name: 'Hamidreza Hassanzadeh',
                    email: 'hamid@h.com',
                    phone: '0912124579',
                    address: 'ahfalj znnzx, qaiowi hcx aslhsa asl hcsaljc jashcaj',
                    country: 'Iran',
                },
                {
                    name: 'Daniel Azimi',
                    email: 'Daiel@d.com',
                    phone: '0978554931',
                    address: 'saamjaeu gfauiqui uoqwhcn qwuhuwq hksafh kasfhnvkqo ye',
                    country: 'UAE',
                },
                {
                    name: 'Ali Azimi',
                    email: 'Ali@gmai;.com',
                    phone: '097845653',
                    address: 'kasd kshad  khasd  khsad  sahkad k sak sahk sa dhkf lasj',
                    country: 'Gemany',
                },
                {
                    name: 'Adriana Nahaani',
                    email: 'adriana@gmail.com',
                    phone: '09125487864',
                    address: 'kas jjjs hhdbv hkaq[[o uqwh h jsadh uh dsf',
                    country: 'Turkey',
                },
                {
                    name: 'Maryam Aryadoust',
                    email: 'maryam@gmail.com',
                    phone: '0930221548',
                    address: 'ha jsaf nnv zuyfuiq fu uhdak hhv a;pq iiufwh  efhi',
                    country: 'USA',
                },
                {
                    name: 'Masoud Hosseini',
                    email: 'masoud@gmail.com',
                    phone: '0978654248',
                    address: 'hdacbahk hhsqoi czxbn qaqdhqwu jc jj bxbcqiou cajs',
                    country: 'Iran',
                },
                {
                    name: 'Melika Hariri',
                    email: 'melika@gmail.com',
                    phone: '091255478663',
                    address: 'tehran,a jjs c kkdqpo pvbkyque iei ackoqef',
                    country: 'China',
                },

            ],
        }
    },
    computed: {
        headers() {
            return [
                {
                    text: 'Name',
                    align: 'start',
                    value: 'name'
                },
                { text: 'E-mail', value: 'email' },
                { text: 'Phone No.', value: 'phone' },
                { text: 'Address', value: 'address' },
                {
                    text: 'Country',
                    value: 'country',
                    filter: value => {
                        if (!this.country) return true
                        //return ?????
                    },
                },
            ]
        }
    }
}
</script>

