
<template lang="html">
  <div class="section">
    <div class="container">
      <div class="panel is-fullwidth">
        <h2 class="panel-heading title">Sign Up For My Web App</h2>


          <div class="panel-block">
            <p class="control has-icon has-icon-left">
              <input class="input" type="text" placeholder="First Name">
              <i class="fa fa-user" aria-hidden="true"></i>
            </p>

            <p class="control has-icon has-icon-left">
              <input class="input" type="text" placeholder="Last Name">
              <i class="fa fa-user" aria-hidden="true"></i>
            </p>

            <p class="control has-icon has-icon-left">
              <input class="input" type="text" placeholder="E-Mail Address">
            <i class="fa fa-envelope" aria-hidden="true"></i>
            </p>

            <p class="control has-icon has-icon-left">
              <input class="input" type="text" placeholder="Current Website URL">
              <i class="fa fa-globe" aria-hidden="true"></i>
            </p>

            <p class="control">
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
              <input class="input" type="text" placeholder="Mobile Phone">
              <i class="fa fa-mobile" aria-hidden="true"></i>
            </p>

            <p class="control has-icon has-icon-left">
              <input class="input" type="text" placeholder="Home Phone">
              <i class="fa fa-phone" aria-hidden="true"></i>
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
export default {
  data() {
    return {
    };
  },

  methods: {

  },
};
</script>
