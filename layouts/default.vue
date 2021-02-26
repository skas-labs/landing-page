<template>
  <div class="wrapper h-100" style="margin-top: -70px;">
    <Navbar />
    <Nuxt />
  </div>
</template>

<script>
export default {};
</script>

<style>
@media (max-width: 576px) {
  html {
    font-size: 12px;
  }
}

* {
  font-family: "muli", sans-serif;
  margin: 0;
}
html {
  font-family: "muli", sans-serif;
  font-weight: 400;
  /* word-spacing: 1px; */
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  background: #0f0f20;
  min-height: 100vh;
}

.wrapper {
  background: #0f0f20;
  color: white;
  /* margin: 0 !important; */
  font-size: 1.5rem;
  position: relative;
  min-height: 95vh;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
