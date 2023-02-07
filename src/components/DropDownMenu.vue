<script>
import { Menu, MenuButton, MenuItems, MenuItem } from "@headlessui/vue";

export default {
  components: {
    Menu,
    MenuButton,
    MenuItems,
    MenuItem,
  },
  props: {
    videos: {
      type: Array,
      required: true,
    },
  },
};
</script>

<template>
  <Menu as="div" class="relative inline-block text-left">
    <MenuButton
      class="inline-flex justify-center rounded-md bg-slate-700 px-4 py-2 text-sm font-medium text-white hover:bg-opacity-30 focus:outline-none focus-visible:ring-2 focus-visible:ring-white focus-visible:ring-opacity-75"
    >
      Videos
    </MenuButton>

    <transition
      enter-active-class="transition duration-100 ease-out"
      enter-from-class="transform scale-95 opacity-0"
      enter-to-class="transform scale-100 opacity-100"
      leave-active-class="transition duration-75 ease-in"
      leave-from-class="transform scale-100 opacity-100"
      leave-to-class="transform scale-95 opacity-0"
    >
      <MenuItems
        class="absolute right-0 mt-2 w-56 origin-top-right divide-y divide-gray-100 rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
      >
        <div class="px-1 py-1">
          <MenuItem v-slot="{ active }" v-for="video in videos">
            <button
              :class="[
                active ? 'bg-slate-500 text-white' : 'text-gray-900',
                'group flex w-full items-center rounded-md px-2 py-2 text-sm',
              ]"
            >
              {{ video.url }}
            </button>
          </MenuItem>
        </div>
      </MenuItems>
    </transition>
  </Menu>
</template>
