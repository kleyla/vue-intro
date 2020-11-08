<template>
  <div>
    <formHelper>
      <div slot="form-header">
        <h3>Form one - Contact us</h3>
        <p>Fill in this form to contact us</p>
      </div>
      <div slot="form-field">
        <input type="text" placeholder="name" required />
        <label>Your message:</label>
        <textarea></textarea>
      </div>
      <div slot="form-controls">
        <button >Send</button>
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
