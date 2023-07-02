<template>
    <v-row justify="center">
    <div class="form-section d-flex justify-center align-center">
        <v-col align="center">
            <h2>Try Figma for free</h2>

            <v-form v-model="valid">
                <v-col align="center">
                    <v-text-field v-model="email" :rules="emailRules" label="Email" required></v-text-field>

                    <v-text-field v-model="password" :rules="passwordRules" label="Password" required></v-text-field>
            <v-btn outlined color="black" style="margin: 20px 0;">
                    Create account
            </v-btn>
           <p align="center"><small>By clicking "Create account" or "Continue with Google", you agree to the <a>Figma TOS</a> and <a>Privacy Policy</a>.</small></p>
           <p align="center"><a>Use single sign-on</a></p>
           <p align="center">Already have an account?<a>Log in</a></p>
        </v-col>
        </v-form>
        </v-col>

    </div>
</v-row>
</template>

<style scoped>
.form-section {
    height: 95vh;
    max-width: 400px;
}
</style>

<script>
  export default {
    data: () => ({
      valid: false,
      email: '',
      emailRules: [
        value => {
          if (value) return true

          return 'E-mail is requred.'
        },
        value => {
          if (/.+@.+\..+/.test(value)) return true

          return 'E-mail must be valid.'
        },
      ],
      password: '',
      passwordRules: [
        value => {
          if (value) return true

          return 'Password requred.'
        },
        value => {
            if (value?.length < 6) return true

          return 'Password must not be less than 6 chars'
        },
      ],
    }),
  }
</script>