<template>
  <v-card>
    <v-card-title class="primary">
      {{ $t('junta') }}
    </v-card-title>
    <v-card-text>
      <v-list disabled>
        <v-list-item-group color="primary">
          <v-list-item v-for="item in items"
                       :key="item.role">
            <v-list-item-content>
              <v-list-item-title class="font-weight-bold">
                {{ $t(item.role) }}
              </v-list-item-title>
              <div v-for="(person, index) in item.who"
                   :key="index">
                {{ person }}
              </div>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    items: [
      { role: 'presidenta', who: ['Mercè A.'] },
      { role: 'vicepresidenta', who: ['Laura L.'] },
      { role: 'tresorer', who: ['Mariona P.'] },
    ],
  }),
};
</script>

<i18n>
en:
  junta: "Board"
  presidenta: "President"
  vicepresidenta: "Vice-President"
  tresorer: "Treasury"
  secretari: "Secretary"
de:
  junta: "Vorstand"
  presidenta: "Vorsitzende"
  vicepresidenta: "Stellvertretende Vorsitzende"
  tresorer: "Schatzmeister"
  secretari: "Geschäftsführerin"
ca:
  junta: "Junta"
  presidenta: "Presidenta"
  vicepresidenta: "Vicepresidenta"
  tresorer: "Tresorer"
  secretari: "Secretària"
</i18n>
