<template>
  <div class="jacket px-md-50 px-25">
    <div class="width-limiter h-100">
      <div class="row no-gutters h-100 align-items-center position-relative">
        <div class="flex-1 left-section t-align-lg-l t-align-c">
          <div class="">
            <div class="">
              <img src="../assets/logo_text.svg" alt="" />
            </div>
            <div>
              <div class="font-level-1">
                get notified when we launch
              </div>
              <div class="my-3 font-level-2">
                don't worry we will not not spam you
              </div>
            </div>
            <div
              class="row mt-5 no-gutters justify-content-lg-start justify-content-center"
            >
              <div class="col-sm-10">
                <BevelForm />
              </div>
            </div>
          </div>
        </div>

        <div class="position-absolute phone-image">
          <div class="mt-5 my-md-0 d-none d-lg-block">
            <img
              src="../assets/mobileFront.png"
              alt=""
              class="mx-auto text-center h-100"
            />
          </div>
        </div>
      </div>
      <div class="mt-10 mx-auto d-block d-lg-none t-align-c">
        <div class="row no-gutters justify-content-center">
          <a href="https://www.instagram.com/codeblitz_cb/" class="text-white">
          <div class="p-3 mx-5 my-4 d-flex">
            <font-awesome-icon :icon="['fab', 'instagram']" style="font-size: 30px" class="mx-3"/>
            <div class="my-auto"> instagram </div>
          </div>
          </a>
        </div>
        <img src="../assets/mobileFront.png" alt="" class="mx-auto" />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.font-level-1 {
  margin-top: 5rem;
  font-size: 3rem !important;
  font-weight: 900;
  line-height: 90%;
}

.phone-image {
  right: 0;
  bottom: 0;
}

.jacket {
  /* margin-top: 1rem; */
  height: calc(100vh - 120px);
}

.font-level-2 {
  font-size: 1.5rem !important;
}

.left-section {
  padding-right: 500px;
}

@media screen and (max-width: 991px) {
  .left-section {
    padding-right: 0;
  }

  .jacket {
    height: unset;
  }
}
</style>
