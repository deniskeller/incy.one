<template>
  <div class="container">
    <div class="row">
      <div class="col-md-6 d-flex justify-content-center">
        <div class="card" style="width: 18rem;">
          <img :src="new_image_url || require(`@/assets/logo.png`)" class="card-img-top" />
          <div class="card-body">
            <h5
              class="card-title text-center"
              :style="{ fontSize: new_font_size + 'px' }"
            >{{ new_title || "Заголовок" }}</h5>
          </div>
        </div>
      </div>
      <div class="col-md-6 d-flex justify-content-start">
        <form>
          <div class="form-group">
            <label for="formGroupExampleInput">title</label>
            <input
              type="text"
              v-model.trim="new_title"
              class="form-control"
              id="formGroupExampleInput"
              placeholder="Введите название загловка"
            />
          </div>
          <div class="form-group">
            <label for="formGroupExampleInput2">font size</label>
            <input
              type="number"
              v-model.trim="new_font_size"
              class="form-control"
              id="formGroupExampleInput2"
              placeholder="Введите размер шрифта"
            />
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    title: {
      type: String,
      default: "Menu",
    },
    font_size: {
      type: Number,
      default: 20,
    },
    image_url: {
      type: String,
      degault: "",
    },
  },
  data() {
    return {
      new_title: this.title,
      new_font_size: this.font_size,
      new_image_url: this.image_url,
    };
  },
  computed: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss"></style>
