<template>
<section>
      
      <h1>Add Dog</h1>
      
  <div>
    <b-form @submit="onSubmit" @reset="onReset" v-if="show">
      <b-form-group id="exampleInputGroup1"
                    label="Name:"
                    label-for="exampleInput1"
                    >
        <b-form-input id="exampleInput1"
                      type="text"
                      v-model="form.name"
                      required
                      placeholder="Enter name">
        </b-form-input>
      </b-form-group>
      <b-form-group id="exampleInputGroup2"
                    label="Race:"
                    label-for="exampleInput2">
        <b-form-input id="exampleInput2"
                      type="text"
                      v-model="form.race"
                      required
                      placeholder="Enter race">
        </b-form-input>
      </b-form-group>
       <b-form-group id="exampleInputGroup2"
                    label="Birthdate:"
                    label-for="exampleInput2">
        <b-form-input id="exampleInput2"
                      type="date"
                      v-model="form.birthdate"
                      required
                      placeholder="Enter birthdate">
        </b-form-input>
      </b-form-group>
      
      <b-button type="submit" variant="primary">Submit</b-button>
      <b-button type="reset" variant="danger">Reset</b-button>
    </b-form>
  </div>
</section>
</template>

<script>

export default {
    name:'AddDog',
  data () {
    return {
      form: {
        
        name: '',
        race: '',
        birthdate: ''
      },
      
      show: true
    }
  },
  methods: {
    onSubmit (evt) {
      evt.preventDefault();
      alert(JSON.stringify(this.form));
    },
    onReset (evt) {
      evt.preventDefault();
      /* Reset our form values */
      
      this.form.name = '';
      this.form.race = '';
      this.form.birthdate = '';
      /* Trick to reset/clear native browser form validation state */
      this.show = false;
      this.$nextTick(() => { this.show = true });
    }
  }
}
</script>