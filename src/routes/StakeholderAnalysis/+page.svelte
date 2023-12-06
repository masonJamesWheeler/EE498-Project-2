<script lang="ts">
    // Stakeholders data
    const stakeholders = [
      {
        name: "End Users",
        interest: "Accurate and reliable measurements for health monitoring",
        concerns: "User-friendliness, comfort, and non-intrusiveness",
        impact: "Low",
        importance: "Low",
        allegiance: "Medium",
        AIH: "Small checkmark",
        LIH: "Big Checkmark",
        HIH: "No Checkmark",
        MIH: "No Checkmark",
        actions: "(a) (b)"
      },
      {
        name: "VR Headset Manufacturers",
        interest: "Seamless integration with VR hardware",
        concerns: "Compatibility with health technologies, user impacts on VR experience, market differentiation",
        impact: "High",
        importance: "High",
        allegiance: "High",
        AIH: "Small checkmark",
        LIH: "Big Checkmark",
        HIH: "Big Checkmark",
        MIH: "No Checkmark",
        actions: "(c) (d)"
      },
      {
        name: "Healthcare Professionals",
        interest: "Seamless integration with software, necessary data collection",
        concerns: "Accuracy and reliability of health data collected",
        impact: "Medium",
        importance: "High",
        allegiance: "High",
        AIH: "Small checkmark",
        LIH: "Big Checkmark",
        HIH: "Big Checkmark",
        MIH: "No Checkmark",
        actions: "(e) (f)"
      },
      {
        name: "Software Developers",
        interest: "Developing algorithms and applications that utilize health data collected",
        concerns: "Accuracy and reliability of data collected",
        impact: "High",
        importance: "High",
        allegiance: "High",
        AIH: "Small checkmark",
        LIH: "Big Checkmark",
        HIH: "Big Checkmark",
        MIH: "No Checkmark",
        actions: "(g) (h)"
      },
      {
        name: "Investors/Financial Backers",
        interest: "Financial success of the project",
        concerns: "Market demand, revenue streams, return on investment",
        impact: "Medium",
        importance: "Medium",
        allegiance: "High",
        AIH: "Small checkmark",
        LIH: "Big Checkmark",
        HIH: "Big Checkmark",
        MIH: "Big Checkmark",
        actions: "(i) (j)"
      },
      {
        name: "Competitors",
        interest: "Monitoring the development of this specific application and project",
        concerns: "Staying competitive and responding with other innovations",
        impact: "Low",
        importance: "Low",
        allegiance: "Low",
        AIH: "Small checkmark",
        LIH: "No checkmark",
        HIH: "Big Checkmark",
        MIH: "No Checkmark",
        actions: "(k) (l)"
      }
    ];

    const nuancedSummary = `
    Our project is a VR health monitoring application that will be used by end users. The end users are interested in accurate and reliable measurements for health monitoring. They are concerned with the user-friendliness, comfort, and non-intrusiveness of the application. The VR headset manufacturers are interested in seamless integration with the VR hardware. They are concerned with compatibility with health technologies, user impacts on the VR experience, and how to differentiate themselves within the market. Healthcare professionals are interested in the seamless integration with the software as well as the necessary data to be collected. They are concerned with the accuracy and reliability of health data collected. Software developers are interested in developing algorithms and applications that utilize the health data collected. They are concerned with the accuracy and reliability of data collected. 
    `;

  </script>
  
  <div class="bg-gray-100 py-8">
    <div class="container mx-auto px-4">
        <h1 class="text-4xl font-bold text-center mb-6">Stakeholder Analysis</h1>

        <!-- Updated Stakeholders List -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            {#each stakeholders as stakeholder}
                <div class="bg-white shadow-lg rounded-lg p-4 mb-4">
                    <h2 class="font-semibold text-2xl mb-2">{stakeholder.name}</h2>
                    <p><strong>Interest:</strong> {stakeholder.interest}</p>
                    <p><strong>Concerns:</strong> {stakeholder.concerns}</p>
                    <p><strong>Impact:</strong> {stakeholder.impact}</p>
                    <p><strong>Importance:</strong> {stakeholder.importance}</p>
                    <p><strong>Allegiance:</strong> {stakeholder.allegiance}</p>
                    <p><strong>Actions:</strong> {stakeholder.actions}</p>
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
        <div class="bg-white shadow-lg rounded-lg p-4 mb-4 grid-cols-1 grid">
          <h2 class="font-semibold text-2xl mb-2 col-span-1">Stakeholder Matrix Table</h2>
          <table class="table-auto">
            <thead>
              <tr>
                <th class ="px-4 py-2">Stakeholder</th>
                <th class="px-4 py-2">Impact</th>
                <th class="px-4 py-2">Importance</th>
                <th class="px-4 py-2">Allegiance</th>
                <th class="px-4 py-2">AIH</th>
                <th class="px-4 py-2">LIH</th>
                <th class="px-4 py-2">HIH</th>
                <th class="px-4 py-2">MIH</th>
                <th class="px-4 py-2">Concerns</th>
                <th class="px-4 py-2">Actions</th>
              </tr>
            </thead>

            <tbody>
              {#each stakeholders as stakeholder}
                <tr>
                  <td class="border px-4 py-2">{stakeholder.name}</td>
                  <td class="border px-4 py-2">{stakeholder.impact}</td>
                  <td class="border px-4 py-2">{stakeholder.importance}</td>
                  <td class="border px-4 py-2">{stakeholder.allegiance}</td>
                  <!-- Logic to draw checkmark depending on value -->
                  {#if stakeholder.AIH === "Small checkmark"}
                    <td class="border px-4 py-2">✓</td>
                  {:else if stakeholder.AIH === "Big Checkmark"}
                    <td class="border px-4 py-2">✓✓</td>
                  {:else}
                    <td class="border px-4 py-2"></td>
                  {/if}
                  {#if stakeholder.LIH === "Small checkmark"}
                    <td class="border px-4 py-2">✓</td>
                  {:else if stakeholder.LIH === "Big Checkmark"}
                    <td class="border px-4 py-2">✓✓</td>
                  {:else}
                    <td class="border px-4 py-2"></td>
                  {/if}
                  {#if stakeholder.HIH === "Small checkmark"}
                    <td class="border px-4 py-2">✓</td>
                  {:else if stakeholder.HIH === "Big Checkmark"}
                    <td class="border px-4 py-2">✓✓</td>
                  {:else}
                    <td class="border px-4 py-2"></td>
                  {/if}
                  {#if stakeholder.MIH === "Small checkmark"}
                    <td class="border px-4 py-2">✓</td>
                  {:else if stakeholder.MIH === "Big Checkmark"}
                    <td class="border px-4 py-2">✓✓</td>
                  {:else}
                    <td class="border px-4 py-2"></td>
                  {/if}
                  <td class="border px-4 py-2">{stakeholder.concerns}</td>
                  <td class="border px-4 py-2">{stakeholder.actions}</td>
                </tr>
              {/each}
            </tbody>
          </table>

         </div>
         </div>

    </div>

  
  <style>
    /* Additional styling if needed */
  </style>
  