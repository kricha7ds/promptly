<template>
  <div class="min-h-screen bg-gray-100">
    <h1 class="text-4xl font-bold text-center py-8">Promptly</h1>
    <p class="text-center text-gray-600">Your AI-powered word puzzle game</p>

    <div class="max-w-4xl mx-auto mt-8 py-5 bg-amber-50 rounded-2xl">
      <h2 class="flex justify-center items-center mb-4 text-2xl">Today's Puzzle</h2>

      <!-- Game board -->
      <div class="mx-5">
        <div class="grid grid-cols-2 py-3 gap-6 hover:bg-amber-200">
          <div class="font-medium flex justify-end items-center p-3 text-right">Encourage growth or development</div>
          <div class="flex flex-row items-center gap-x-3 h-full">
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>cul</p></div>
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>tiv</p></div>
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>ate</p></div>
          </div>
        </div>

        <div class="grid grid-cols-2 py-3 gap-6 hover:bg-amber-200">
          <div class="font-medium flex justify-end items-center p-3 text-right">Normal; standard</div>
          <div class="flex flex-row items-center gap-x-3 h-full">
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>reg</p></div>
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>u</p></div>
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>lar</p></div>
          </div>
        </div>

        <div class="grid grid-cols-2 py-3 gap-6 hover:bg-amber-200">
          <div class="font-medium flex justify-end items-center p-3 text-right">Medieval precursor to chemsitry</div>
          <div class="flex flex-row items-center gap-x-3 h-full">
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>al</p></div>
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>che</p></div>
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>my</p></div>
          </div>
        </div>

        <div class="grid grid-cols-2 py-3 gap-6 hover:bg-amber-200">
          <div class="font-medium flex justify-end items-center p-3 text-right">Smart and quick-witted</div>
          <div class="flex flex-row items-center gap-x-3 h-full">
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>in</p></div>
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>tel</p></div>
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>li</p></div>
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>gent</p></div>
          </div>
        </div>

        <div class="grid grid-cols-2 py-3 gap-6 hover:bg-amber-200">
          <div class="font-medium flex justify-end items-center p-3 text-right">Plainness or clarity</div>
          <div class="flex flex-row items-center gap-x-3 h-full">
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>sim</p></div>
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>plic</p></div>
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>i</p></div>
            <div class="flex items-center justify-center py-1 px-3 min-w-10 bg-white rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150"><p>ty</p></div>
          </div>
        </div>
      </div>
    </div>

    <!-- Scrambled pieces pool -->
    <div>
      <div class="max-w-4xl justicy-center mx-auto mt-8 p-5 bg-amber-50 rounded-2xl">
        <div class="max-w-xl mx-auto flex flex-row flex-wrap gap-3 justify-center">
          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">cul</div>
          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">tiv</div>
          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">ate</div>

          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">reg</div>
          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">u</div>
          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">lar</div>

          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">al</div>
          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">che</div>
          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">my</div>

          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">in</div>
          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">tel</div>
          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">li</div>
          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">gent</div>

          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">sim</div>
          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">plic</div>
          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">i</div>
          <div class="font-medium text-2xl py-1 px-3 bg-amber-200 rounded hover:cursor-pointer hover:drop-shadow-lg/50 transition duration-150">ty</div>
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

<script>
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
  answers: ['cultivate', 'regular', 'alchemy', 'intelligent', 'simplicity']
})

// to track which pieces are placed in each row
const userAnswers = ref([
  [], // Row 1
  [], // Row 2
  [], // Row 3
  [], // Row 4
  [], // Row 5
])

const availablePieces = ref([...puzzle.value.pieces])
export default {
  name: 'App'
}
</script>
