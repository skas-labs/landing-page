<template>
  <div class="registeration-form">
      <div :class="{visible: hasSubmitted}">Thanks for your interest! You'll hear from us soon. </div>
      <div :class="{visible: !hasSubmitted}" class="bevel py-1">
        <div class="d-inline-block flex-grow-1 d-flex">
          <input type="email" placeholder="enter your email address" class="emailForm  my-auto pl-3 py-2" v-model="email">
        </div>
        <button class="btn btn-orange px-md-4 py-md-2 text-white flex-shrink-1" @click="submitForm">notify me</button>
      </div> 
  </div> 
</template>

<script>
export default {
  name: 'EmailRegisterationForm',
  data () {
    return {
      email: '',
      hasSubmitted: Boolean(window.localStorage.getItem('hasRegistered')) ?? false
    }
  },
  methods: {
    async submitForm () {
      const {email} = this
      try {
        await this.$axios.post('/registration', {email})
        this.hasSubmitted = true
        window.localStorage.setItem('hasRegistered', true)
      } catch (err) {
        if (!err?.response?.data) {
          throw err
        }

        const {response: {data}} = err

        switch(data.statusCode) {
          case 500: return alert(data.message)
          case 400: return alert('Invalid Input')
          default: return alert('We cannot process that request now. Try again later.')
        }
      }
    }
  }
}
</script>

<style scoped>
.bevel{
  box-sizing: content-box;
  box-shadow: inset 4px 4px 8px #03030A, inset -4px -4px 8px #24242E;
  background: #0F0F20;
  border: none;
  font-family: muli;
  font-weight: 800;
  font-size: 1registeration-form;
  display: flex;
}
.emailForm{
    background: none;
    border: none;
    width: 100%;
    color: white;
    /* box-shadow: inset 4px 4px 8px #03030A, inset -4px -4px 8px #24242E; */
}
.btn-orange{
  background: linear-gradient(224.85deg, #F8501C 2.25%, #FFAB1D 100%);
  color: white;
  height: 100%;
  font-weight: 600;
  font-size: 1em;
}

.registeration-form>div {
  transition: all 0.5s ease-in-out;
  opacity: 0;
}


.registeration-form>div.visible {
  opacity: 1;
}

</style>