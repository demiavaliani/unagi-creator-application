<template>
	<div>
		<b-container>
			<b-row class="d-flex justify-content-center">
				<!-- left half -->
				<b-col cols="12" md="6" lg="5" class="mr-md-0 mr-lg-5">
					<!-- header -->
					<b-row cols="1" class="justify-content-center greetings">
						<b-col class="b-col">
							<img src="@/assets/images/logo.png" />
						</b-col>

						<b-col class="b-col">
							<p class="greeting mr-2">Ahoy, Arianna</p>
							<img class="waving-hand" src="@/assets/emojis/waving-hand.png" />
						</b-col>

						<b-col cols="12" sm="9" class="b-col mb-md-3 mb-lg-0">
							<p class="p-jost-400 text-center" style="color: #717171">
								To continue with your creator’s profile please provide some additional information
								below. All fields are mandatory ;)
							</p>
						</b-col>
					</b-row>

					<!-- body -->
					<b-form>
						<b-form-row class="justify-content-center">
							<b-col cols="12" sm="11">
								<b-form-group
									id="profiles-group"
									label="LINK TO ONE OF YOUR CURRENT PROFILES"
									label-for="profiles"
									class="lb-sm"
								>
									<b-form-input
										id="profiles"
										type="url"
										placeholder="Instagram, TikTok, YouTube, or other..."
										size="sm"
										v-model="form.profiles"
										required
									></b-form-input>
								</b-form-group>
							</b-col>

							<b-col cols="12" sm="11">
								<b-form-group
									id="username-group"
									label="CHOOSE YOUR USERNAME"
									label-for="username"
									description="At least 3 symbols. Please use only lower case latin letters, numbers, dash(-), hyphen(_), or dot(.)"
									class="lb-sm"
								>
									<b-input-group size="sm">
										<b-input-group-prepend is-text>
											unagi.media/
										</b-input-group-prepend>

										<b-form-input
											id="username"
											type="text"
											size="sm"
											v-model="form.userName"
											required
										>
										</b-form-input>

										<b-input-group-append is-text>
											<div class="d-flex align-items-center">
												<img width="20" src="@/assets/images/check-valid.png" />
											</div>
											<div class="d-flex align-items-center">
												<img width="20" src="@/assets/images/check-invalid.png" />
											</div>
										</b-input-group-append>
									</b-input-group>
								</b-form-group>
							</b-col>

							<b-col cols="12" sm="11">
								<b-form-group
									id="country-group"
									label="COUNTRY OF RESIDENCE"
									label-for="country"
									class="lb-sm"
								>
									<b-form-input
										id="country"
										type="text"
										placeholder="Start typing..."
										size="sm"
										v-model="form.residence"
										required
									>
									</b-form-input>
								</b-form-group>
							</b-col>

							<b-col cols="12" sm="11">
								<b-form-group label="YOUR INTERESTS (PICK 1-3)" id="interests" class="lb-sm">
									<b-form-row>
										<b-col cols="auto" class="b-col"
											><b-form-checkbox
												name="interests-button"
												value="art"
												v-model="form.selected"
												size="sm"
												class="custom-size"
												button
											>
												<p>Art</p>
											</b-form-checkbox></b-col
										>
										<b-col cols="auto" class="b-col"
											><b-form-checkbox
												name="interests-button"
												value="fashion"
												v-model="form.selected"
												size="sm"
												class="custom-size"
												button
											>
												<p>Fashion</p>
											</b-form-checkbox></b-col
										>
										<b-col cols="auto" class="b-col"
											><b-form-checkbox
												name="interests-button"
												value="travel"
												v-model="form.selected"
												size="sm"
												class="custom-size"
												button
											>
												<p>Travel</p>
											</b-form-checkbox></b-col
										>
										<b-col cols="auto" class="b-col"
											><b-form-checkbox
												name="interests-button"
												value="food"
												v-model="form.selected"
												size="sm"
												class="custom-size"
												button
											>
												<p>Food</p>
											</b-form-checkbox></b-col
										>
										<b-col cols="auto" class="b-col"
											><b-form-checkbox
												name="interests-button"
												value="make-up"
												v-model="form.selected"
												size="sm"
												class="custom-size"
												button
											>
												<p>Make-up</p>
											</b-form-checkbox></b-col
										>
										<b-col cols="auto" class="b-col"
											><b-form-checkbox
												name="interests-button"
												value="business"
												v-model="form.selected"
												size="sm"
												class="custom-size"
												button
											>
												<p>Business</p>
											</b-form-checkbox></b-col
										>
										<b-col cols="auto" class="b-col"
											><b-form-checkbox
												name="interests-button"
												value="beauty"
												v-model="form.selected"
												size="sm"
												class="custom-size"
												button
											>
												<p>Beauty</p>
											</b-form-checkbox></b-col
										>
										<b-col cols="auto" class="b-col"
											><b-form-checkbox
												name="interests-button"
												value="health"
												v-model="form.selected"
												size="sm"
												class="custom-size"
												button
											>
												<p>Health</p>
											</b-form-checkbox></b-col
										>
										<b-col cols="auto" class="b-col"
											><b-form-checkbox
												name="interests-button"
												value="fitness"
												v-model="form.selected"
												size="sm"
												class="custom-size"
												button
											>
												<p>Fitness</p>
											</b-form-checkbox></b-col
										>
									</b-form-row>
								</b-form-group>
							</b-col>
						</b-form-row>

						<!-- footer -->
						<b-row class="justify-content-center" cols="1">
							<b-col cols="12" sm="11" class="mb-3">
								<div class="terms-box">
									<b-row cols="1">
										<b-col>
											<p class="p-jost-500">
												<img width="15px" src="@/assets/emojis/pointing-index-finger.png" />
												By applying as a creator you agree to Unagi Media
												<a href="#">Creators Terms Of Service</a>
											</p>
										</b-col>
										<b-col>
											<p class="p-jost-400" style="color: #717171">
												We encourage you to read it carefully. It describes our content and payment
												policies as well as other important issues. There is a short version
												included as well.
											</p>
										</b-col>
									</b-row>
								</div>
							</b-col>
							<b-col cols="12" sm="11">
								<b-button @click="onSubmit" class="submit-btn mb-3 mb-sm-0">
									<p>APPLY AS A CREATOR</p>
								</b-button>
							</b-col>
						</b-row>
					</b-form>
				</b-col>

				<!-- right half -->
				<b-col
					cols="12"
					md="6"
					lg="5"
					class="d-flex justify-content-center align-items-center mr-md-0 mr-lg-5 mr-xl-0 ml-lg-5"
				>
					<div>
						<img class="flamingo" src="@/assets/images/flamingo.png" />
					</div>
				</b-col>
			</b-row>
		</b-container>
	</div>
