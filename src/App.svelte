<script>
	// import Button from "./Button.svelte";
</script>

<style>
* {
  box-sizing: border-box;
}
*:focus {
  outline: 2px dashed #000;
}
*[class*="fw"]:focus {
  outline-offset: -2px;
}

ul {
  list-style: none;
}

button {
  border: none;
  margin: 0;
  padding: 0;
  width: auto;
  overflow: visible;

  background: transparent;

  /* inherit font & color from ancestor */
  color: inherit;
  font: inherit;

  /* Normalize `line-height`. Cannot be changed from `normal` in Firefox 4+. */
  line-height: normal;

  /* Corrects font smoothing for webkit */
  -webkit-font-smoothing: inherit;
  -moz-osx-font-smoothing: inherit;

  /* Corrects inability to style clickable `input` types in iOS */
  -webkit-appearance: none;
}

button::-moz-focus-inner {
  border: 0;
}

.new-todo-label {
  display: block;
  font-size: 24px;
  font-family: inherit;
  font-weight: inherit;
  line-height: 1.4;
  font-weight: 300;
  padding: 8px;
  text-align: center;
}

.new-todo-input {
  position: relative;
  margin: 0;
  width: 100%;
  font-size: 24px;
  font-family: inherit;
  font-weight: inherit;
  line-height: 1.4em;
  color: inherit;
  padding: 16px 60px;
  border: none;
  background:
  rgba(0, 0, 0, 0.003);
  box-shadow: inset 0 -2px 1px
  rgba(0,0,0,0.03);
}

.btn__primary {
  color: #fff;
  background-color: #000;
}
.btn__primary:focus {
  outline: 2px dashed #fff;
}

.btn__fw {
  display: block;
  width: 100%;
  padding: 16px;
  font-size: 24px;
  line-height: 1.4;
}
</style>

<div class="todoapp">
  <form>
    <label for="new-todo-input" class="new-todo-label">What needs to be done?</label>
    <input type="text" id="new-todo-input" class="new-todo-input input__fw" name="text" autocomplete="off">
    <button type="submit" class="btn btn__primary btn__fw">Add</button>
  </form>
</div>