<template>
  <div class="card">
    <div class="card-header border-0">
      <div class="row align-items-center">
        <div class="col">
          <h3 class="mb-0">Accounts summary</h3>
        </div>
        <div class="col text-right">
          <a href="#!" class="btn btn-sm btn-primary">See all</a>
        </div>
      </div>
    </div>

    <div class="table-responsive">
      <base-table thead-classes="thead-light"
                  :data="myJson">
        <template slot="columns">
          <th>Account number</th>
          <th>Bank name</th>
          <th>Bank balance</th>
          <th>Credit frequency</th>
          <th>Debit frequency</th>
          <th>Open date</th>
          <th>Last credit date</th>
          <th>Last debit date</th>
        </template>

        <template slot-scope="{row}">
          <th scope="row">
            {{row.accNo}}
          </th>
          <td>
            {{row.bankName}}
          </td>
          <td>
            Ksh. {{row.bankBalance}}
          </td>
          <td>
            {{row.creditFrequency}}
          </td>
          <td>
            {{row.debitFrequency}}
          </td>
          <td>
            {{row.openDate}}
          </td>
          <td>
            {{row.activityDatesDetails.lastCreditDate}}
          </td>
          <td>
            {{row.activityDatesDetails.lastDebitDate}}
          </td>
        </template>

      </base-table>
    </div>

  </div>
</template>
<script>
  import json from '../../../json/accounts'
  export default {
    name: 'page-visits-table',
    data() {
      return {
        myJson: json.accounts_details,
        tableData: [
          {
            page: '/argon/',
            visitors: '4,569',
            unique: '340',
            bounceRate: '46,53%',
            bounceRateDirection: 'up'
          },
          {
            page: '/argon/index.html',
            visitors: '3,985',
            unique: '319',
            bounceRate: '46,53%',
            bounceRateDirection: 'down'
          },
          {
            page: '/argon/charts.html',
            visitors: '3,513',
            unique: '294',
            bounceRate: '36,49%',
            bounceRateDirection: 'down'
          },
          {
            page: '/argon/tables.html',
            visitors: '2,050',
            unique: '147',
            bounceRate: '50,87%',
            bounceRateDirection: 'up'
          },
          {
            page: '/argon/profile.html',
            visitors: '1,795',
            unique: '190',
            bounceRate: '46,53%',
            bounceRateDirection: 'down'
          }
        ]
      }
    }
  }
</script>
<style>
</style>
