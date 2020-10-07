<template>
  
<div class='wrapper'>
<h1 class='header burple'>Report</h1>
<form dark
    input
    ref="form"
    lazy-validation
    method="POST"
    @submit.prevent="onSubmit"
    action = 'https://backend.crying.world/relay'

    class='padding'
>
 <v-text-field
      name = 'name'
      :counter="30"
      label="What is your discord tag?"
      required
    ></v-text-field>
    <br>
  <v-select
      name = 'type_of'
      :items="items"
      label="What type of user are you?"
      required
    ></v-select>
    <br>
     <v-text-field
      name = 'issue'
      :counter="200"
      label="Please describe the issue."
      required
    ></v-text-field>

    <recaptcha @error="onError" @success="onSuccess" @expired="onExpired" />
    <div class='button-wrapper'>
              <v-btn
      type="submit"
      dark
      elevation = 24
      ripple
      class = 'button'
    >
      Submit report
    </v-btn>
    </div>
</form>

</div>
</template>

<script>
export default {

  data: () => ({
      items: [
        "I'm a server guest",
        "I'm a server admin",
        "I'm a security researcher",
      ],
    }),

  methods: {
    onError(error) {
      console.log('Error happened:', error)
    },
    async onSubmit() {
      try {
        const token = await this.$recaptcha.getResponse()
        console.log('ReCaptcha token:', token)
        await this.$recaptcha.reset()
      } catch (error) {
        console.log('Failed: ',token)
      }
    },
    onSuccess(token) {
      console.log('Succeeded:', token)
      this.$refs.form.submit()
    },
    onExpired() {
      console.log('Expired')
    }
  }
};

</script>

<style>
.padding {
    padding-top: 100px;
}

.header {
    font-size: 70px;
    text-align: center;
}

.burple {
  color: #7289DA;
}

.button-wrapper {
    padding-top: 50px;
    margin-right: auto;
    margin-left: auto;
}

.grecaptcha-badge { 
    bottom:75px !important; 
}

.wrapper {
    padding-top: 100px;
    height: auto;
    width: auto;
    margin-right: auto;
    margin-left: auto;
}
</style>

