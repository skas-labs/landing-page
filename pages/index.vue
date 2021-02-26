<template>
  <div class="jacket">
    <div class="width-limiter">
      <div class="row mx-5 h-100 align-items-center">
        <div class="col-lg-7">
          <div class="">
            <div class="">
              <img src="../assets/logo_text.svg" alt="" />
            </div>
            <div>
              <div class="font-1">
                get notified when we launch
              </div>
              <div class="my-3 font-2">
                don't worry we will not not spam you
              </div>
            </div>
            <div class="row mt-5">
              <div class="col-sm-10">
                <BevelForm />
              </div>
            </div>
          </div>
        </div>

        <div class="col-lg-5 d-flex justify-content-center">
          <div class="mt-5 my-md-0 d-none d-sm-block ">
            <img
              src="../assets/mobileFront.png"
              alt=""
              class="phone-image mx-auto text-center h-100"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.font-1 {
  margin-top: 5rem;
  font-size: 3rem !important;
  font-weight: 900;
  line-height: 90%;
}
.phone-image {
  background-size: contain;
}

.jacket {
  margin-top: 1rem;
  height: 70vh;
}

.font-2 {
  font-size: 1.5rem !important;
}
</style>
