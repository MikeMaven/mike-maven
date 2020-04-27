<template>
  <div
    class="section section-signup"
    style="background-image: url('img/bg11.jpg'); background-size: cover; background-position: top center; min-height: 700px;"
  >
    <div class="container">
      <div class="row">
        <card class="card-signup" header-classes="text-center" color="orange">
          <template slot="header">
            <h3 class="card-title title-up">JOIN THE JOURNEY</h3>
          </template>
          <template>
            <form name="email-list">
              <fg-input
                name="name"
                v-model="name"
                class="no-border"
                placeholder="Full Name"
                addon-left-icon="now-ui-icons users_circle-08"
              >
              </fg-input>

              <fg-input
                name="email"
                v-model="email"
                class="no-border"
                placeholder="Email"
                addon-left-icon="now-ui-icons ui-1_email-85"
              >
              </fg-input>
            </form>
          </template>
          <div class="card-footer text-center">
            <n-button @click="submitForm" type="neutral" round size="lg">Take Me To The Dreamworld</n-button>
          </div>
        </card>
      </div>
    </div>
    <modal
      :show.sync="modals.mini"
      class="modal-primary"
      :show-close="false"
      headerClasses="justify-content-center"
      type="mini"
    >
      <div slot="header" class="modal-profile">
        <i class="now-ui-icons tech_controller-modern"></i>
      </div>
      <p>
        Thanks! We'll keep you updated with all our deepest secrets.
      </p>
      <template slot="footer">
        <n-button type="neutral" link @click.native="modals.mini = false"
          >Close</n-button
        >
      </template>
    </modal>
  </div>
</template>
<script>
import axios from 'axios';
import { Card, FormGroupInput, Button, Modal } from '@/components';

export default {
  components: {
    Card,
    Modal,
    [Button.name]: Button,
    [FormGroupInput.name]: FormGroupInput
  },
  data() {
    return {
      formUrl: 'https://script.google.com/macros/s/AKfycbwtBsiooI7vpEsnaR-qbsXQmRSlCJnYJszA1fG8SDsAGHeTiz0/exec',
      name: null,
      email: null,
      modals: {
        mini: false
      }
    }
  },
  methods: {
    submitForm () {
      let form = document.forms["email-list"]
      let vm = this;
      axios.post(this.formUrl, new FormData(form)).then( response => {
        vm.modals.mini = true;
      });
    }
  }
};
</script>
<style></style>
