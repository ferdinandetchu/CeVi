<template>
	<v-container>
		<v-row justify="center" align="center">
			<v-col cols="8">
				<v-img style="clip-path: circle(37% at 50% 50%);" class="elevation-12" src="/graphic-designer-tools-icon-pattern-background-vector.jpg">
						<v-row justify="center" align="center" class="fill-height" style="background-color: rgba(0, 0, 0, 0.5);">
							<h1 class="white--text">Re-Connect</h1>
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
				           <v-btn class="green" fab large>
				           	Login
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