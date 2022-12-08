<template>
  <Page>
    <ActionBar>
      <Label text="Home"/>
    </ActionBar>

    <GridLayout>
      <ScrollView >
        <StackLayout >

          <Button
              row="2"
              @tap="navigate"
              class="mt-4 px-4 py-2 text-2xl bg-white border-2 border-blue-400 rounded-lg"
              horizontalAlignment="center"
          >
            Navigate
          </Button>
          <MapView height="200"></MapView>
        </StackLayout>
      </ScrollView>
    </GridLayout>
  </Page>
</template>

<script lang="ts">
import Vue from "nativescript-vue";
import Details from "~/components/Details.vue";

export default Vue.extend({
  computed: {
    message() {
      return "Blank {N}-Vue app";
    }
  },
  methods: {
    navigate() {
      this.$navigateTo(Details)
    }
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
