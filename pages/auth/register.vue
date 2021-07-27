<template>
	<v-container>
		<v-row justify="center" align="center">
			<v-col cols="8">
				<v-img style="clip-path: circle(37% at 50% 50%);" class="elevation-12" src="/graphic-designer-tools-icon-pattern-background-vector.jpg">
						<v-row justify="center" align="center" class="fill-height" style="background-color: rgba(0, 0, 0, 0.5);">
							<h1 class="white--text">Get Involved</h1>
						</v-row>
					</v-img>
				<v-card dark class="py-12 px-md-6" color="primary" shaped>
					<v-form v-model="valid">
				    <v-container>
				      <v-row>
				        <v-col
				          cols="12"
				        >
				          <v-text-field
				            v-model="firstname"
				            :rules="nameRules"
				            :counter="10"
				            label="First name"
				            required
				            rounded
				            outlined
				          ></v-text-field>
				        </v-col>

				        <v-col
				          cols="12"
				        >
				          <v-text-field
				            v-model="lastname"
				            :rules="nameRules"
				            :counter="10"
				            label="Last name"
				            required
				            rounded
				            outlined
				          ></v-text-field>
				        </v-col>

				        <v-col
				          cols="12"
				        >
				          <v-text-field
				            v-model="email"
				            :rules="emailRules"
				            label="E-mail"
				            required
				            rounded
				            outlined
				          ></v-text-field>
				        </v-col>
				        <v-col
				          cols="12"
				        >
				           <v-select
							      v-model="select"
							      :items="items"
							      :rules="[v => !!v || 'Item is required']"
							      label="Country"
							      required
							      rounded
				            outlined
							    ></v-select>
				        </v-col>
				        <v-col
				          cols="12"
				        >
				          <v-text-field
				            v-model="email"
				            :rules="emailRules"
				            label="Phone Number"
				            required
				            rounded
				            outlined
				          ></v-text-field>
				        </v-col>
				        <v-col
				          cols="12"
				        >
				          <v-text-field
				            v-model="email"
				            :rules="emailRules"
				            label="Password"
				            required
				            rounded
				            outlined
				          ></v-text-field>
				        </v-col>
				        <v-col
				          cols="12"
				        >
				          <v-text-field
				            v-model="email"
				            :rules="emailRules"
				            label="Confirm Password"
				            required
				            rounded
				            outlined
				          ></v-text-field>
				        </v-col>
				        <v-col
				          cols="12"
				        >
				        <p>Gender</p>
				          <v-radio-group v-model="radioGroup">
							      <v-radio
							        label="Male"
							        value="Male"
							      ></v-radio>
							       <v-radio
							        label="Female"
							        value="Female"
							      ></v-radio>
							    </v-radio-group>
				        </v-col>
				        <v-col
				          cols="12"
				        >
				           <v-select
							      v-model="select"
							      :items="items"
							      :rules="[v => !!v || 'Item is required']"
							      label="Role"
							      required
							      rounded
				            outlined
							    ></v-select>
				        </v-col>
				        <v-col
				          cols="12"
				        >
				        <nuxt-link class="white--text" to="/">Do you agree to our terms and policies?</nuxt-link>
				          <v-checkbox
							      v-model="checkbox"
							      label="I Agree?"
							      required
							    ></v-checkbox>
				        </v-col>
				         <v-col
				          cols="12"
				        >
				           <v-btn class="green" fab large>
				           	Register
				           </v-btn>
				        </v-col>
				      </v-row>
				    </v-container>
				  </v-form>
				</v-card>
			</v-col>
		</v-row>
	</v-container>
</template>

<script>
	
  export default {
    data: () => ({
      valid: false,
      checkbox: false,
      firstname: '',
      lastname: '',
      nameRules: [
        v => !!v || 'Name is required',
        v => v.length <= 10 || 'Name must be less than 10 characters',
      ],
      select: null,
      items: [
        'Item 1',
        'Item 2',
        'Item 3',
        'Item 4',
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+/.test(v) || 'E-mail must be valid',
      ],
    }),
  }

</script>

<style lang="css" scoped>
	
</style>