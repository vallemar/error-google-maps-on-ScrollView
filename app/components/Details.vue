<template>
  <Page>
    <ActionBar>
      <Label text="Home"/>
    </ActionBar>

    <GridLayout>
      <ScrollView orientation="horizontal">
        <StackLayout orientation="horizontal">
          <Label text="this" />

        </StackLayout>
      </ScrollView>
    </GridLayout>
  </Page>
</template>

<script lang="ts">
  import Vue from "nativescript-vue";

  export default Vue.extend({
    computed: {
      message() {
        return "Blank {N}-Vue app";
      }
    },
    methods:{

    }
  });
</script>

<style scoped lang="scss">
  @import '@nativescript/theme/scss/variables/blue';

  // Custom styles
  .fas {
    @include colorize($color: accent);
  }

  .info {
    font-size: 20;
    horizontal-align: center;
    vertical-align: center;
  }
</style>
