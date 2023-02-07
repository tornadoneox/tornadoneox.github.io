<template>
  <b-loading v-model="enabled">
    <div class="loading-container">
<<<<<<< HEAD
      <div class="loading-tornado" data-test="tornado_loader"></div>
=======
      <div class="loading-white" data-test="tornado_loader"></div>
>>>>>>> 95c13a08109fe71f23578455200c086c1e2cbcca
      <div class="loading-message">{{ message }}...</div>
      <approve-loader v-if="isApprove" />
    </div>
  </b-loading>
</template>
<script>
import { mapState, mapGetters } from 'vuex'

import ApproveLoader from './ApproveLoader'

export default {
  components: {
    ApproveLoader
  },
  computed: {
    ...mapGetters('metamask', ['isWalletConnect']),
    ...mapState('metamask', ['providerName']),
    ...mapState('loading', ['enabled', 'message', 'type']),
    isApprove() {
      return this.type === 'approve'
    }
  }
}
</script>
