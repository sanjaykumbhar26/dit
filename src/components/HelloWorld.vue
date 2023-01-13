
<template >
<v-container class="month">
   <v-row>
    <v-col cols="6">
       <h2 class="mb-6">GROSS MONTHLY INCOME</h2>
      <v-row>
        <v-col cols="8">
          <v-subheader>Wages</v-subheader>
        </v-col>
        <v-col cols="4">
          <v-text-field label="Amount" placeholder="10" prefix="$"></v-text-field>
        </v-col>
        <v-range-slider hint="Im a hint" max="100" min="-100"></v-range-slider>

      </v-row>
      <v-row>
        <v-col cols="8">
          <v-subheader>Salaries</v-subheader>
        </v-col>
        <v-col cols="4">
          <v-text-field label="Amount" placeholder="28.00" prefix="$"></v-text-field>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="8">
          <v-subheader>Tips and bonuses</v-subheader>
        </v-col>
        <v-col cols="4">
         <v-text-field label="Amount" placeholder="28.00" prefix="$"></v-text-field>
        </v-col>
      </v-row>
      <h2 class="mb-6">Social Security </h2>
        <v-row>
          <v-col cols="8">
            <v-subheader>Child support and alimony</v-subheader>
          </v-col>
          <v-col cols="4">
            <v-text-field label="Amount" placeholder="10" prefix="$"></v-text-field>
          </v-col>
        </v-row>
      <v-row>
        <v-col cols="8">
          <v-subheader>Any other additional income</v-subheader>
        </v-col>
        <v-col cols="4">
          <v-text-field label="Amount" placeholder="28.00" prefix="$"></v-text-field>
        </v-col>
      </v-row>
        <v-row class="monthIncome">
          <v-col cols="8"> TOTAL MONTHLY INCOME </v-col>
          <v-col cols="4"> $ 20020.00 </v-col>
        </v-row>
      
     </v-col>
     <!-- --- -->
      <v-col cols="6">

       <h2 class="mb-6">MONTHLY EXPENSES</h2>
      <v-row>
        <v-col cols="8">
          <v-subheader>Monthly mortgage payments (or rent)</v-subheader>
        </v-col>
        <v-col cols="4">
          <v-text-field label="Amount" placeholder="10" prefix="$"></v-text-field>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="8">
          <v-subheader>Monthly expense for real estate taxes (if Escrowed)</v-subheader>
        </v-col>
        <v-col cols="4">
          <v-text-field label="Amount" placeholder="28.00" prefix="$"></v-text-field>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="8">
          <v-subheader>Monthly car payments</v-subheader>
        </v-col>
        <v-col cols="4">
         <v-text-field label="Amount" placeholder="28.00" prefix="$"></v-text-field>
        </v-col>
      </v-row>
        <v-row>
          <v-col cols="8">
            <v-subheader>Monthly student loan payments</v-subheader>
          </v-col>
          <v-col cols="4">
            <v-text-field label="Amount" placeholder="10" prefix="$"></v-text-field>
          </v-col>
        </v-row>
      <v-row>
        <v-col cols="8">
          <v-subheader>Minimum monthly credit card payments</v-subheader>
        </v-col>
        <v-col cols="4">
          <v-text-field label="Amount" placeholder="28.00" prefix="$"></v-text-field>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="8">
          <v-subheader>Monthly time share payments</v-subheader>
        </v-col>
        <v-col cols="4">
          <v-text-field label="Amount" placeholder="28.00" prefix="$"></v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="8">
          <v-subheader>Monthly personal loan payments</v-subheader>
        </v-col>
        <v-col cols="4">
          <v-text-field label="Amount" placeholder="28.00" prefix="$"></v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="8">
          <v-subheader>Monthly child support payment</v-subheader>
        </v-col>
        <v-col cols="4">
          <v-text-field label="Amount" placeholder="28.00" prefix="$"></v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="8">
          <v-subheader>Monthly alimony payment</v-subheader>
        </v-col>
        <v-col cols="4">
          <v-text-field label="Amount" placeholder="28.00" prefix="$"></v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="8">
          <v-subheader>Any Co-Signed Loan monthly payments  </v-subheader>
        </v-col>
        <v-col cols="4">
          <v-text-field label="Amount" placeholder="28.00" prefix="$"></v-text-field>
        </v-col>
      </v-row>


      <v-row class="monthexpenses">
        <v-col cols="8"> TOTAL MONTHLY EXPENSES </v-col>
        <v-col cols="4"> $ 5063.00 </v-col>
      </v-row>




      
     </v-col>
   </v-row>

  <v-row class="ditMonth">
   <v-col cols="4">
    DTI = 
   </v-col>
   <v-col cols="8" class="monthIncome">
    25.29%
   </v-col>
  </v-row>

  </v-container>
  <!-- <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/logo.svg')"
          class="my-3"
          contain
          height="200"
        />
      </v-col>
      <v-col
        class="mb-5"
        cols="12"
      >
        <h2 class="headline font-weight-bold mb-5">
          What's next?
        </h2>

        <v-row justify="center">
          <a
            v-for="(next, i) in whatsNext"
            :key="i"
            :href="next.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ next.text }}
          </a>
        </v-row>
      </v-col>

      

      <v-col
        class="mb-5"
        cols="12"
      >
        <h2 class="headline font-weight-bold mb-5">
          Ecosystem
        </h2>

        <v-row justify="center">
          <a
            v-for="(eco, i) in ecosystem"
            :key="i"
            :href="eco.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ eco.text }}
          </a>
        </v-row>
      </v-col>
    </v-row>
  </v-container> -->
</template>

<script>

export default {
  name: 'HelloWorld',

  data: () => ({
    ecosystem: [
      {
        text: 'vuetify-loader',
        href: 'https://github.com/vuetifyjs/vuetify-loader/tree/next',
      },
      {
        text: 'github',
        href: 'https://github.com/vuetifyjs/vuetify/tree/next',
      },
      {
        text: 'awesome-vuetify',
        href: 'https://github.com/vuetifyjs/awesome-vuetify',
      },
    ],
    importantLinks: [
      {
        text: 'Chat',
        href: 'https://community.vuetifyjs.com',
      },
      {
        text: 'Made with Vuetify',
        href: 'https://madewithvuejs.com/vuetify',
      },
      {
        text: 'Twitter',
        href: 'https://twitter.com/vuetifyjs',
      },
      {
        text: 'Articles',
        href: 'https://medium.com/vuetify',
      },
    ],
    whatsNext: [
      {
        text: 'Explore components',
        href: 'https://vuetifyjs.com',
      },
      {
        text: 'Roadmap',
        href: 'https://vuetifyjs.com/introduction/roadmap/',
      },
      {
        text: 'Frequently Asked Questions',
        href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions',
      },
    ],
  }),
}
</script>
