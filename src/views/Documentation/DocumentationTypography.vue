<template>
  <article class="documentation-typography">
    <p class="documentation-typography__title-1">
      h1 title
    </p>

    <p class="documentation-typography__title-2">
      h2 title
    </p>

    <p class="documentation-typography__title-3">
      h3 title
    </p>

    <p class="documentation-typography__title-4">
      h4 title
    </p>

    <p class="documentation-typography__title-5">
      H5 TITLE or caption
    </p>

    <p class="documentation-typography__body">
      Body text. Ipsum cupidatat consequat nisi aliqua. Cupidatat elit voluptate est labore voluptate voluptate incididunt eiusmod incididunt aute elit. Ea ex aliqua sunt do magna sit laborum exercitation aliquip ea. Aliquip fugiat reprehenderit in est excepteur est.
    </p>
  </article>
</template>

<style lang="scss" scoped>
.documentation-typography {
  color: var(--neutral-60);
  padding: var(--padding-3-square);

  &__title-1 {
    font: var(--font-title-1);
    margin-top: 16px;
  }

  &__title-2 {
    font: var(--font-title-2);
    margin-top: 16px;
  }

  &__title-3 {
    font: var(--font-title-3);
    margin-top: 16px;
  }

  &__title-4 {
    font: var(--font-title-4);
    margin-top: 16px;
  }

  &__title-5 {
    font: var(--font-caption);
    margin-top: 16px;
  }

  &__body {
    font: var(--font-body);
    margin-top: 16px;
  }
}
</style>
