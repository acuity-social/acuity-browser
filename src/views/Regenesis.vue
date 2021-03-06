<template>
  <v-container>
    <v-row>
      <v-col cols="12" md="10">
        <v-card>
          <v-card-text>
            <div class="text-h5 mb-1">Why did Acuity have a Regenesis?</div>
            <div class="body-2 mb-4">Acuity is a fully decentralized social media platform that has been in development for six years, but it began as an independent Ethereum blockchain called MIX. The project has now migrated to a new <a target="_blank" href="https://polkadot.network/">Polkadot</a> blockchain with native cryptocurrency ACU. This has a number of advantages:
            </div>
            <div class="ml-4">
              <div class="text-h6 mb-1">Blockchain Interoperability</div>
              <div class="body-2 mb-4">Acuity is being built with Polkadot's <a target="_blank" href="https://www.substrate.io/">Substrate</a> blockchain construction kit. Chains built with this technology can connect together for improved block finality, decentralized token exchange and message passing.</div>
              <div class="text-h6 mb-1">Cheaper Transactions</div>
              <div class="body-2 mb-4">Being an independent Ethereum blockchain, MIX has a lot of capacity and cheap transactions. However, as we have seen on the Ethereum mainnet, transactions can get expensive very easily once transaction throughput increases. Proof-of-stake blockchains built with Substrate have much greater capacity than a PoW Ethereum blockchain. This is very important for Acuity because it uses on-chain transactions extensively when publishing content.</div>
              <div class="text-h6 mb-1">Massively Extensible</div>
              <div class="body-2 mb-4">Substrate has a system called <a target="_blank" href="https://substrate.dev/docs/en/knowledgebase/runtime/frame">FRAME</a> that provides many pluggable pallets that can easily add functionality to the blockchain.</div>
              <div class="text-h6 mb-1">Forkless Upgrades</div>
              <div class="body-2 mb-4">Using the Democracy pallet the Acuity community can agree when to upgrade the blockchain and this will happen automatically without node software having to be manually upgraded.</div>
              <div class="text-h6 mb-1">Reduced Supply Inflation</div>
              <div class="body-2 mb-4">30k MIX was mined everyday, inflating the MIX supply by ~14% per year. After regenesis the ACU supply inflates due to staking rewards by only ~10% per year.</div>
              <div class="text-h6 mb-1">WASM Smart Contracts</div>
              <div class="body-2 mb-4">The Substrate <a target="_blank" href="https://www.substrate.io/kb/smart-contracts">Contracts</a> pallet uses a WASM VM instead of the Ethereum VM. This greatly increases processing capacity.</div>
            </div>
            <div class="text-h5 mb-1">How did the migration happen?</div>
            <div class="body-2 mb-4">On 1st September 2020 at 5am UTC a snapshot of all balances on MIX blockchain occurred. On 3rd September the new Acuity blockchain launched. All MIX holders have be allocated the same amount of ACU as they held in MIX at the time of the snapshot.</div>
            <div class="body-2 mb-4">ACU can be claimed by signing a message from a MIX address using MyCrypto, MyEtherWallet, Metamask or Coinomi. Arun Goutham has published some excellent <a target="_blank" href="https://www.youtube.com/channel/UCbAIcinwIejHlpMAYHEA9dg">tutorials</a> on his YouTube channel.</div>
            <div class="text-h5 mb-1">Was any extra ACU be created during Regenesis?</div>
            <div class="body-2 mb-4">No. Only ACU that can be claimed 1:1 from MIX balances will come into existence during Regenesis.</div>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts">
  import Vue from 'vue'

  export default Vue.extend({
    name: 'Regenesis',

    data: () => ({
    }),
  })
</script>
