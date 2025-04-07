<template>
  <header class="menu-container">
    <div class="menu-header flex justify-between items-center p-8">
      <div class="logo">
        <span class="font-bold text-4xl text-gray-950">Daria Antonescu</span>
      </div>

      <!-- Hamburger icon (mobile version) -->
      <div class="hamburger-icon md:hidden" @click="toggleMenu">
        <div :class="{'hamburger': !isOpen, 'close': isOpen}"></div>
        <div :class="{'hamburger': !isOpen, 'close': isOpen}"></div>
        <div :class="{'hamburger': !isOpen, 'close': isOpen}"></div>
      </div>

      <!-- Navigation links (desktop) -->
      <div class="nav-links md:flex hidden">
        <a href="#projects" class="menu-link">Projects</a>
        <a href="#art" class="menu-link">Art</a>
        <a href="#about" class="menu-link">About</a>
        <a href="#contact" class="menu-link">Contact</a>
      </div>
    </div>

    <!-- Mobile menu items (Visible when hamburger is clicked) -->
    <div :class="{'menu-items': true, 'menu-open': isOpen}" class="md:hidden">
      <nav class="flex flex-col items-center py-4 space-y-4 text-lg text-blue-800">
        <a href="#projects" class="menu-link">Projects</a>
        <a href="#art" class="menu-link">Art & Play</a>
        <a href="#about" class="menu-link">About</a>
        <a href="#contact" class="menu-link">Contact</a>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false, // Controls the visibility of the mobile menu
    };
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen; // Toggles the mobile menu visibility
    },
  },
};
</script>

<style scoped>
/* Styling */
.menu-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.menu-container {
  max-width: 100%;
}

.menu-link {
  font-size: 1.5rem;
  text-decoration: none;
  color: #1e3a8a;
  margin: 0 15px;
}

.menu-link:hover {
  text-decoration: underline;
}

/* Hamburger icon styles */
.hamburger-icon div {
  width: 30px;
  height: 3px;
  background-color: #1e3a8a;
  margin: 5px;
  transition: transform 0.3s ease-in-out, opacity 0.3s ease-in-out;
}

/* Hamburger to X transition */
.hamburger:nth-child(1) {
  transform-origin: top left;
}

.hamburger:nth-child(2) {
  opacity: 1;
}

.hamburger:nth-child(3) {
  transform-origin: bottom left;
}

/* Close animation */
.close:nth-child(1) {
  transform: rotate(45deg) translate(5px, 5px);
}

.close:nth-child(2) {
  opacity: 0;
}

.close:nth-child(3) {
  transform: rotate(-45deg) translate(7px, -7px);
}

/* Menu Items for mobile (hidden by default) */
.menu-items {
  display: none;
  background-color: #f1f5f9;
  position: absolute;
  top: 60px;
  width: 100%;
  left: 0;
  padding: 10px;
  text-align: center;
}

/* Show the menu when the hamburger is clicked */
.menu-open {
  display: block;
}

/* Show the hamburger icon on smaller screens */
@media (min-width: 768px) {
  .hamburger-icon {
    display: none;
  }

  .nav-links {
    display: flex;
    gap: 20px;
  }

  .menu-link {
    font-size: 1rem;
  }
}
</style>
