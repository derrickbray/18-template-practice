
<template lang="html">
  <div class="section">
    <div class="container">
      <div class="panel is-fullwidth">
        <h2 class="panel-heading title">Sign Up For My Web App</h2>

        <div class="panel-block">
          <p class="control has-icon has-icon-left">
            <span class="select is-fullwidth">
                <select>
                  <option value="">English</option>
                  <option>Klingon</option>
                  <option>Pig-Latin</option>
                </select>
              </span>
          </p>

          <p class="control has-icon has-icon-left">
            <textarea class="textarea input" placeholder="Your Comments"></textarea>
            <i class="fa fa-comments" aria-hidden="true"></i>
          </p>

          <p class="control has-icon has-icon-left">
            <input class="input" type="text" placeholder="Current Website URL">
            <i class="fa fa-globe" aria-hidden="true"></i>
          </p>
        </div>

        <p class="control is-fullwidth">
          <button class="button is-fullwidth is-primary">Submit</button>
        </p>
      </div>
    </div>
  </div>
</template>

<script>

const apiUrl = 'http://json-data.herokuapp.com/forms';

export default {
  data() {
    return {
      formInputs: [],
      formValues: {},
      apiUrl,
    };
  },

  mounted() {
    this.getData;
  },

  methods: {
    getData() {
      fetch(apiUrl)
      .then((r) => r.json())
      .then((formInputs) => {
        this.formInputs = formInputs;
      };
    },
    submitForm() {},
  },
};
</script>
