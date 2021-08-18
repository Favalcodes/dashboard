<template>
  <div id="top">
      <div class="d-flex justify-content-between">
            <div class="search d-flex">
                <font-awesome-icon icon="search" class="search-fonts d-flex"/>
                <input v-model="text" class="bg-transparent form-control" placeholder="Search" />
            </div>
            <div class="theme d-flex justify-content-evenly">
                <div class="moon">
                    <font-awesome-icon icon="moon" class="fonts"/>
                </div>
                <div class="pix">
                    <img src="../assets/hanna.png" alt="">
                </div>
                <p><strong>Hanna Idahosa <font-awesome-icon icon="caret-down"/></strong></p>
            </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'top',
    props: ['text']
}
</script>

<style>
#top{
    padding: 25px 0px;
}
.search{
    width: 50%;
    align-items: center;
    justify-content: center;
}
.search-fonts{
    color: #90A0C2;
    font-size: 20px;
    margin-right: 5px;
}
.form-control{
    border: none !important;
    outline: none !important;
    box-shadow: none;
}
.form-control:focus{
    outline: none !important;
}
.theme{
    width: 30%;
    color: #fff;
}
.moon{
    padding: 5px;
    background: radial-gradient(78.1% 197.78% at 48.06% 0%, #5285F2 0%, #2250E7 100%);
    width: 32px;
    height: 32px;
    border-radius: 50%;
}
.fonts{
    /* color: #fff; */
    font-size: 20px;
}
.pix{
    width: 32px;
    height: 32px;
    border-radius: 50%;
}
.pix img{
    width: 100%;
    height: 100%;
    object-fit: contain;
    border-radius: 50%;
}
</style>