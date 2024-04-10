<template>
  <div class="md:flex lg:justify-between pt-9 pb-8 px-8 bg-[#333333]">
    <figure class="md:hidden flex justify-center mb-7">
      <img class="w-36" src="/assets/logos/Leadbox-Logo-black.png" alt="" />
    </figure>

    <div
      class="flex flex-col items-center md:items-start md:w-4/12 lg:w-3/12 text-white mb-6"
    >
      <div class="mb-4">
        <span class="text-sm font-normal"
          >number street, city, province, postal code</span
        >
      </div>
      <div class="mb-4">
        <span class="text-sm font-normal">Sales: (XXX) XXX-XXXX</span>
      </div>
      <div class="mb-4">
        <span class="text-sm font-normal">Parts: (XXX) XXX-XXXX</span>
      </div>
      <div class="mb-4">
        <span class="text-sm font-normal">Service: (XXX) XXX-XXXX</span>
      </div>
    </div>

    <div class="hidden md:block md:w-4/12 lg:w-5/12">
      <figure class="flex justify-center mb-7 md:mb-14">
        <img class="w-36" src="/assets/logos/Leadbox-Logo-black.png" alt="" />
      </figure>
      <figure class="flex justify-center mb-6">
        <a href="https://www.facebook.com/" target="_blank">
          <img
            class="w-6 h-6 mr-2"
            src="../../public/assets/logos/facebook.png"
            alt=""
          />
        </a>
        <a href="https://twitter.com/" target="_blank">
          <img
            class="w-6 h-6 mr-2"
            src="../../public/assets/logos/twitter.png"
            alt=""
          />
        </a>
        <a href="https://www.youtube.com/" target="_blank"
          ><img
            class="w-6 h-6 mr-2"
            src="../../public/assets/logos/youtube.png"
            alt=""
        /></a>

        <a href="https://www.instagram.com/" target="_blank"
          ><img
            class="w-6 h-6 mr-2"
            src="../../public/assets/logos/instagram.png"
            alt=""
        /></a>

        <a href="https://www.pinterest.com/" target="_blank"
          ><img
            class="w-6 h-6 mr-2"
            src="../../public/assets/logos/pinterest.png"
            alt=""
        /></a>

        <a href="https://www.linkedin.com/" target="_blank"
          ><img
            class="w-6 h-6 mr-2"
            src="../../public/assets/logos/linkedin.png"
            alt=""
        /></a>
      </figure>

      <div class="text-center md:px-6">
        <span class="text-xs font-normal text-white"
          >Sitemap | Terms and Conditions | Privacy Policy | Dealership © 2022 |
          Powered by Leadbox</span
        >
      </div>
    </div>

    <div class="md:w-4/12 lg:w-3/12">
      <select v-model="selectedDays" class="w-full mb-3" name="" id="">
        <option class="bg-[#828282]" :value="'sales'">SALES</option>
        <option class="bg-[#828282]" :value="'service'">SERVICE</option>
        <option class="bg-[#828282]" :value="'parts'">PARTS</option>
      </select>

      <div class="mb-6">
        <div
          v-if="selectedDays === 'sales' || selectedDays === 'parts'"
          class="flex justify-between md:justify-start mb-2"
        >
          <div class="text-xs font-normal text-white">
            <div class="hidden md:block md:mr-14">
              <p>Monday:</p>
              <p>8:00am-8:00pm</p>
            </div>

            <span class="md:hidden">Monday: 8:00am-8:00pm</span>
          </div>
          <div class="text-xs font-normal text-white">
            <div class="hidden md:block">
              <p>Thursday:</p>
              <p>8:00am-8:00pm</p>
            </div>

            <span class="md:hidden">Thursday: 8:00am-8:00pm</span>
          </div>
        </div>
        <div
          v-if="selectedDays === 'sales'"
          class="flex justify-between md:justify-start mb-2"
        >
          <div class="text-xs font-normal text-white">
            <div class="hidden md:block md:mr-14">
              <p>Tuesday:</p>
              <p>8:00am-8:00pm</p>
            </div>

            <span class="md:hidden">Tuesday: 8:00am-8:00pm</span>
          </div>
          <div class="text-xs font-normal text-white">
            <div class="hidden md:block">
              <p>Friday:</p>
              <p>8:00am-8:00pm</p>
            </div>

            <span class="md:hidden">Friday: 8:00am-8:00pm</span>
          </div>
        </div>
        <div class="flex justify-between md:justify-start mb-2">
          <div class="text-xs font-normal text-white">
            <div class="hidden md:block md:mr-14">
              <p>Wednesday:</p>
              <p>8:00am-8:00pm</p>
            </div>

            <span class="md:hidden">Wednesday: 8:00am-8:00pm</span>
          </div>
          <div class="text-xs font-normal text-white">
            <div class="hidden md:block">
              <p>Saturday:</p>
              <p>8:00am-8:00pm</p>
            </div>

            <span class="md:hidden">Saturday: 8:00am-8:00pm</span>
          </div>
        </div>
        <div class="flex justify-between md:justify-start mb-2">
          <div class="text-xs font-normal text-white">
            <div class="hidden md:block">
              <p>Sunday:</p>
              <p>Closed</p>
            </div>

            <span class="md:hidden">Sunday: Closed</span>
          </div>
        </div>
      </div>
    </div>

    <div class="md:hidden">
      <figure class="flex justify-center mb-6">
        <a href="https://www.facebook.com/" target="_blank">
          <img
            class="w-6 h-6 mr-2"
            src="../../public/assets/logos/facebook.png"
            alt=""
          />
        </a>
        <a href="https://twitter.com/" target="_blank">
          <img
            class="w-6 h-6 mr-2"
            src="../../public/assets/logos/twitter.png"
            alt=""
          />
        </a>
        <a href="https://www.youtube.com/" target="_blank"
          ><img
            class="w-6 h-6 mr-2"
            src="../../public/assets/logos/youtube.png"
            alt=""
        /></a>

        <a href="https://www.instagram.com/" target="_blank"
          ><img
            class="w-6 h-6 mr-2"
            src="../../public/assets/logos/instagram.png"
            alt=""
        /></a>

        <a href="https://www.pinterest.com/" target="_blank"
          ><img
            class="w-6 h-6 mr-2"
            src="../../public/assets/logos/pinterest.png"
            alt=""
        /></a>

        <a href="https://www.linkedin.com/" target="_blank"
          ><img
            class="w-6 h-6 mr-2"
            src="../../public/assets/logos/linkedin.png"
            alt=""
        /></a>
      </figure>

      <div class="text-center">
        <span class="text-xs font-normal text-white"
          >Sitemap | Terms and Conditions | Privacy Policy | Dealership © 2022 |
          Powered by Leadbox</span
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedDays: 'sales',
    }
  },
}
</script>

<style></style>
