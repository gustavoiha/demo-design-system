<template>
  <div class="ds-timeline">
    <template
      v-for="item in items"
      :key="item.id"
    >
      <div class="ds-timeline__title-container">
        <p class="ds-timeline__title">
          {{ item.title }}
        </p>
      </div>

      <div class="ds-timeline__marker" />

      <div class="ds-timeline__content-container">
        <slot
          :name="item.id"
          :content="item.content"
        >
          <p class="ds-timeline__content-text">
            {{ item.content }}
          </p>
        </slot>
      </div>

      <div class="ds-timeline__connector" />
    </template>
  </div>
</template>

<script setup>
defineProps({
  items: {
    type: Array,
    required: true
  }
})
</script>

<style lang="scss" scoped>
.ds-timeline {
  $marker-size: 2rem;

  display: grid;
  grid-auto-rows: $marker-size minmax(40px, auto);
  grid-template-columns: auto auto 1fr;

  &__title-container {
    padding: 0.3rem 16px;
    grid-row: span 2;
  }

  &__content-container {
    color: var(--neutral-60);
    padding: 0.3rem 16px;
    grid-row: span 2;
  }

  &__content-text {
    font: var(--font-body);
  }

  &__title {
    color: var(--neutral-60);
    text-align: end;
  }

  &__marker {
    background-color: transparent;
    border: 2px solid var(--plum-100);
    border-radius: 50%;
    display: grid;
    height: $marker-size;
    place-content: center;
    width: $marker-size;

    &:before {
      background-color: var(--plum-100);
      border-radius: 50%;
      content: "";
      height: 1rem;
      width: 1rem;
    }
  }

  &__connector {
    background-color: var(--plum-100);
    justify-self: center;
    width: 2px;

    &:last-of-type {
      display: none;
    }
  }
}
</style>
