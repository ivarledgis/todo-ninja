<template>
	<div id="login" class="primary">
		<v-container fill-height>
			<v-layout row wrap justify-center>
				<v-flex xs12 sm6 md6 lg5>
					<v-card class="elevation-10 vcardouter my-5">
						<div class="vcardinner">
							<v-card-text pd-0>
								<div class="loginTitle py-4">
									<h1 class="primary--text">Log in</h1>
								</div>
								<v-form>
									<v-text-field class="textfieldsize" solo single-line outline prepend-icon="email" clearable name="email" type="text" placeholder="Email"></v-text-field>
									<v-text-field single-line solo outline prepend-icon="lock" clearable name="password" type="password" placeholder="Password"></v-text-field>
								</v-form>
								<v-layout row wrap class="dark--text">
									<v-flex xs12 md6>
										<v-checkbox label="Remember me" color="primary" value=""></v-checkbox>
									</v-flex>
									<v-flex xs12 md6 hide-details style="text-align: center;">
										<router-link class="subheading" to="/forgetpassword">Forgot password?</router-link>
									</v-flex>
								</v-layout>
							</v-card-text>
							<v-card-actions class="vcardaction mb-3">
								<v-btn class="px-5 py-4 loginbtn" depressed dark large v-bind:color="colorGreen" to="/login">Login</v-btn>
							</v-card-actions>
							<h3 class="make-center">Don't have an account?<router-link to="/signup" class="secondary--text"> Sign up</router-link>
							</h3>
						</div>
					</v-card>
				</v-flex>
			</v-layout>
		</v-container>
	</div>
</template>
<script type="text/javascript">
	export default {
		data() {
			return {
				colorGreen: "#059500"
			}
		}

	}
</script>
<style>
#login {
	text-align: center;
}

#login .vcardouter {
	border-radius: 15px;
	padding-bottom: 40px;
}

#login .vcardinner {
	width: 80%;
    margin: auto;
    padding: auto;
}

#login .textfieldsize {
    height: 70px;
}

#login .v-text-field--outline.v-text-field--single-line input {
    margin-top: 3px;
}

#login .v-text-field.v-text-field--solo:not(.v-text-field--solo-flat) .v-input__slot {
    border: 1px solid;
    border-radius: 9px;
}

#login .v-text-field>.v-input__control>.v-input__slot {
    min-height: 30px;
}

#login .vcardaction {
    justify-content: center;
}

#login .loginbtn {
    border-radius: 10px;
}

#login .v-input--selection-controls {
    margin: 0;
    padding: 0;
}

#login .v-input--selection-controls .v-input__control {
    margin-left: 30px;
}

#login .v-card__text {
    padding: 16px 16px 0px 16px;
}
</style>