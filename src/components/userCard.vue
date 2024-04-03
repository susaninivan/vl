<template>
  <div>
    <div class="row g-0 bg-body-secondary position-relative">
      <div class="col-md-6 mb-md-0 p-md-4">
        <img src="../assets/istockphoto.jpg" class="w-100" alt="..." />
      </div>
      <div class="col-md-6 p-4 ps-md-0">
        <h5 class="mt-0">{{ getFullName }}</h5>
        <p>
          Другой экземпляр содержимого-заполнителя для этого другого
          настраиваемого компонента. Он предназначен для имитации того, как
          будет выглядеть реальный контент, и мы используем его здесь, чтобы
          придать компоненту немного тела и размера.
        </p>
        <a href="#" class="stretched-link">Иди куда-нибудь</a>
        <p>Количество Участников <strong>{{ users.length }}</strong></p>

        <ul>
          <li v-for="(user, index) in users" :key="index">
            {{ `${index + 1} ${getFullUsers(user)}` }}
          </li>
          
        </ul>
        <ul>
          <li v-for="(value, key, index) in users[0]" :key="index">
            {{ `${key}: ${value}` }}
          </li>
          
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "userCard",
  data() {
    return {
      firstName: "Иван1",
      secondName: "Борисович1",
      lastName: "Вел1",

      users: [
        {
          firstName: "Иван2",
          secondName: "Борисович2",
          lastName: "Вел2",
        },
        {
          firstName: "Иван3",
          secondName: "Борисович3",
          lastName: "Вел3",
        },
        {
          firstName: "Иван4",
          secondName: "Борисович4",
          lastName: "Вел4",
        },
      ],
    };
  },
  methods: {
    getFullUsers(user) {
      return `${user.firstName} ${user.secondName} ${user.lastName}`;
    },
  },
  computed: {
    getFullName() {
      // return this.firstName.toUpperCase() + " " + this.secondName.toUpperCase() + " " + this.lastName.toUpperCase()
      return `${this.firstName} ${this.secondName} ${this.lastName}`.toUpperCase();
    },
  },
};
</script>

<style>
</style>