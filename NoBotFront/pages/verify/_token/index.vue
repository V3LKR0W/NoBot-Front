<template>
  

<div>
     <section>
        <form
        ref="form"
        method="POST"
        @submit.prevent="onSubmit"
        v-bind:action="'https://backend.crying.world/verify?token='+$route.params.token+'&?member='+$route.params.member+'&?guild='+$route.params.guild">
      <h1 class='top-header burple'>Complete the reCaptcha to gain access the server</h1>
  
      <h1 class='secondary-header burple'>Your Access-Token</h1>
      <h1 class='access-token-header'>{{$route.params.token}} </h1>
      <h1 class='third-header burple'>Click the button below</h1>
      
      <div class='center'>
              <v-btn
      type="submit"
      dark
      elevation = 24
      ripple
      class = 'button'
    >
      I am human
    </v-btn>
    </div>

    <recaptcha @error="onError" @success="onSuccess" @expired="onExpired" />
    </form>
      </section>

</div>
</template>

<script>
export default {
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


.burple {
  color: #7289DA;
}

.top-header{
  padding-top: 200px !important;
  font-size: 40px !important;
  padding-bottom: 20px !important;
  text-align: center !important;
}

.grecaptcha-badge { 
    bottom:75px !important; 
}


.secondary-header {
  padding-bottom: 30px !important;
  text-align: center !important;
}

.third-header {
  padding-bottom: 30px !important;
  text-align: center !important;
}

.button {
  text-transform:none !important;
}

.center {
    text-align: center !important;
}

.access-token-header {
text-align: center !important;
padding-bottom: 70px !important;
}
</style>

