
<template lang="html">
  <div class="section">
    <div class="container">
      <div class="panel is-fullwidth">
        <h2 class="panel-heading title">Sign Up For My Web App</h2>

        <div class="panel-block">

          <p v-for="item in formInputs" v-if="item.type !== 'select' && item.type !== 'textarea'" class="control has-icon has-icon-left">
            <input class="input" type="text" :placeholder="item.label">
            <i :class="item.icon"  class="fa" aria-hidden="true"></i>
          </p>

            <p v-for="item in formInputs" v-if="item.type == 'select'" v-model="formValues[formInputs.id]" class="control has-icon has-icon-left">
              <span class="select is-fullwidth">
                <select>
                  <option v-for="option in item.options" :placeholder="item.label" value="">{{ option.label }}</option>
                </select>
              </span>
            </p>

          <p v-for="item in formInputs" v-if="item.type == 'textarea'" class="control has-icon has-icon-left">
            <textarea class="textarea input" :placeholder="item.label"></textarea>
            <i class="fa" :class="item.icon" aria-hidden="true"></i>
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
    this.getData();
  },

  methods: {
    getData() {
      fetch(apiUrl)
      .then((r) => r.json())
      .then((formInputs) => {
        this.formInputs = formInputs;
      });
    },
    submitForm(formValues) {
      fetch('http://tiny-tn.herokuapp.com/collections/form-derrick',{
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
        },
        body: JSON.stringify(this.formValues)
      })
      .then(() => {
        console.log(formValues);
        this.formValues = formValues;
      });
    },
  },
};
</script>
