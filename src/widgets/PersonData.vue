<script setup lang="ts">
const saveContact = () => {
  // Get the contact information from the website
  var contact = {
    name: "Mukhtorkhon Tashkhodjaev, Mr.",
    phone: "",
    email: "mukhtorkhon.tashkhodjaev@gmail.com",
  };
  // create a vcard file
  var vcard =
    "BEGIN:VCARD\nVERSION:4.0\nFN:" +
    contact.name +
    "\nTEL;TYPE=work,voice:" +
    contact.phone +
    "\nEMAIL:" +
    contact.email +
    "\nEND:VCARD";
  var blob = new Blob([vcard], { type: "text/vcard" });
  var url = URL.createObjectURL(blob);

  const newLink = document.createElement("a");
  newLink.download = contact.name + ".vcf";
  newLink.textContent = contact.name;
  newLink.href = url;

  newLink.click();
};
</script>

<template>
  <div class="person-data">
    <h1>Mukhtorkhon Tashkhodjaev, Mr.</h1>
    <p>Deputy Director of the National Agency for Social Protection</p>
    <div class="divider"></div>
    <p>Chairman of the National Paralympic Committee of Uzbekistan</p>
    <div class="divider"></div>
    <p>Vice President of Paralympic Committee Asia</p>
    <button @click="saveContact">Save contact</button>
  </div>
</template>

<style lang="scss" scoped>
.person-data {
  padding: 1.0625rem 0.875rem 1.3125rem 0.875rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  justify-content: center;
  .divider {
    width: 100%;
    height: 0.0625rem;
    background: #ffffff;
    margin: 0.3125rem 0;
  }

  h1 {
    font-size: 1.6rem;
    font-weight: 700;
    margin-bottom: 0.8125rem;
  }

  p {
    font-size: 0.875rem;
  }

  button {
    width: 123px;
    height: 30px;
    font-size: 14px;
    font-weight: 700;
    background: var(--success);
    color: var(--text-color);
    border-radius: 6.25rem;
    margin-top: 1.3125rem;
  }
}
</style>
