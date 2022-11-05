<template>
  <v-github-icon url="https://github.com/vinayakkulkarni/v-tweakpane" />
  <section class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4">
    <v-tweakpane class="p-4" :pane="state.pane" />
    <v-tweakpane class="p-4" :pane="state.pane" />
    <v-tweakpane class="p-4" :pane="state.pane" />
    <v-tweakpane class="p-4" :pane="state.pane" />
  </section>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import { VGithubIcon } from 'v-github-icon';
import { VTweakpane } from 'v-tweakpane';

export default defineComponent({
  components: {
    VTweakpane,
    VGithubIcon,
  },
  setup() {
    const state = ref({
      pane: {
        title: 'My Awesome Pane',
        inputs: [
          {
            factor: 123,
            title: 'hello',
            color: '#0f0',
          },
        ],
      },
    });
    return {
      state,
    };
  },
});
</script>
<style>
@import 'v-github-icon/dist/v-github-icon.css';
@import 'v-tweakpane/dist/v-tweakpane.css';
</style>
