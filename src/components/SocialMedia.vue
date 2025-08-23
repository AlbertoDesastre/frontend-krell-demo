<template>
  <section class="social-media-section">
    <ul class="social-list">
      <!-- Github -->
      <li class="social-icon">
        <a href="https://github.com/AlbertoDesastre" target="_blank">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          >
            <path
              d="M15 22v-4a4.8 4.8 0 0 0-1-3.5c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65-.17.6-.22 1.23-.15 1.85v4"
            ></path>
            <path d="M9 18c-4.51 2-5-2-7-2"></path>
          </svg>
        </a>
      </li>

      <!-- Linkedin -->
      <li class="social-icon">
        <a href="https://www.linkedin.com/in/alberto-armas-santana/" target="_blank">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="lucide lucide-linkedin"
          >
            <path
              d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"
            ></path>
            <rect width="4" height="12" x="2" y="9"></rect>
            <circle cx="4" cy="4" r="2"></circle>
          </svg>
        </a>
      </li>

      <!-- CV -->
      <li class="social-icon">
        <a href="/CV_Fullstack_Castellano.pdf" target="_blank">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="lucide lucide-file-down"
          >
            <path d="M15 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V7Z"></path>
            <path d="M14 2v4a2 2 0 0 0 2 2h4"></path>
            <path d="M12 18v-6"></path>
            <path d="m9 15 3 3 3-3"></path>
          </svg>
        </a>
      </li>
    </ul>
  </section>
</template>

<style scoped>
.social-list {
  display: flex;
  gap: 10px;
}

.social-icon {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  padding: 5px;
}

.social-icon svg {
  width: 38px;
  height: 38px;
  stroke: whitesmoke;
  transition: all 0.2s ease;
}

.social-icon:hover svg {
  width: 45px;
  height: 45px;
  stroke: var(--green-lime);
}
</style>
