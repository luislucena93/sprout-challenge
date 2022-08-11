<script>

const validateEmail = (email) => {
    return String(email)
      .toLowerCase()
      .match(
        /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
      );
  };

  export default {
    data() {
      return {
        email: '',
        hasError: false,
        errorMessage: ''
      }
    },
    methods: {
      onInput(e) {
        this.hasError = false;
        this.errorMessage = '';
        this.email = e.target.value;
      },
      onSubscribe() {
        if (this.email === '') {
          this.hasError = true;
          this.errorMessage = 'Oops! Please add your email';
        } else if(validateEmail(this.email) === null) {
          this.hasError = true;
          this.errorMessage = 'Oops! That doesn’t look like an email address'
        }
      }
    }
  }
</script>

<template>
  <div class="subscribe-container">
    <h2>Get notified when we launch</h2>
    <div class="form">
      <input placeholder="Email address" :value="email" @input="onInput" :class="{error: hasError}"/>
      <p class="errorMessage" v-if="hasError">{{errorMessage}}</p>
      <button @click="onSubscribe">Get notified</button>
    </div>
  </div>
</template>

<style>
  .subscribe-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 145px 24px 164px 24px;
  }

  .subscribe-container h2 {
    font-weight: 800;
    font-size: 24px;
    line-height: 33px;
    padding: 0 24px;
    text-align: center;
    margin-bottom: 31px;
  }

  .form {
    display: flex;
    flex-direction: column;
    width: 100%;
  }

  .errorMessage {
    font-weight: 500;
    font-size: 12px;
    line-height: 25px;
    position: absolute;
    top: 25px;
    left: 15px;
    color: var(--color-error);
  }


  .form input {
    width: 100%;
    background-color: var(--color-light-blue);
    border: none;
    padding: 12px 18px;
    margin-bottom: 24px;
    border-radius: 24px;
    color: white;
    font-weight: 800;
    font-size: 15px;
    line-height: 25px;
  }

  .form .error {
    border: 2px solid var(--color-error);
    padding: 10px 16px;
  }

  .form input:focus {
    outline: none;
  }

  .form button {
    width: 100%;
    padding: 12px 18px;
    border-radius: 24px;
    background-color: var(--color-secondary);
    color: var(--color-light-blue);
    font-weight: 800;
    font-size: 15px;
    line-height: 25px;
  }

  .form button:hover {
    background-color: transparent;
    border: 2px solid var(--color-secondary);
    color: white;
  }

  @media (min-width:480px) {
    .form {
      max-width: 476px;
      flex-direction: row;
    }

    .form button {
      width: 40%;
      height: 48px;
      margin-left: 16px;
    }
  }

</style>