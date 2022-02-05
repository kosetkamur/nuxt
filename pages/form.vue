<template>
<div>
<div>
    <h1>Посмотрите на этих малышек и запишитесь!</h1>
    <img src="@/assets/images/cow_img.jpg" alt="animal" class="animal">
    <img src="@/assets/images/rabbit_img.jpg" alt="animal" class="animal">
    <img src="@/assets/images/sheep_img.jpg" alt="animal" class="animal">
</div>
    <v-card-text
            class="text-center"
          >
            <v-btn
              color="primary"
              @click="hidden = !hidden"
            >
              {{ hidden ? 'Показать форму' : 'Скрыть форму' }}
    </v-btn>
    </v-card-text>
    <form @submit.prevent="submit" v-show="!hidden">
      <validation-provider
        name="Name"
        rules="required|max:10"
      >
        <v-text-field
          v-model="name"
          label="Имя"
          required
        ></v-text-field>
      </validation-provider>
      <validation-provider
        name="phoneNumber"
      >
        <v-text-field
          v-model="phoneNumber"
          :counter="11"
          label="Номер телефона"
          required
        ></v-text-field>
      </validation-provider>
      <validation-provider
        name="email"
      >
        <v-text-field
          v-model="email"
          label="E-mail"
          required
        ></v-text-field>
      </validation-provider>
      <validation-provider
        name="select"
        rules="required"
      >
        <v-checkbox
          v-model="checkbox"
          value="1"
          label="Даю согласие на обработку персональных данных"
          type="checkbox"
          required
        ></v-checkbox>
      </validation-provider>

      <v-btn
        class="mr-4"
        type="submit"
        :disabled="invalid"
      >
        Отправить
      </v-btn>
    </form>
</div>
</template>
<script>
  export default {
    data: () => ({
      hidden: false,
    }),
  }
</script>
<style scoped>
    .animal{
        height: 300px;
        width: auto;
        margin-top: 40px;
    }
</style>