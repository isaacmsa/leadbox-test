<template>
  <nav
    class="flex justify-between items-center h-20 pl-8 md:pl-16 lg:pl-14 pr-6 md:pr-16 bg-white shadow-lg fixed z-50 left-0 right-0"
  >
    <figure>
      <img
        class="w-36"
        src="/assets/logos/LeadboxLogo-large.png"
        alt="header-logo"
      />
    </figure>

    <div class="flex items-center h-full">
      <ul class="hidden md:flex md:items-center md:h-full mr-12">
        <dropdown-button :title="'new'">
          <template #drop>
            <div>
              <div class="mb-3">
                <span
                  class="font-normal text-sm hover:font-bold hover:underline underline-offset-2"
                  >New Vehicle Inventory</span
                >
              </div>
              <div class="mb-3">
                <span
                  class="font-normal text-sm hover:font-bold hover:underline underline-offset-2"
                  >2023 Ford Lightning</span
                >
              </div>
              <div class="mb-3">
                <span
                  class="font-normal text-sm hover:font-bold hover:underline underline-offset-2"
                  >2023 Ford Bronco</span
                >
              </div>
              <div class="mb-3">
                <span
                  class="font-normal text-sm hover:font-bold hover:underline underline-offset-2"
                  >New Vehicle Specials</span
                >
              </div>
            </div>
          </template>
        </dropdown-button>
        <li class="text-sm font-medium uppercase mx-4 lg:mx-10 hover:font-bold">
          used
        </li>
        <li
          class="hidden lg:flex text-sm font-medium uppercase mx-4 lg:mx-10 hover:font-bold"
        >
          parts
        </li>
        <li class="text-sm font-medium uppercase mx-4 lg:mx-10 hover:font-bold">
          service
        </li>
        <li class="text-sm font-medium uppercase mx-4 lg:mx-10 hover:font-bold">
          about
        </li>
      </ul>

      <button
        type="button"
        @click="showSearch"
        class="flex items-center mr-3 md:mr-0"
      >
        <img
          class="w-8 h-8"
          src="/assets/icons/search-icon.png"
          alt="search-logo"
        />
      </button>

      <button
        @click="showMenu"
        type="button"
        class="flex items-center md:hidden"
      >
        <img
          v-if="!isShowMenu"
          class="w-11"
          src="/assets/icons/menu-md-.png"
          alt="search-logo"
        />

        <span class="text-5xl font-semibold uppercase" v-else>x</span>
      </button>
    </div>

    <search-bar v-if="isSearch" />

    <drop-menu-mobile v-if="isShowMenu" />
  </nav>
</template>

<script>
import DropdownButton from '../components/DropdownButton.vue'
import DropMenuMobile from '../components/DropMenuMobile.vue'
import SearchBar from '../components/SearchBar.vue'

export default {
  components: {
    DropdownButton,
    DropMenuMobile,
    SearchBar,
  },
  data() {
    return {
      isShowMenu: false,
      isSearch: false,
    }
  },
  methods: {
    showMenu() {
      this.isShowMenu = !this.isShowMenu
    },
    showSearch() {
      this.isSearch = !this.isSearch
    },
  },
}
</script>

<style></style>
