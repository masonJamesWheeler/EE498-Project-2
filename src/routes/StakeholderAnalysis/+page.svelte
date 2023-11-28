<script lang="ts">
    // Stakeholders data
    const stakeholders = [
      {
        name: "Project Team",
        stakes: "Successful development and deployment of the VR headset.",
        strategy: "Regular meetings, clear communication, and agile methodology.",
        importance: "High",
        directRelationship: "High",
      },
      {
        name: "End Users",
        stakes: "High-quality, reliable, and user-friendly VR headset.",
        strategy: "Gather user feedback, user testing, and continuous improvement.",
        importance : "High",
        directRelationship: "High",
        },
        {
        name: "Investors",
        stakes: "Successful development and deployment of the VR headset.",
        strategy: "Regular meetings, clear communication, and agile methodology.",
        importance: "Medium",
        directRelationship: "High",
        },
        {
        name: "Suppliers",
        stakes: "Successful development and deployment of the VR headset.",
        strategy: "Regular meetings, clear communication, and agile methodology.",
        importance: "Medium",
        directRelationship: "Medium",
        },
        {
        name: "Competitors",
        stakes: "Successful development and deployment of the VR headset.",
        strategy: "Regular meetings, clear communication, and agile methodology.",
        importance: "Medium",
        directRelationship: "Low",
        },
        {
        name: "Government",
        stakes: "Successful development and deployment of the VR headset.",
        strategy: "Regular meetings, clear communication, and agile methodology.",
        importance: "Medium",
        directRelationship: "Low",
        },
        {
        name: "Media",
        stakes: "Successful development and deployment of the VR headset.",
        strategy: "Regular meetings, clear communication, and agile methodology.",
        importance: "Low",
        directRelationship: "Low",
        },
        {
        name: "Public",
        stakes: "Successful development and deployment of the VR headset.",
        strategy: "Regular meetings, clear communication, and agile methodology.",
        importance: "Low",
        directRelationship: "Low",
        },
        {
        name: "Other Stakeholders",
        stakes: "Successful development and deployment of the VR headset.",
        strategy: "Regular meetings, clear communication, and agile methodology.",
        importance: "Low",
        directRelationship: "Low",
        },
    ];

    const nuancedSummary = `
    Our project encompasses a diverse range of stakeholders, each with varying levels of interest and influence. The project team and end users hold the highest importance and direct relationship, necessitating close attention and regular engagement. Investors, while having a high direct relationship, display medium importance, indicating a need for balanced engagement and transparent communication.

    Suppliers and competitors, classified under medium importance, require strategic interaction to ensure supply chain efficiency and competitive edge, respectively. Government and media stakeholders, though ranked lower in direct relationship, are critical for regulatory compliance and public perception, necessitating periodic and strategic engagement.

    The public, other stakeholders, and environmental concerns, though ranked lower in both metrics, cannot be overlooked as they represent the broader impact of our project on society and ethical considerations. Overall, our approach should be dynamic, prioritizing stakeholders according to the project phase and emerging scenarios.
  `;

  </script>
  
  <div class="bg-gray-100 py-8">
    <div class="container mx-auto px-4">
      <h1 class="text-4xl font-bold text-center mb-6">Stakeholder Analysis</h1>
  
      <!-- Stakeholders List -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        {#each stakeholders as stakeholder}
          <div class="bg-white shadow-lg rounded-lg p-4 mb-4">
            <h2 class="font-semibold text-2xl mb-2">{stakeholder.name}</h2>
            <p><strong>Stakes:</strong> {stakeholder.stakes}</p>
            <p><strong>Management Strategy:</strong> {stakeholder.strategy}</p>
          </div>
        {/each}
      </div>
    </div>

    <!-- Stake Holder Matrix -->
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-semibold mb-4">Stakeholder Matrix</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <div class="bg-white shadow-lg rounded-lg p-4 mb-4">
          <h2 class="font-semibold text-2xl mb-2">Importance</h2>
          <p><strong>High:</strong> The stakeholder has a high interest in the project and can significantly impact the project's success.</p>
          <p><strong>Medium:</strong> The stakeholder has a medium interest in the project and can moderately impact the project's success.</p>
          <p><strong>Low:</strong> The stakeholder has a low interest in the project and can minimally impact the project's success.</p>
        </div>
        <div class="bg-white shadow-lg rounded-lg p-4 mb-4">
          <h2 class="font-semibold text-2xl mb-2">Direct Relationship</h2>
          <p><strong>High:</strong> The stakeholder has a direct relationship with the project team and can directly impact the project's success.</p>
          <p><strong>Medium:</strong> The stakeholder has an indirect relationship with the project team and can indirectly impact the project's success.</p>
          <p><strong>Low:</strong> The stakeholder has no relationship with the project team and cannot impact the project's success.</p>
        </div>
      </div>

        <!-- Stake Holder Matrix Table -->
        <div class="bg-white shadow-lg rounded-lg p-4 mb-4 grid-cols-2 grid">
          <h2 class="font-semibold text-2xl mb-2 col-span-1">Stakeholder Matrix Table</h2>
          <table class="table-auto">
            <thead>
              <tr>
                <th class="px-4 py-2">Stakeholder</th>
                <th class="px-4 py-2">Importance</th>
                <th class="px-4 py-2">Direct Relationship</th>
              </tr>
            </thead>
            <tbody>
              {#each stakeholders as stakeholder}
                <tr>
                  <td class="border px-4 py-2">{stakeholder.name}</td>
                  <td class="border px-4 py-2">{stakeholder.importance}</td>
                  <td class="border px-4 py-2">{stakeholder.directRelationship}</td>
                </tr>
              {/each}
            </tbody>
          </table>

            <!-- Nuanced Summary -->
            <div class="bg-white shadow-lg rounded-lg p-4 mb-4 col-span-1">
              <h2 class="font-semibold text-2xl mb-2">Nuanced Summary</h2>
              <p>{nuancedSummary}</p>
              </div>
          </div>
        </div>
    </div>


  
  <style>
    /* Additional styling if needed */
  </style>
  