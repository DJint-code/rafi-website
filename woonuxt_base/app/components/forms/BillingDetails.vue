<script lang="ts" setup>
const { updateShippingLocation } = useCheckout();
const { isBillingAddressEnabled } = useCart();

const props = defineProps({
  modelValue: { type: Object, required: true },
});

const billing = toRef(props, 'modelValue');
</script>

<template>
  <div class="grid w-full gap-4 lg:grid-cols-2">
    <div class="w-full">
      <label for="first-name">{{ $t('messages.billing.firstName') }}</label>
      <input id="first-name" v-model="billing.firstName" placeholder="" autocomplete="given-name" type="text" required />
    </div>

    <div class="w-full">
      <label for="last-name">{{ $t('messages.billing.lastName') }}</label>
      <input id="last-name" v-model="billing.lastName" placeholder="" autocomplete="family-name" type="text" required />
    </div>

    <div v-if="isBillingAddressEnabled" class="w-full col-span-full">
      <label for="address1">{{ $t('messages.billing.address1') }}</label>
      <input id="address1" v-model="billing.address1" placeholder="" autocomplete="street-address" type="text" required />
    </div>

    <div v-if="isBillingAddressEnabled" class="w-full col-span-full">
      <label for="address2">{{ $t('messages.billing.address2') }} ({{ $t('messages.general.optional') }})</label>
      <input id="address2" v-model="billing.address2" placeholder="" autocomplete="address-line2" type="text" />
    </div>

    <div v-if="isBillingAddressEnabled" class="w-full">
      <label for="city">{{ $t('messages.billing.city') }}</label>
      <input id="city" v-model="billing.city" placeholder="" autocomplete="locality" type="text" required />
    </div>

    <div v-if="isBillingAddressEnabled" class="w-full">
      <label for="zip">{{ $t('messages.billing.zip') }}</label>
      <input id="zip" v-model="billing.postcode" placeholder="" autocomplete="postal-code" type="text" required />
    </div>

    <div v-if="isBillingAddressEnabled" class="w-full col-span-full">
      <label for="phone">{{ $t('messages.billing.phone') }}</label>
      <input id="phone" v-model="billing.phone" placeholder="" autocomplete="tel" type="tel" required />
    </div>
  </div>
</template>
