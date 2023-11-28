<script lang="ts">
    // Level 0 (L0) Requirements
    const L0Requirements = [
      "The system shall accurately measure the user's heart rate.",
      "The system shall accurately measure the user's breathing rate.",
      "The system shall integrate these measurements with a VR headset interface.",
      "The system shall ensure user safety during use.",
      "The system shall provide real-time feedback based on the measured data.",
      "The VR headset shall be comfortable to wear for extended periods.",
      "The system shall process data securely to protect user privacy.",
      "The system shall operate continuously for a minimum of 4 hours on a single charge.",
      "The system shall provide an intuitive user interface.",
      "The system shall be compatible with standard VR software."
    ];
  
    // Level 1 (L1) Requirements
    const L1Requirements = {
      hardware: [
        "The hardware shall include a reliable heart rate sensor.",
        "The hardware shall include a breathing rate sensor capable of detecting subtle changes.",
        "The headset shall incorporate a wireless module for data transmission.",
        "The headset shall be designed with materials that are non-irritating to the skin.",
        "The hardware shall include a haptic feedback system for real-time user alerts."
      ],
      software: [
        "The software shall process heart and breathing data in real-time.",
        "The software shall encrypt sensitive data during transmission and storage.",
        "The software shall display battery life and notify users when charging is needed.",
        "The user interface shall be navigable with VR headset controls.",
        "The software shall be compatible with major VR gaming and training platforms."
      ]
    };
  </script>
  
  <div class="bg-gray-100 py-8">
    <div class="container mx-auto px-4">
      <h1 class="text-4xl font-bold text-center mb-6">System Requirements</h1>
  
      <!-- Level 0 Requirements -->
      <div class="mb-8">
        <h2 class="text-3xl font-semibold mb-4">Level 0 (L0) Requirements</h2>
        <ol class="list-decimal ml-4">
          {#each L0Requirements as req}
            <li>{req}</li>
          {/each}
        </ol>
      </div>
  
      <!-- Level 1 Requirements -->
      <div class="mb-8">
        <h2 class="text-3xl font-semibold mb-4">Level 1 (L1) Requirements</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          <!-- Hardware Requirements -->
          <div>
            <h3 class="text-2xl font-semibold">Hardware</h3>
            <ol class="list-decimal ml-4">
              {#each L1Requirements.hardware as req}
                <li>{req}</li>
              {/each}
            </ol>
          </div>
          <!-- Software Requirements -->
          <div>
            <h3 class="text-2xl font-semibold">Software</h3>
            <ol class="list-decimal ml-4">
              {#each L1Requirements.software as req}
                <li>{req}</li>
              {/each}
            </ol>
          </div>
        </div>
      </div>
    </div>
  </div>
  
  <style>
    /* Additional styling if needed */
  </style>
  