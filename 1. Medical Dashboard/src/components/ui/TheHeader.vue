<template>
  <div class="header">
    <div class="search-field">
      <img src="../../assets/search.svg" class="search-icon" />
      <input
        type="search"
        class="search"
        id="search"
        placeholder="Search Anything"
      />
    </div>
    <img src="../../assets/notification.svg" alt="bell" class="bell-icon" />
  </div>
</template>

<style lang="scss" scoped>
.header {
  position: relative;
  display: flex;
  justify-content: space-between;
}

.search-field {
  position: relative;
}

.bell-icon {
  margin-right: 2rem;

  &:hover {
    cursor: pointer;
  }
}

.search-icon {
  position: absolute;
  transform: translate(-50%, -50%);
  left: 8%;
  top: 50%;
}

.search {
  width: 388px;
  height: 48px;
  background: #ffffff;
  border: 1px solid #f2f2fd;
  box-sizing: border-box;
  border-radius: 40px;
  padding: 0 2rem 0 5.6rem;
  font-size: 1.4rem;
  letter-spacing: 0.02em;
  transition: border-color 0.3s ease;

  &:active,
  &:focus {
    outline: none;
    border-color: var(--primary-color-1);
  }

  &::placeholder {
    color: #b1b1c9;
  }
}
</style>
