<template>
  <div class="swap-container">
    <div class="content-title">
      <h2>{{ $t('reused.swap') }}</h2>
      <img class="icon" src="~@/assets/images/etc/bity.png">
    </div>

    <div class="send-form">
      <div class="form-block amount-to-address">
        <div class="amount">
          <div class="title">
            <h4>{{ $t('reused.from') }}</h4>
          </div>
          <div class="dropdown-select-search-1">
            <v-select :options="['foo','bar']"></v-select>
          </div>
          <div class="the-form amount-number">
            <input type="number" name="" value="" placeholder="Deposit Amount">
          </div>
        </div>
        <div class="exchange-icon">
          <i class="fa fa-exchange" aria-hidden="true"></i>
        </div>
        <div class="amount">
          <div class="title">
            <h4>{{ $t('reused.to') }}</h4>
          </div>
          <div class="dropdown-select-search-1">
            <v-select :options="['foo','bar']"></v-select>
          </div>
          <div class="the-form amount-number">
            <input type="number" name="" value="" placeholder="Received Amount">
          </div>
        </div>
      </div>
    </div>

    <div class="send-form">
      <div class="title-container">
        <div class="title">
          <h4>{{ $t('reused.speedTx') }}</h4>
        </div>
      </div>
      <div class="the-form gas-amount">
        <input type="number" name="" value="" placeholder="Please Enter The Address">
      </div>
    </div>

    <div class="send-form">
      <div class="title-container">
        <div class="title">
          <h4>{{ $t('reused.speedTx') }}<span class="alert-button"></span></h4>
          <p>{{ $t('reused.txFee') }}: 0.000013 ETH ($1.234)</p>
        </div>
        <div class="buttons">
          <div class="small-circle-button-green-border">
            {{ $t('reused.slow') }}
          </div>
          <div class="small-circle-button-green-border active">
            {{ $t('reused.regular') }}
          </div>
          <div class="small-circle-button-green-border">
            {{ $t('reused.fast') }}
          </div>
        </div>
      </div>

      <div class="the-form gas-amount">
        <input type="number" name="" value="" placeholder="Gas Amount">
        <div class="good-button-container">
          <p>Gwei</p>
          <i class="fa fa-check-circle good-button not-good" aria-hidden="true"></i>
        </div>
      </div>
    </div>

    <div class="submit-button-container">
      <h4>1 ETH = 0.000231 BTC</h4>
      <div class="submit-button large-round-button-green-filled clickable">
        {{ $t('reused.continue') }}
      </div>
      <interface-bottom-text link="/" :linkText="$t('interface.learnMore')" :question="$t('interface.haveIssues')"></interface-bottom-text>
    </div>

  </div>
</template>
<script>
import InterfaceBottomText from '@/components/InterfaceBottomText'

export default {
  components: {
    'interface-bottom-text': InterfaceBottomText
  },
  data () {
    return {
    }
  },
  methods: {
    copyAddress () {
      alert('This doesn\'t work for now.')
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "SwapContainer.scss";
</style>
