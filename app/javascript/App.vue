<template>
  <div class="min-h-screen bg-gray-100">
    <h1 class="text-4xl font-bold text-center py-8">Promptly</h1>
    <p class="text-center text-gray-600">Your AI-powered word puzzle game</p>

    <div class="max-w-4xl mx-auto mt-8 py-5 bg-amber-50 rounded-2xl">
      <h2 class="flex justify-center items-center mb-4 text-2xl">Today's Puzzle</h2>

      <!-- Game board -->
      <div class="mx-5">
        <div
          v-for="(clue, index) in puzzle.clues"
          :key="index"
          class="grid grid-cols-2 py-3 gap-6 hover:bg-amber-200"
          :class="{
            'bg-amber-200': selectedSlot && selectedSlot.rowIndex === index
          }"
          @click="selectAvailableSlot(index)"
        >
          <div class="font-medium flex justify-end items-center p-3 text-right">
            {{ clue }}
          </div>
          <div class="flex flex-row items-center gap-x-3 h-full">
            <div
            v-for="placeholderIndex in puzzle.placeholderSlots[index]"
            :key="placeholderIndex"
            class="flex items-center justify-center py-1 px-3 min-w-10 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"
            :class="{
              'bg-white drop-shadow-lg/50': selectedSlot && selectedSlot.rowIndex === index && selectedSlot.slotIndex === placeholderIndex - 1,
              'bg-amber-100 hover:bg-white hover:drop-shadow-lg/50': !(selectedSlot && selectedSlot.rowIndex === index && selectedSlot.slotIndex === placeholderIndex - 1)
            }"
            @click.stop="selectSlot(index, placeholderIndex - 1)"
            >
            <p v-if="userAnswers[index][placeholderIndex - 1]">{{ userAnswers[index][placeholderIndex - 1] }}</p>
            <p v-else>&nbsp;</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Scrambled pieces pool -->
    <div>
      <div class="max-w-4xl justicy-center mx-auto mt-8 p-5 bg-amber-50 rounded-2xl">
        <div class="max-w-xl mx-auto flex flex-row flex-wrap gap-3 justify-center">
          <div
          v-for="(piece, index) in availablePieces"
          :key="index"
          class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"
          >
          {{ piece }}
          </div>
        </div>

        <div class="max-w-xl flex justify-around mx-auto text-amber-600 text-2xl mt-8 gap-y-3">
          <button>Hint</button>
          <button>Shuffle</button>
          <button>Sort</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const puzzle = ref({
  clues: [
    'Encourage growth or development',
    'Normal; standard',
    'Medieval precursor or development',
    'Smart and quick-witted',
    'Plainness or clarity'
  ],
  pieces: ['cul', 'tiv', 'ate', 'reg', 'u', 'lar', 'al', 'chem', 'my', 'in', 'tel', 'li', 'gent', 'sim', 'plic', 'i', 'ty'],
  answers: ['cultivate', 'regular', 'alchemy', 'intelligent', 'simplicity'],
  placeholderSlots: [3, 3, 3, 4, 4] // Number of pieces needed for each word
})

// to track which pieces are placed in each row
const userAnswers = ref(
  puzzle.value.placeholderSlots.map(count => Array(count).fill(null))
)

const availablePieces = ref([...puzzle.value.pieces])

const selectedSlot = ref(null)

const selectSlot = (rowIndex, slotIndex) => {
  selectedSlot.value = { rowIndex, slotIndex }
}

const selectAvailableSlot = (rowIndex) => {
  const isNull = (element) => element === null
  let updatedSlotIndex = userAnswers.value[rowIndex].findIndex(isNull)

  selectedSlot.value = { rowIndex, slotIndex: updatedSlotIndex }
}
</script>