</template>

<script>
export default {
	name: "ProfileSignUp",

	data() {
		return {
			form: {
				profiles: "",
				userName: "",
				residence: "",
				selected: [],
			},
		};
	},

	methods: {
		onSubmit() {},
	},
};
</script>

<style scoped>
::v-deep #interests .btn {
	border-radius: 10px;
	border: 0;
	background-color: white;
	color: #717171;
}

::v-deep .btn-secondary.active {
	background-color: #717171 !important;
	color: white !important;
}

::v-deep .btn-secondary.focus {
	background-color: white;
	color: #717171;
}

::v-deep small {
	font-size: 12px;
	color: #aeaeae !important;
}

::v-deep label {
	margin-bottom: 7px;
}

p {
	margin-bottom: 0;
}

.p-jost-400 {
	font-size: 12px;
	font-family: "Jost";
	font-weight: 400;
}

.p-jost-500 {
	font-size: 14px;
	font-family: "Jost";
	font-weight: 500;
}

.b-col {
	margin-top: 5px;
	margin-bottom: 5px;
	display: flex;
	justify-content: center;
	align-items: center;
}

.form-control {
	border-radius: 10px;
	font-weight: 500;
}

.input-group-prepend .input-group-text {
	padding-right: 0 !important;
	border-top-left-radius: 10px !important;
	border-bottom-left-radius: 10px !important;
	background-color: white;
	color: #717171;
	font-weight: 500;
}

.input-group-append .input-group-text {
	border-left: 0;
	border-top-right-radius: 10px !important;
	border-bottom-right-radius: 10px !important;
	background-color: white;
}

.lb-sm {
	font-size: 10px;
	font-family: "Jost";
	font-weight: 500;
	color: #717171;
}

.form-control::placeholder {
	color: #aeaeae;
}

.waving-hand {
	width: 1.5rem;
	height: 1.5rem;
}

.greeting {
	font-family: "KyivType";
	font-size: 24px;
}

#username {
	padding-left: 0;
	padding-right: 0;
	border-left: 0;
	border-right: 0;
	color: black;
}

.submit-btn {
	width: 100%;
	height: 45px;
	border-radius: 10px;
	border: 0;
	font-family: "TT Norms";
	font-size: 14px;
	color: white;
	background-color: #ff4200;
}

.submit-btn:hover {
	background-color: #d63700;
}

.submit-btn:active {
	background-color: #d63700 !important;
}

.submit-btn:focus {
	background-color: #ff4200;
}

.terms-box {
	padding: 10px 15px;
	border: 1px solid #d3d3d3;
	border-radius: 10px;
}

.flamingo {
	width: 31vw;
}

@media (max-width: 576px) {
	.greetings {
		margin-bottom: 15px;
	}

	.form-control {
		height: 12vw !important;
	}

	.input-group-prepend {
		height: 12vw;
	}

	.input-group-append {
		height: 12vw;
	}

	::v-deep .custom-size label {
		/* display: flex;
		justify-content: center;
		align-items: center; */
		/* min-width: 2.5vw;
		min-height: 2.6vh; */
		font-size: 15px;
	}

	.flamingo {
		width: 100% !important;
	}
}

@media (max-width: 991.98px) {
	.flamingo {
		width: 45vw;
	}
}

@media (max-width: 1199.98px) {
	.flamingo {
		width: 45vw;
	}
}

@media (max-width: 1199.98px) and (orientation: landscape) {
	.flamingo {
		width: 50vw;
	}
}

@media (min-width: 1200px) {
	.form-control {
		height: 2.7vw !important;
	}

	.input-group-prepend {
		height: 2.7vw;
	}

	.input-group-append {
		height: 2.7vw;
	}

	.form-group {
		margin-bottom: 10px;
	}
}

@media (min-width: 1600px) {
	.greetings {
		margin-bottom: 15px;
	}

	.p-jost-400 {
		font-size: 13px;
	}

	.p-jost-500 {
		font-size: 15px;
	}

	.lb-sm {
		font-size: 11px;
	}

	.submit-btn {
		font-size: 15px;
	}

	::v-deep .custom-size label {
		display: flex;
		justify-content: center;
		align-items: center;
		min-height: 2.6vh;
		font-size: 16px;
	}

	::v-deep small {
		font-size: 13px;
	}

	.form-control {
		height: 2vw !important;
	}

	.input-group-prepend {
		height: 2vw;
	}

	.input-group-append {
		height: 2vw;
	}

	.flamingo {
		width: 22vw !important;
	}
}
</style>
