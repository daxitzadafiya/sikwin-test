<template>
  <div class="pb-3">
    <b-container fluid="md">
      <b-row class="justify-content-between">
        <div class="col-sm-5 col-12 d-flex align-items-end h-75">
          <div class="col-2">
            <img
              src="@/assets/images/pocketsection/pocket.png"
              alt=""
              class="img-fluid"
            />
          </div>
          <div class="col-10">
            <div class="ms-3">
              <h3 class="m-0 fw-normal">
                KEN
                <img
                  src="@/assets/images/pocketsection/vip.png"
                  alt=""
                  class="img-fluid vip-img pb-1 me-1"
                />
                <span class="text-gold fs-3">7</span>
              </h3>
              <p class="w-full m-0 fw-normal text-wrap">
                $<span class="text-gold fs-4">122121233</span>
              </p>
            </div>
          </div>
        </div>
        <div class="col-1 d-none d-sm-block  text-center">
          <img
            src="@/assets/images/pocketsection/divider.png"
            alt=""
            class="img-fluid"
          />
        </div>
        <div class="col-sm-5 col-12 mt-4 mt-sm-0">
          <p class="w-full m-0 text-wrap">
            <img
              src="@/assets/images/pocketsection/volume.png"
              alt=""
              class="img-fluid"
            />
            <span class="text-break">

            :Dragon Boat Festival holiday!holiday!holiday!holiday!Dragon Boat
            Festival holiday! estival holiday!
            </span>
          </p>
        </div>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  name: "pocket-com",
};
</script>

<style scoped>
.vip-img {
  width: 30px;
}
</style>