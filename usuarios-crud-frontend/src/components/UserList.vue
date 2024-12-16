<template>
  <v-container>
    <v-btn color="primary" @click="createUser">Adicionar Usuário</v-btn>
    <v-data-table :headers="headers" :items="users">
      <template v-slot:item.actions="{ item }">
        <v-btn color="blue" @click="editUser(item)">Editar</v-btn>
        <v-btn color="red" @click="deleteUser(item.id)">Deletar</v-btn>
      </template>
    </v-data-table>
  </v-container>
</template>

<script>
import axios from 'axios';

export default {
  data: () => ({
    headers: [
      { text: 'Nome', value: 'nome' },
      { text: 'CPF', value: 'cpf' },
      { text: 'Email', value: 'email' },
      { text: 'Ações', value: 'actions', sortable: false },
    ],
    users: [],
  }),
  methods: {
    fetchUsers() {
      axios.get('/api/users').then(response => {
        this.users = response.data;
      });
    },
    createUser() {
      // lógica para abrir o formulário
    },
    editUser(user) {
      // lógica para edição
    },
    deleteUser(id) {
      axios.delete(`/api/users/${id}`).then(() => {
        this.fetchUsers();
      });
    },
  },
  mounted() {
    this.fetchUsers();
  },
};
</script>
