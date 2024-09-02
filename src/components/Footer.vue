<template>
  <footer class="relative bg-blue-900 text-white pt-8 pb-6">
    <div class="container mx-auto px-4">
      <div class="flex flex-wrap text-left lg:text-left">
        <div class="w-full lg:w-6/12 px-4">
          <h4 class="text-3xl fonat-semibold text-blueGray-700">
            Let's keep in touch!
          </h4>
          <h5 class="text-lg mt-0 mb-2 text-blueGray-600">
            Copyright {{ currentYear }} © All rights reserved. | Designed &
            Developed by HSPM Solutions LLP.
          </h5>

          <!-- Display the visitor count image -->
          <div class="flex mx-auto mt-4">
            <img
              src="https://dhfservices.in/api/admin/images/counter"
              alt="Website Visitors"
              class="w-48"
            />
          </div>
        </div>
      </div>
      <hr class="my-6 border-blueGray-300" />
      <div
        class="flex flex-wrap items-center md:justify-between justify-center"
      >
        <div class="w-full md:w-4/12 px-4 mx-auto text-center">
          <div class="text-sm text-blueGray-500 font-semibold py-1"></div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      currentYear: new Date().getFullYear(),
    };
  },
};
</script>
