<template>
  <div class="modal-backdrop">
    <div class="modal">
        <header class="modal-header">
            <slot name="header">
                <h3>Sign Up!</h3>
            </slot>
            <button type="button" class="btn-close" @click="close">
            x
            </button>
        </header>

        <section class="modal-body">
            <slot name="body">
                <form class="form-modal">
                    <div class="form-group">
                        <label for="email" class="form-label">Email</label>
                        <br>
                        <input type="email" class="form-control" id="email" placeholder="Enter email">
                    </div>
                    <br>
                    <div class="form-group">
                        <label for="password" class="form-label">Password</label>
                        <br>
                        <input type="password" class="form-control" id="password" placeholder="Password">
                    </div>
                </form>
            </slot>
        </section>

        <footer class="modal-footer">
            <slot name="footer">

            </slot>
            <button type="button" class="btn-purple" @click="close">
                Sign Up
            </button>
        </footer>

    </div>
  </div>
</template>

<script>
  export default {
    name: 'Modal',
    methods: {
      close() {
        this.$emit('close');
      },
    },
  };
</script>


<style>
  .modal-backdrop {
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: rgba(0, 0, 0, 0.3);
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .modal {
    background: #FFFFFF;
    box-shadow: 2px 2px 20px 1px;
    overflow-x: auto;
    display: flex;
    flex-direction: column;
  }

  .modal-header,
  .modal-footer {
    padding: 15px;
    display: flex;
  }

  .modal-header {
    position: relative;
    border-bottom: 1px solid #eeeeee;
    color: #6c63ff;
    justify-content: space-between;
  }

  .modal-footer {
    border-top: 1px solid #eeeeee;
    flex-direction: column;
    justify-content: flex-end;
  }

  .modal-body {
    position: relative;
    padding: 20px 10px;
    margin: 10px 25px;
  }

.form-label {
    font-size: 14px;
    font-weight: bold;
    text-transform: uppercase;
}

  .form-control {
    padding: 10px;
  }

.form-control:focus {
    outline: none;
}

  .btn-close {
    position: absolute;
    top: 0;
    right: 0;
    border: none;
    font-size: 20px;
    padding: 10px;
    cursor: pointer;
    font-weight: bold;
    color: #6c63ff;
    background: transparent;
  }

  .btn-purple {
    color: white;
    background: #6c63ff;
    border: 1px solid #6c63ff;
    border-radius: 2px;
    padding: 8px;
  }

.btn-purple:hover {
    background: #4e48c0;
    cursor: pointer;
}
</style>