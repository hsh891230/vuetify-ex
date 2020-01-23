<template>
  <v-container fluid>
    <v-row dense>
      <v-col cols="9">
        총 비용
      </v-col>
      <v-col cols="3" class="text-right">
        ￦100,000
      </v-col>
      <v-col cols="12">
        <v-divider></v-divider>
        <v-row dense>
          <v-col cols="9">
            여행 준비 비용
          </v-col>
          <v-col cols="3" class="text-right">
            ￦40,000
          </v-col>
          <v-col cols="12">
            <v-divider></v-divider>
            <v-row dense v-for="i in 2" :key="i">
              <v-col cols="9" class="pl-4">
                내용 {{ i }}
              </v-col>
              <v-col cols="3" class="text-right">
                ￦40,000
              </v-col>
            </v-row>
            <v-row dense>
              <v-col offset="9" class="text-right">
                <v-btn x-small>비용 추가</v-btn>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
        <v-divider></v-divider>
        <v-row dense>
          <v-col cols="9">
            Day 1
          </v-col>
          <v-col cols="3" class="text-right">
            ￦40,000
          </v-col>
          <v-col cols="12">
            <v-divider></v-divider>
            <v-row dense v-for="i in 2" :key="i">
              <v-col cols="9" class="pl-4">
                내용 {{ i }}
              </v-col>
              <v-col cols="3" class="text-right">
                ￦40,000
              </v-col>
            </v-row>
            <v-row dense>
              <v-col offset="9" class="text-right">
                <v-btn x-small>비용 추가</v-btn>
              </v-col>
            </v-row>
          </v-col>
          <v-col cols="12">
            <v-row dense>
              <v-col cols="9" class="pl-4" v-ripple @click="show = !show">
                장소별
                <v-icon v-if="show">mdi-menu-down</v-icon>
                <v-icon v-else>mdi-menu-up</v-icon>
              </v-col>
              <v-col cols="3" class="text-right">
                ￦40,000
              </v-col>
              <v-col cols="12" v-show="show">
                <v-divider></v-divider>
                <v-row dense v-for="i in 3" :key="i">
                  <v-col cols="9" class="pl-8">
                    장소 - {{ i }}
                  </v-col>
                  <v-col cols="3" class="text-right">
                    ￦40,000
                  </v-col>
                  <v-col offset="9" class="text-right">
                    ￦10,000
                  </v-col>
                  <v-col offset="9" class="text-right">
                    <v-btn x-small>비용 추가</v-btn>
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: () => ({
    show: false
  }),
};
</script>
