<script setup>
import TicketList from "./TicketList.vue";
const tickets = [
  {
    tn: "a123",
    cn: "01",
  },
  {
    tn: "a123",
    cn: "10",
  },
  {
    tn: "a123",
    cn: "01",
  },
  {
    tn: "a123",
    cn: "01",
  },
  {
    tn: "a123",
    cn: "01",
  },
  {
    tn: "a123",
    cn: "01",
  },
  {
    tn: "a123",
    cn: "01",
  },
  {
    tn: "a123",
    cn: "01",
  },
  {
    tn: "a123",
    cn: "01",
  },
  {
    tn: "a123",
    cn: "88",
  },
];
</script>

<template>
  <div class="flex h-screen bg-gray-50">
    <div class="w-1/3 overflow-scroll">
      <TicketList
        v-for="(t, index) in tickets"
        v-bind:key="t"
        :ticket-no="t.tn"
        :counter-no="index + 1"
      />
    </div>
    <div class="w-2/3">
      <div
        style="height: calc(100vh - 190px)"
        class="m-4 bg-blue-300 p-2 h-4/5 rounded-lg"
      ></div>
      <div class="flex">
        <div
          style="height: 121.46px; width: 121.46px"
          class="w-1/3 rounded-lg shadow overflow-hidden mt-4 ml-4"
        >
          <img
            style="height: 121.46px; width: 121.46px"
            src="https://static.dezeen.com/uploads/2019/09/volkswagen-electric-id-rebrand-design_dezeen_2364_col_12.gif"
            alt="logo"
          />
        </div>
        <TicketList
          lt="teal"
          style="width: 350px"
          ticket-no="abcd"
          :counter-no="tickets[1].cn"
        />
        <TicketList
          lt="teal"
          style="width: 350px"
          ticket-no="dcba"
          :counter-no="tickets.length"
        />
      </div>
    </div>
  </div>
</template>

<style></style>
