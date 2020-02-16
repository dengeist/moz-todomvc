<script>
  import Item from "./Item.svelte";
  let items = [
    {
      id: '001',
      name: 'Apple',
      checked: false,
      isEditing: false
    },
    { id: '002',
      name: 'Oranges',
      checked: false,
      isEditing: true
    }
  ];
</script>

<style>

.todoapp {
  background:
  #fff;
  margin: 130px 0 40px 0;
  padding: 0 60px;
  position: relative;
  box-shadow: 0 2px 4px 0
rgba(0, 0, 0, 0.2), 0 25px 50px 0 rgba(0, 0, 0, 0.1);
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
  border: 2px solid #000;
  background:
  rgba(0, 0, 0, 0.003);
  box-shadow: inset 0 -2px 1px
  rgba(0,0,0,0.03);
}

.new-todo-input:focus {
  border-color: #4d4d4d;
  outline-offset: -6px;
}

button {
  margin-top: 4px;
}
</style>

<div class="todoapp">
  <form>
    <label for="new-todo-input" class="new-todo-label">What needs to be done?</label>
    <input type="text" id="new-todo-input" class="new-todo-input input__fw" name="text" autocomplete="off">
    <button type="submit" class="btn btn__primary btn__fw">Add</button>
  </form>
  <ul>
    { #each items as item }
    <Item {...item} />
    {/each}
  </ul>
</div>