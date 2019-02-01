<template>
  <v-container>
    <v-layout row>
      <v-flex xs6>
        <ClientList />
        <ClientList />
        <ClientList />
      </v-flex>

      <v-flex xs5 offset-xs1>
        <v-layout column>      
          <v-flex >
            <ClientList />
          </v-flex>

          <v-flex class="object-list">
            <ClientList />
          </v-flex>
        </v-layout>      

      </v-flex>

      
    </v-layout>      
  </v-container>
</template>

<script>
  import ClientList from '../components/ClientList'

  export default {
    components: {
      ClientList
    }
  }
</script>

<style>
  .object-list {
    margin-top: 32px;
  }
</style>
