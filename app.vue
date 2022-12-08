<template>
  <div :class="{ 'dark': darkMode }">
    <div class="bg-white dark:bg-dim-900">
      <div class="min-h-full">
        <div class="grid grid-cols-12 mx-auto sm:px-6 lg:max-w-7xl lg:px-8 lg:gap-5">
          <!-- Left Sidebar -->
          <div class=" hidden md:block xs:col-span-1 xl:col-span-2 ">
            <div class="sticky top-0">

              <SidebarLeft />
            </div>
          </div>

          <!-- main content -->
          <div class="col-span-12  md:col-span-8 xl:col-span-6">
            <router-view />
          </div>
<!-- Right Sidebar -->
<div class=" hidden md:block md:col-span-3  xl:col-span-4  ">
            <div class="sticky top-0">

            <SidebarRight />
            </div>
          </div>


        </div>

      </div>
    </div>
  </div>

  <footer class="footer absolute bottom-0 items-center">
    <div class="">
      <button
        class="bg-stone-500 text-white active:bg-stone-600 font-bold uppercase text-xs px-4 py-2 rounded shadow hover:shadow-md outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150"
        type="button" @click="toggleTheme">
        Theme
      </button>


    </div>
  </footer>
</template>

<script setup>



const darkMode = ref(false)
const toggleTheme = () => {
  darkMode.value = !darkMode.value
}

</script>


