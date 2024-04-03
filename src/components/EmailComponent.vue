<template>
  <div class="app4">
    <form>
      <div class="mb-3">
        <label for="exampleInputEmail1" class="form-label"
          >Адрес электронной почты</label
        >
        <input
          v-bind:value="email"
          v-on:input="emailInput($event.target.value)"
          type="email"
          class="form-control"
          id="exampleInputEmail1"
          aria-describedby="emailHelp"
        />
        {{ email }}
        <!-- Краткая запись -->
        <!-- v-on:input="emailInput" = @input="emailInput"  v-on – это атрибут, который добавляется к элементам DOM, чтобы прослушивать события в VueJS. -->
        <!-- v-bind:value="email" = :input="emailInput"  для динамического связывания данных с определенными атрибутами во vue.js используется директива v-bind, которая имеет сокращение “:”.-->
        <!-- :value="searchText" @input="searchText=$event.target.value"
   равно записи  v-model = "searchText " -->
        <div id="emailHelp" class="form-text">
          Мы никогда никому не передадим вашу электронную почту.
        </div>
      </div>
      <div class="mb-3">
        <label for="exampleInputPassword1" class="form-label">Пароль</label>
        <input
          v-bind:value="password"
          v-on:input="passInput($event.target.value)"
          type="password"
          class="form-control"
          id="exampleInputPassword1"
        />
        {{ password }}
      </div>
      <div class="mb-3 form-check">
        <input type="checkbox" class="form-check-input" id="exampleCheck1" />
        <label class="form-check-label" for="exampleCheck1"
          >Проверить меня</label
        >
      </div>
      <button type="submit" class="btn btn-primary">Отправить</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "EmailComponent",
  data() {
    return {
      email: "test@mail.com",
      password: "123456",
    };
  },

  methods: {
    emailInput(value) {
      this.email = value;
    },
    passInput(value) {
      this.password = value;
    },
  },
};
</script>

<style>
</style>