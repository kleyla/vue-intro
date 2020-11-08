<template>
  <div>
    <formHelper>
      <div slot="form-header">
        <h3>Form two - Log in</h3>
        <p>Enter your details to log-in</p>
      </div>
      <div slot="form-field">
        <input type="text" placeholder="name" required />
        <input type="password" placeholder="pass" required />
      </div>
      <div slot="form-controls">
        <button >Login</button>
      </div>
    </formHelper>
  </div>
</template>

<script>
import formHelper from "./formHelper";

export default {
  components: {
    formHelper,
  },
};
</script>
