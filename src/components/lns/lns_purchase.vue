<template>
  <div class="lns-purchase">
    <div class="q-mb-lg q-px-md q-pt-md">
      <div class="tab-desc">
        {{ $t("strings.lnsPurchaseDescription") }}
      </div>
      <div class="prices">
        {{ $t("strings.lns.prices") }}
        <table>
          <tr>
            <td>{{ $t("strings.lns.sessionID") }}:</td>
            <td>15 QMR</td>
          </tr>
        </table>
      </div>
      <LNSInput ref="input" />
    </div>
  </div>
</template>

<script>
import LNSInput from "./lns_input";
export default {
  name: "LNSPurchase",
  components: {
    LNSInput
  },
  methods: {
    startUpdating(record) {
      this.$refs.input.startUpdating(record);
    },
    startRenewing(record) {
      this.$refs.input.startRenewing(record);
    }
  }
};
</script>
<style lang="scss">
.lns-purchase {
  .description {
    white-space: pre-line;
    // quenero-navy
    color: #1f1c47;
  }

  .prices {
    // quenero-navy
    margin-top: 20px;
    color: #1f1c47;
  }
}
</style>
