<template>
  <div class="header-style">
    <div>
      <img
        src="../assets/settings.svg"
        alt=""
        style="width: 25px; height: auto; fill: #CCD1D5;"
      />
    </div>
    <div
      style="text-align: center;font-family: 'Pacifico', cursive; font-size: 24px; font-weight: 400; flex-grow: 1;"
    >
      Instagram
    </div>
    <div class="mail-icon">
      <img src="../assets/mail.svg" alt="" style="width: 22px; height: auto" />
      <span class="noti"></span>
    </div>
    <div></div>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.header-style {
  @media (max-width: 576px) {
    display: flex;
    //justify-content: space-around;
    align-items: center;
    padding: 2px 0 3px 0;
    margin-left: 1.5rem;
    margin-right: 1.5rem;
  }
  .noti {
    position: absolute;
    width: 8px;
    height: 8px;
    background-color: #fc045c;
    border-radius: 50px;
    right: 21px;
    top: 24px;
    //hide
  }
}
</style>
