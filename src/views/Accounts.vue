<template>
  <v-container>
    <v-row>
      <v-col cols="12" md="10">
        <v-data-table :headers="headers" :items="items" @click:row="click"

        item-key="address"
        v-model="selected"
        show-select
        :single-select="true"

        ></v-data-table>
        <v-text-field v-model="address" label="Address"></v-text-field>
        <v-btn>Goto</v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts">
  import Vue from 'vue';
  import {
    web3Accounts,
    web3Enable,
    web3FromAddress,
    web3ListRpcProviders,
    web3UseRpcProvider
  } from '@polkadot/extension-dapp';

  export default Vue.extend({
    name: 'Accounts',

    data () {
      return {
        headers: [
          { text: 'Name', value: 'name' },
          { text: 'Address', value: 'address' },
        ],
        items: [] as {}[],
        address: '',
        selected: [] as {}[],
      }
    },

    async created() {
      const allInjected = await web3Enable('Acuity Browser');
      const allAccounts = await web3Accounts();
      for (let account of allAccounts) {
        this.items.push({
          address: account.address,
          name: account.meta.name,
        });
      }
      console.log(this.$activeAccount.get())
      this.selected = [{address: this.$activeAccount.get()}];
    },

    // define methods under the `methods` object
    methods: {
      click(event: any, row: any) {
        this.$activeAccount.set(event.address);
        console.log(this.$activeAccount.get())
        row.select(true);
      }
    }
  })
</script>
