<script lang="ts">
    const weeks = 12;
    const categories = [
      { key: "planning", label: "Planning", color: "bg-blue-500" },
      { key: "design", label: "Hardware & Software Design", color: "bg-green-500" },
      { key: "implementation", label: "Implementation", color: "bg-yellow-500" },
      { key: "testing", label: "Testing & Validation", color: "bg-red-500" },
      { key: "documentation", label: "Documentation", color: "bg-purple-500" },
    ];
  
    const getCategoryColor = (categoryKey: string) => {
      const category = categories.find((c) => c.key === categoryKey);
      return category ? category.color : "bg-gray-500";
    };
      
    // Specific Tasks for VR Headset Project
    const tasks = [
      { id: 1, text: "Market Analysis and Feasibility Study", start_week: 1, duration: 1, category: "planning" },
      { id: 2, text: "Project Planning and Roadmap Development", start_week: 1, duration: 1, category: "planning" },
      { id: 3, text: "Hardware Design and Prototyping", start_week: 2, duration: 2, category: "design" },
      { id: 4, text: "Software Architecture and Interface Design", start_week: 4, duration: 2, category: "design" },
      { id: 5, text: "Integration of Hardware and Software", start_week: 6, duration: 2, category: "implementation" },
      { id: 6, text: "VR Environment Development", start_week: 8, duration: 2, category: "implementation" },
      { id: 7, text: "Alpha Testing and Feedback Collection", start_week: 10, duration: 1, category: "testing" },
      { id: 8, text: "Beta Testing with Early Adopters", start_week: 11, duration: 1, category: "testing" },
      { id: 9, text: "Final Documentation and Reporting", start_week: 11, duration: 1, category: "documentation" },
      { id: 10, text: "Project Presentation and Demo", start_week: 12, duration: 1, category: "documentation" },
    ];
  </script>
  
  <div class="bg-gray-100 py-8">
    <div class="container mx-auto px-4">
      <h1 class="text-4xl font-bold text-center mb-6">Project Plan</h1>
  
      <!-- Chart -->
      <div class="flex flex-col md:flex-row">
        <div class="w-full">
          {#each tasks as task}
            <div class="flex items-center mb-4">
              <div class="flex-1 flex items-center">
                <div class={`w-4 h-6 mr-2 rounded-full ${getCategoryColor(task.category)}`}></div>
                <div>{task.text}</div>
              </div>
              <div class="w-3/4 flex relative">
                <div class={`absolute h-4 ${getCategoryColor(task.category)} rounded`}
                     style={`left: ${(task.start_week - 1) * (100 / weeks)}%; width: ${task.duration * (100 / weeks)}%`}></div>
              </div>
            </div>
          {/each}
        </div>
      </div>
    </div>

    <!-- Informational about our process -->
    <div class="container mx-auto px-4 py-8">
      <h2 class="text-3xl font-semibold mb-4">Process</h2>
      <p class="text-lg mb-4">
        Our team's plan is designed to be agressive, but also realistic. We have a total of 12 weeks to complete our project, and we have broken down our tasks into 5 categories: Planning, Design, Implementation, Testing, and Documentation. We have also included a Gantt chart to visualize our project plan.
        </p>
        <p class="text-lg mb-4">
        We have a total of 10 tasks, and each task has a start week and a duration. The start week is the week that the task will begin, and the duration is the number of weeks that the task will take to complete. The Gantt chart is divided into 12 weeks, and each task is represented by a colored bar. The color of the bar corresponds to the category of the task. The length of the bar corresponds to the duration of the task, and the position of the bar corresponds to the start week of the task.
        </p>
        <p class="text-lg mb-4">

        Our project plan is designed to be flexible, and we will adjust our plan as needed. We will also be using an agile development process, which will allow us to adapt to changes and deliver a high-quality product.
        </p>
        </div>
  </div>

