<template>
  <div class="field">
    <!-- <div class="label">
      {{ $t('relayerTotal.label') }}
    </div> -->
    <div class="withdraw-data">
      <!-- <div class="withdraw-data-item">
        {{ $t('relayerTotal.name') }}
        <span>{{ relayerName }}</span>
      </div> -->
      <div class="withdraw-data-item">
        {{ $t('relayerTotal.fee') }}
        <!-- <span>{{ selectedRelayer.tornadoServiceFee }}%</span> -->
<<<<<<< HEAD
        <span>1%</span>
=======
        <span>2%</span>
>>>>>>> 95c13a08109fe71f23578455200c086c1e2cbcca
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  computed: {
    ...mapState('relayer', ['selectedRelayer']),
    relayerName() {
      const { name, url } = this.selectedRelayer

      if (name === 'custom') {
        return url.replace(/http(s)?|:|\//g, '')
      }

      return name
    }
  }
}
</script>
