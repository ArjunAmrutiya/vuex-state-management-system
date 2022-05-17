<template>
  <v-app>
    <v-app-bar color="primary" density="compact">
      <v-app-bar-title>Vuex State Management</v-app-bar-title>

      <template v-slot:append>
        <v-btn icon="mdi-dots-vertical"></v-btn>
      </template>
    </v-app-bar>

    <v-main>
      <v-container class="d-flex justify-center">
        <v-col cols="12" sm="12" md="12" lg="10" xl="8">
          <v-card>
            <v-card-title>Create User</v-card-title>
            <form ref="userform">
              <v-col cols="12">
                <v-row>
                  <v-col cols="12" xl="4">
                    <v-text-field
                      v-model="fname"
                      label="First name"
                      hide-details="auto"
                      color="primary"
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" xl="4">
                    <v-text-field
                      v-model="mname"
                      label="Middle name"
                      hide-details="auto"
                      color="primary"
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" xl="4">
                    <v-text-field
                      v-model="lname"
                      label="Last name"
                      hide-details="auto"
                      color="primary"
                    ></v-text-field>
                  </v-col>
                  <v-col cols="6" xl="6">
                    <v-text-field
                      v-model="email"
                      label="Email Address"
                      hide-details="auto"
                      color="primary"
                    ></v-text-field>
                  </v-col>
                  <v-col cols="6" xl="6">
                    <v-text-field
                      v-model="phone"
                      label="Mobile no"
                      hide-details="auto"
                      color="primary"
                    ></v-text-field>
                  </v-col>
                  <v-col cols="6">
                    <v-textarea
                      v-model="address"
                      rows="2"
                      label="Address"
                      hide-details="auto"
                      color="primary"
                    ></v-textarea>
                  </v-col>
                  <v-col cols="6">
                    <v-textarea
                      v-model="bio"
                      rows="2"
                      label="Bio"
                      hide-details="auto"
                      color="primary"
                    ></v-textarea>
                  </v-col>
                  <v-col cols="4">
                    <v-select
                      v-model="country"
                      :items="countryList"
                      label="Country"
                      hide-details
                    ></v-select>
                  </v-col>
                  <v-col cols="4">
                    <v-select
                      v-model="state"
                      :items="stateList"
                      label="State"
                      hide-details
                    ></v-select>
                  </v-col>
                  <v-col cols="4">
                    <v-select
                      v-model="city"
                      :items="cityList"
                      label="City"
                      hide-details
                    ></v-select>
                  </v-col>
                </v-row>
                <v-card-actions class="justify-end">
                  <v-btn
                    small
                    color="primary"
                    variant="contained-flat"
                    @click.stop="submit"
                    >Submit</v-btn
                  >
                </v-card-actions>
              </v-col>
            </form>
          </v-card>
        </v-col>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "AppPage",
  data() {
    return {
      countryList: ["india", "U.S", "United Kingdom"],
      stateList: ["Gujarat", "Delhi", "Goa"],
      cityList: ["Rajkot", "Surat", "Ahmedabad"],

      fname: "",
      mname: "",
      lname: "",
      email: "",
      phone: "",
      address: "",
      bio: "",
      country: "",
      state: "",
      city: "",
    };
  },
  methods: {
    submit() {
      alert('click');
    },
  },
};
</script>
