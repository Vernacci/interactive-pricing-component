<template>
  <section class="details-container">
    <div class="details wrapper">
      <ul>
        <li>Unlimited websites</li>
        <li>100% data ownership</li>
        <li>Email reports</li>
      </ul>
    </div>
    <div class="wrapper">
      <button class="btn">Start my trial</button>
    </div>
  </section>
</template>

<style scoped>
.details-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  margin-top: 10px;
  gap: 110px;
}

.wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10px;
}

.btn {
  border: none;
  color: var(--lg-blue);
  background-color: var(--dark-blue);
  padding: 20px 50px;
  border-radius: 50px;
  transition: all 0.3s;
}

.btn:hover {
  cursor: pointer;
  color: white;
}

li {
  color: var(--gray-blue);
  list-style-image: url(../images/icon-check.svg);
  margin-bottom: 10px;
  font-size: 15px;
}

@media (max-width: 650px) {
  .details-container {
    grid-template-columns: 1fr;
    gap: 5px;
    margin-top: 0;
  }
}
</style>
