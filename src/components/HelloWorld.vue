<template>
  <v-container class="month">
    <v-row>
      <v-col cols="6">
        <h2 class="mb-6">GROSS MONTHLY INCOME</h2>
        <v-row>
          <v-col cols="8">
            <v-subheader>Wages</v-subheader>
          </v-col>
          <v-col cols="4">
            <v-text-field
              label="Amount"
              v-model="grossMonthly.wages"
              placeholder="10"
              prefix="$"
            ></v-text-field>
          </v-col>
          <v-slider
            hint="Im a hint"
            max="200000"
            min="0"
            v-model="grossMonthly.wages"
          ></v-slider>
        </v-row>
        <v-row>
          <v-col cols="8">
            <v-subheader>Salaries</v-subheader>
          </v-col>
          <v-col cols="4">
            <v-text-field
              label="Amount"
              v-model="grossMonthly.salaries"
              placeholder="28.00"
              prefix="$"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="8">
            <v-subheader>Tips and bonuses</v-subheader>
          </v-col>
          <v-col cols="4">
            <v-text-field
              label="Amount"
              v-model="grossMonthly.tipsBonus"
              placeholder="28.00"
              prefix="$"
            ></v-text-field>
          </v-col>
        </v-row>
        <h2 class="mb-6">Social Security</h2>
        <v-row>
          <v-col cols="8">
            <v-subheader>Child support and alimony</v-subheader>
          </v-col>
          <v-col cols="4">
            <v-text-field
              label="Amount"
              v-model="grossMonthly.childSupport"
              placeholder="10"
              prefix="$"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="8">
            <v-subheader>Any other additional income</v-subheader>
          </v-col>
          <v-col cols="4">
            <v-text-field
              label="Amount"
              v-model="grossMonthly.additionalIncome"
              placeholder="28.00"
              prefix="$"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row class="monthIncome">
          <v-col cols="8"> TOTAL MONTHLY INCOME </v-col>
          <v-col cols="4"> ${{ getGrossTotatlly }}</v-col>
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
            <v-text-field
              label="Amount"
              v-model="monthlyExpenses.morgage"
              placeholder="10"
              prefix="$"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="8">
            <v-subheader
              >Monthly expense for real estate taxes (if Escrowed)</v-subheader
            >
          </v-col>
          <v-col cols="4">
            <v-text-field
              label="Amount"
              v-model="monthlyExpenses.realEstate"
              placeholder="28.00"
              prefix="$"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="8">
            <v-subheader>Monthly car payments</v-subheader>
          </v-col>
          <v-col cols="4">
            <v-text-field
              label="Amount"
              v-model="monthlyExpenses.carPayments"
              placeholder="28.00"
              prefix="$"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="8">
            <v-subheader>Monthly student loan payments</v-subheader>
          </v-col>
          <v-col cols="4">
            <v-text-field
              label="Amount"
              v-model="monthlyExpenses.studentLoan"
              placeholder="10"
              prefix="$"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="8">
            <v-subheader>Minimum monthly credit card payments</v-subheader>
          </v-col>
          <v-col cols="4">
            <v-text-field
              label="Amount"
              v-model="monthlyExpenses.creditCard"
              placeholder="28.00"
              prefix="$"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="8">
            <v-subheader>Monthly time share payments</v-subheader>
          </v-col>
          <v-col cols="4">
            <v-text-field
              label="Amount"
              v-model="monthlyExpenses.timeShare"
              placeholder="28.00"
              prefix="$"
            ></v-text-field>
          </v-col>
        </v-row>

        <v-row>
          <v-col cols="8">
            <v-subheader>Monthly personal loan payments</v-subheader>
          </v-col>
          <v-col cols="4">
            <v-text-field
              label="Amount"
              v-model="monthlyExpenses.studentLoan"
              placeholder="28.00"
              prefix="$"
            ></v-text-field>
          </v-col>
        </v-row>

        <v-row>
          <v-col cols="8">
            <v-subheader>Monthly child support payment</v-subheader>
          </v-col>
          <v-col cols="4">
            <v-text-field
              label="Amount"
              v-model="monthlyExpenses.childSupport"
              placeholder="28.00"
              prefix="$"
            ></v-text-field>
          </v-col>
        </v-row>

        <v-row>
          <v-col cols="8">
            <v-subheader>Monthly alimony payment</v-subheader>
          </v-col>
          <v-col cols="4">
            <v-text-field
              label="Amount"
              v-model="monthlyExpenses.alimonyPayments"
              placeholder="28.00"
              prefix="$"
            ></v-text-field>
          </v-col>
        </v-row>

        <v-row>
          <v-col cols="8">
            <v-subheader>Any Co-Signed Loan monthly payments </v-subheader>
          </v-col>
          <v-col cols="4">
            <v-text-field
              label="Amount"
              v-model="monthlyExpenses.cosingnedLoan"
              placeholder="28.00"
              prefix="$"
            ></v-text-field>
          </v-col>
        </v-row>

        <v-row class="monthexpenses">
          <v-col cols="8"> TOTAL MONTHLY EXPENSES </v-col>
          <v-col cols="4"> $ {{ getMonthlyExpense }}</v-col>
        </v-row>
      </v-col>
    </v-row>

    <v-row class="ditMonth">
      <v-col cols="4"> DTI = </v-col>
      <v-col cols="8" class="monthIncome-low" v-if="getDtiPercentage < 25">
        {{ getDtiPercentage }} %
      </v-col>
      <v-col
        cols="8"
        class="monthIncome-middle"
        v-else-if="getDtiPercentage > 24 && getDtiPercentage < 51"
      >
        {{ getDtiPercentage }} % </v-col
      ><v-col
        cols="8"
        class="monthIncome-high"
        v-else-if="getDtiPercentage > 50"
      >
        {{ getDtiPercentage }} %
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
  name: "HelloWorld",

  data: () => ({
    ecosystem: [
      {
        text: "vuetify-loader",
        href: "https://github.com/vuetifyjs/vuetify-loader/tree/next",
      },
      {
        text: "github",
        href: "https://github.com/vuetifyjs/vuetify/tree/next",
      },
      {
        text: "awesome-vuetify",
        href: "https://github.com/vuetifyjs/awesome-vuetify",
      },
    ],
    importantLinks: [
      {
        text: "Chat",
        href: "https://community.vuetifyjs.com",
      },
      {
        text: "Made with Vuetify",
        href: "https://madewithvuejs.com/vuetify",
      },
      {
        text: "Twitter",
        href: "https://twitter.com/vuetifyjs",
      },
      {
        text: "Articles",
        href: "https://medium.com/vuetify",
      },
    ],
    whatsNext: [
      {
        text: "Explore components",
        href: "https://vuetifyjs.com",
      },
      {
        text: "Roadmap",
        href: "https://vuetifyjs.com/introduction/roadmap/",
      },
      {
        text: "Frequently Asked Questions",
        href: "https://vuetifyjs.com/getting-started/frequently-asked-questions",
      },
    ],

    grossMonthly: {
      wages: 2000,
      salaries: 1,
      tipsBonus: 2,
      childSupport: 4,
      additionalIncome: 5,
      totalMonthly: 0,
    },
    monthlyExpenses: {
      morgage: 500,
      realEstate: 4,
      carPayments: 2,
      studentLoan: 5,
      creditCard: 1,
      timeShare: 1,
      childSupport: 3,
      alimonyPayments: 4,
      cosingnedLoan: 3,
      totalMonthly: 5,
    },
    dti: 0,
  }),

  computed: {
    getGrossTotatlly() {
      let total =
        parseInt(this.grossMonthly.wages) +
        parseInt(this.grossMonthly.salaries) +
        parseInt(this.grossMonthly.tipsBonus) +
        parseInt(this.grossMonthly.childSupport) +
        parseInt(this.grossMonthly.additionalIncome);
      if (total) {
        this.AddTotalMonthly(total);
        return total;
      }
      return 0;
    },

    getMonthlyExpense() {
      let expense =
        parseInt(this.monthlyExpenses.morgage) +
        parseInt(this.monthlyExpenses.realEstate) +
        parseInt(this.monthlyExpenses.carPayments) +
        parseInt(this.monthlyExpenses.studentLoan) +
        parseInt(this.monthlyExpenses.creditCard) +
        parseInt(this.monthlyExpenses.timeShare) +
        parseInt(this.monthlyExpenses.childSupport) +
        parseInt(this.monthlyExpenses.alimonyPayments) +
        parseInt(this.monthlyExpenses.cosingnedLoan);
      if (expense) {
        this.addMonthlyExpenses(expense);
        return expense;
      }
      return 0;
    },

    getDtiPercentage() {
      if (this.grossMonthly.totalMonthly & this.monthlyExpenses.totalMonthly) {
        const percentage = Math.round(
          (this.monthlyExpenses.totalMonthly / this.grossMonthly.totalMonthly) *
            100
        );
        return percentage;
      }
      return "";
    },
  },
  methods: {
    AddTotalMonthly(value) {
      this.grossMonthly.totalMonthly = value;
    },

    addMonthlyExpenses(expense) {
      this.monthlyExpenses.totalMonthly = expense;
    },
  },
};
</script>

<style scoped>
.monthIncome-low {
  background-color: red;
}
.monthIncome-middle {
  background-color: yellow;
}
.monthIncome-high {
  background-color: green;
}
</style>
