<template>
    <div>
        <base-header type="gradient-success" class="pb-6 pb-8 pt-5 pt-md-8">
            <!-- Card stats -->
            <div class="row">
                <div class="col-xl-3 col-lg-6">
                    <stats-card title="Accounts"
                                type="gradient-red"
                                v-bind:sub-title="myJson.accounts_count"
                                icon="ni ni-active-40"
                                class="mb-4 mb-xl-0">
                    </stats-card>
                </div>
                <div class="col-xl-3 col-lg-6">
                    <stats-card title="Total traffic"
                                type="gradient-orange"
                                sub-title="2,356"
                                icon="ni ni-chart-pie-35"
                                class="mb-4 mb-xl-0">

                    </stats-card>
                </div>
                <div class="col-xl-3 col-lg-6">
                    <stats-card title="Sales"
                                type="gradient-green"
                                sub-title="924"
                                icon="ni ni-money-coins"
                                class="mb-4 mb-xl-0">

                    </stats-card>

                </div>
                <div class="col-xl-3 col-lg-6">
                    <stats-card title="Performance"
                                type="gradient-info"
                                sub-title="49,65%"
                                icon="ni ni-chart-bar-32"
                                class="mb-4 mb-xl-0">

                    </stats-card>
                </div>
            </div>
        </base-header>

        <div class="container-fluid mt--7">
            <div class="row">
                <div class="col">
                    <projects-table title="Light Table"></projects-table>
                </div>
            </div>
            <div class="row mt-5">
                <div class="col">
                    <projects-table type="dark" title="Dark Table"></projects-table>
                </div>
            </div>
        </div>

    </div>
</template>
<script>
  import ProjectsTable from './Tables/ProjectsTable'
  import json from '../../json/transactions'

  export default {
    name: 'tables',
    components: {
      ProjectsTable
    },
      data() {
          return {
              myJson: json,
              myJsonCredits: json.transaction_details,
              myJsonDebits: json
          }
      }
  };
</script>
<style></style>
