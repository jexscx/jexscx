<template>
  <div>
    <b-button v-b-modal.modal-prevent-closing variant="primary">Add Event</b-button>
    <b-modal
      id="modal-prevent-closing"
      ref="modal"
      title="New event"
      @show="resetModal"
      @hidden="resetModal"
      @ok="handleOk"
    >
      <form ref="form" @submit.stop.prevent="handleSubmit">
        <b-form-group
          :state="nameState"
          label="Name"
          label-for="name-input"
          invalid-feedback="Name is required"
        >
          <b-form-input
            id="name-input"
            v-model="name"
            :state="nameState"
            required
          ></b-form-input>
        </b-form-group>
              <b-form-group id="event-input" label="Event:" label-for="event-input">
        <b-form-select
          id="event-input"
          v-model="form.event"
          :options="events"
          required
        ></b-form-select>
      </b-form-group>
      </form>
    </b-modal>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        form: {
            event: null
            },
            foods: [{ text: 'Select an event', value: null }, '🥳 Birthday', '🍻 Borrel', '🏁 End of ...', '🗓️ Holiday', '🎮 Game night'],
        show: true
      }
    },
    methods: {
      onSubmit(evt) {
        evt.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onReset(evt) {
        evt.preventDefault()
        this.form.food = null
        this.show = false
        this.$nextTick(() => {
          this.show = true
        })
      }
    }
  }
