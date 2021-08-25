<template>
  <section class="header">
    <h1 class="header__title">Добавление товара</h1>
    <div class="header__select">
      <span class="header__select-value">По умолчанию</span>
      <svg
        width="8"
        height="8"
        viewBox="0 0 8 8"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M7.48532 3.24264L4.24268 6.48528L1.00003 3.24264"
          stroke="#B4B4B4"
        />
      </svg>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HeaderApp'
}
</script>

<style scoped lang="scss">
@import "../styles/scss/_variables";
.header {
  font-family: "SourceSansPro-SemiBold";
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 32px 0 16px;
  &__title {
    font-size: 28px;
    line-height: 36px;
  }
  &__select {
    font-family: 'Source Sans Pro', monospace;
    padding: 10px 16px;
    border-radius: 4px;
    color: $color__B4;
    font-size: 12px;
    line-height: 15px;
    box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
    cursor: pointer;
  }
}
</style>
