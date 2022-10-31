<template>
  <header class="page-header">
    <div class="page-header__inner">
      <svg class="page-header__logo" width="84" height="73" viewBox="0 0 84 73" fill="none" xmlns="http://www.w3.org/2000/svg">
        <rect x="14" y="11" width="70" height="62" fill="#FFEBD3"/>
        <rect x="42" y="14.4828" width="14" height="45.8621" rx="2" fill="#2B2D33"/>
        <rect width="14" height="14.4828" rx="2" transform="matrix(1 0 0 -1 56 28.9651)" fill="#2B2D33"/>
        <rect y="0.000366211" width="14" height="44.6552" rx="2" fill="#2B2D33"/>
        <rect width="14" height="14.4828" rx="2" transform="matrix(1 0 0 -1 28 14.4828)" fill="#2B2D33"/>
        <rect width="14" height="14.4828" rx="2" transform="matrix(1 0 0 -1 28 44.6559)" fill="#2B2D33"/>
        <rect x="14" y="24.1381" width="14" height="45.8621" rx="2" fill="#2B2D33"/>
      </svg>
      <ul class="main-menu">
        <li class="main-menu__item">
          How it works
        </li>
        <li class="main-menu__item">
          Features
        </li>
        <li class="main-menu__item">
          Download
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: 'PageHeader',
}
</script>

<style scoped lang="less">
  @import "../less/variables.less";
    .page-header {
      min-height: 100%;
 
      &__inner {
        max-width: 1108px;
        margin: 0 auto;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        padding-top: 32px;
      }

      &__logo {
        width: 84px;
        height: 73px;
      }
    }

    .main-menu {
      display: flex;
      flex-direction: row;

      &__item {
        margin-right: 8px;
        padding: 12px 20px;

        &:last-child {
          margin-right: 0;
        }
      }
    }
</style>
