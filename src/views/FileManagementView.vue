<template>
  <div id="file_manager" class="m-2">

    <div class="file_toolbar p-2 flex justify-between bg-[#fafafa] w-full" style="border-bottom: 1px solid gainsboro">
      <div class="toolbar_action flex">
        <span class="flex toolbar_item w-fit p-1 cursor-pointer">
        <IconUpload/>
        <span class="text-[13px] ml-[3px]">Upload</span>
      </span>

        <span class="flex toolbar_item w-fit p-1 cursor-pointer relative z-1" @click="openSortDialog">
        <IconSort/>
        <span class="text-[13px] ml-[3px]">Sort By</span>

        <div id="sort_dialog" class="hidden sort_opt absolute z-10 bg-white left-0 top-[26px] text-[13px]"
             style="border: 1px solid gainsboro">
          <ul style="border-bottom: 1px solid gainsboro" class="pb-1">
            <li class="sort_opt_item p-2 flex items-center gap-[5px]">
              <IconCheck/>
              Name
            </li>
           <li class="sort_opt_item p-2 flex items-center gap-[5px]">
              Size
            </li>
            <li class="sort_opt_item p-2 flex items-center gap-[5px]">
              Type
            </li>
          </ul>

          <ul class="pb-1">
           <li class="sort_opt_item p-2 flex items-center gap-[5px]">
              <IconCheck/>
              Ascending
            </li>
            <li class="sort_opt_item p-2 flex items-center gap-[5px]">
              Descending
            </li>
            <li class="sort_opt_item p-2 flex items-center gap-[5px]">
              None
            </li>
          </ul>
        </div>
      </span>

        <span class="flex toolbar_item w-fit p-1 cursor-pointer">
        <IconReload/>
        <span class="text-[13px] ml-[3px]">Refresh</span>
      </span>
      </div>

      <span class="flex toolbar_menu toolbar_item w-fit p-1 cursor-pointer relative" @click="openMenuDialog">
        <IconBar/>
        <div id="menu_dialog" class="hidden sort_opt absolute z-10 bg-white right-0 top-[26px] text-[13px]"
                     style="border: 1px solid gainsboro">
          <ul class="pb-1">
           <li class="sort_opt_item p-2 flex items-center gap-[5px]">
              <IconCheck />
              Large icon
            </li>
            <li class="sort_opt_item p-2 flex items-center gap-[5px]">
              Detail
            </li>
          </ul>
        </div>

      </span>
    </div>


    assas
    as

  </div>
</template>

<script setup>
import IconUpload from '@/components/icons/IconUpload.vue'
import IconSort from '@/components/icons/IconSort.vue'
import IconReload from "@/components/icons/IconReload.vue";
import IconBar from "@/components/icons/IconBar.vue";
import IconCheck from "@/components/icons/IconCheck.vue";


const openSortDialog = () => {
  const sortDialog = document.querySelector('#sort_dialog')
  sortDialog.classList.toggle('hidden')
}
const openMenuDialog = () => {
  const sortDialog = document.querySelector('#menu_dialog')
  sortDialog.classList.toggle('hidden')
}

</script>


<style scoped>
#file_manager {
  border: 1px solid black;
}

.toolbar_item:hover {
  background-color: rgba(0, 0, 0, 0.12);
}

.sort_opt .sort_opt_item:hover, .toolbar_menu:hover {
  background-color: rgba(0, 0, 0, 0.12);
}
</style>