<script setup lang="ts">
import { storeToRefs } from 'pinia'
import { useAuth } from '@/composables/useAuth'
import { useFilmCreateModal } from '@/features/filmkritiken/composables/useFilmCreateModal'

// storeToRefs, weil ein direktes Destructuring den Computed-Wert einmalig
// auspackt: canAddFilm wäre für immer false, da die Session erst nach dem
// Mounten geladen wird.
const { canAddFilm } = storeToRefs(useAuth())
const { openModal } = useFilmCreateModal()
</script>

<template>
  <!-- Admin FAB: only visible when user can add films -->
  <button
    v-if="canAddFilm"
    id="admin-fab"
    class="fixed bottom-6 right-6 z-50 w-14 h-14 rounded-full bg-cinema-red hover:opacity-90 text-white text-2xl font-bold shadow-2xl border border-white/10 backdrop-blur-md transition-all duration-200 hover:scale-110 active:scale-95 flex items-center justify-center"
    aria-label="Film hinzufügen"
    title="Film hinzufügen"
    @click="openModal"
  >
    +
  </button>
</template>
