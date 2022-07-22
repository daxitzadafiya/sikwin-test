<template>
  <div class="dark-bg">
    <b-container fluid="md">
      <b-row>
        <b-navbar
          toggleable="xxl"
          type="dark"
          class="py-3 d-flex justify-content-between"
        >
          <b-navbar-toggle target="nav-collapse" class="p-0">
            <b-navbar-nav class="align-items-start">
              <b-nav-item href="#">
                <img
                  src="@/assets/images/header/notification.png"
                  alt=""
                  class="w-50"
                />
              </b-nav-item>
            </b-navbar-nav>
          </b-navbar-toggle>

          <b-navbar-brand href="#">
            <img src="@/assets/images/header/logo.png" alt="" />
          </b-navbar-brand>
          <div>
            <!-- src="@/assets/images/header/popover.png"  -->
            <b-dropdown variant="transparent">
              <template #button-content>
                <img src="@/assets/images/header/popover.png" alt="" class="w-50"/>
              </template>
              <b-dropdown-item href="#"
                ><b-navbar-nav class="align-items-start">
                  <b-nav-item
                    href="#"
                    v-for="icon in socialIcon"
                    :key="icon.id"
                  >
                    <img
                      :src="
                        require(`@/assets/images/header/icons/${icon.icon}.png`)
                      "
                      alt=""
                      class="w-75"
                    /><span>{{ icon.iconName }}</span>
                  </b-nav-item>
                </b-navbar-nav></b-dropdown-item
              >
            </b-dropdown>
          </div>
          <b-collapse id="nav-collapse" is-nav>
            <b-navbar-nav>
              <div class="accordion" role="tablist">
                <b-card no-body class="card-border bg-transparent mb-1">
                  <b-card-header header-tag="header" class="p-1" role="tab">
                    <div
                      block
                      v-b-toggle.accordion-1
                      variant="transparent"
                      class="text-white py-3 fs-3 fw-normal"
                    >
                      IMPORTANT NOTICE!!!
                    </div>
                  </b-card-header>
                  <b-collapse
                    id="accordion-1"
                    accordion="my-accordion"
                    role="tabpanel"
                  >
                    <b-card-body>
                      <b-card-text class=" fs-3 fw-normal"
                        >To avoid cheating, All payment from SIKWIN must be
                        transfer through by SIKWIN website . Don't ever try to
                        transact payment with Individual Person.<br />SIKWIN
                        will not assign any responsibility for this
                        problem.</b-card-text
                      >
                    </b-card-body>
                  </b-collapse>
                </b-card>
                <b-card no-body class="card-border bg-transparent mb-1">
                  <b-card-header header-tag="header" class="p-1" role="tab">
                    <div
                      block
                      v-b-toggle.accordion-2
                      variant="transparent"
                      class="text-white py-3 fs-3 fw-normal"
                    >
                      Attention!!!
                    </div>
                  </b-card-header>
                  <b-collapse
                    id="accordion-2"
                    accordion="my-accordion"
                    role="tabpanel"
                  >
                    <b-card-body>
                      <b-card-text class=" fs-3 fw-normal"
                        >To avoid cheating, All payment from SIKWIN must be
                        transfer through by SIKWIN website . Don't ever try to
                        transact payment with Individual Person.<br />SIKWIN
                        will not assign any responsibility for this
                        problem.</b-card-text
                      >
                    </b-card-body>
                  </b-collapse>
                </b-card>
                <b-card no-body class="bg-transparent mb-1">
                  <b-card-header header-tag="header" class="p-1" role="tab">
                    <div
                      block
                      v-b-toggle.accordion-3
                      variant="transparent"
                      class="text-white py-3 fs-3 fw-normal"
                    >
                      Announcement
                    </div>
                  </b-card-header>
                  <b-collapse
                    id="accordion-3"
                    accordion="my-accordion"
                    role="tabpanel"
                  >
                    <b-card-body>
                      <b-card-text class="fs-3 fw-normal"
                        ><p>
                          <a href="https://google.com" target="_blank" class="fs-3 fw-normal text-decoration-none"
                            >Google</a
                          >
                        </p></b-card-text
                      >
                    </b-card-body>
                  </b-collapse>
                </b-card>
              </div>
            </b-navbar-nav>
          </b-collapse>
        </b-navbar>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  name: "Header-com",
  data() {
    return {
      showPopover: false,
      placements: ["auto"],
      socialIcon: [
        {
          id: 1,
          icon: "langauge",
          iconName: "हिंदी",
        },
        {
          id: 2,
          icon: "facebook",
          iconName: "Facebook",
        },
        {
          id: 3,
          icon: "instagrame",
          iconName: "Ins",
        },
        {
          id: 4,
          icon: "youtube",
          iconName: "Youtube",
        },
        {
          id: 5,
          icon: "telegram",
          iconName: "Telegram ",
        },
      ],
    };
  },
};
</script>

<style scoped>
.nav-item .nav-link {
  display: flex;
  align-items: center;
}
.nav-item .nav-link span {
  font-size: 20px;
  margin-left: 20px;
  color: #8b8780;
}
.card-border {
  border-bottom: 1px solid #efc275;
}
::v-deep .navbar-dark .navbar-toggler {
  border-color: transparent !important;
}
::v-deep .dropdown-menu {
  right: 50%;
  background-color: rgba(0, 0, 0, 0.8);
  padding: 10px;
  width: 200px;
  top: 110%;
}
::v-deep .dropdown-toggle::after {
  background-image: url("/assets/images/header/popover.png") !important;
  font-size: 0;
}
</style>