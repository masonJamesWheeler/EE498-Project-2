<script>
  // Any required script can be added here
</script>

<div class="container mx-auto p-4">
  <h1 class="text-4xl font-bold text-center mb-6">Test Plan</h1>
  
  <!-- Function Tests Section -->
  <div class="mb-8">
    <h2 class="text-3xl font-semibold text-center mb-4">Function Tests</h2>

    <!-- Test Sections -->
    <div class="test-section mb-4">
      <h3 class="test-title">Heart-rate Test</h3>
      <p class="test-description">Using a medical-grade oximeter for calibration, the heart-rate will be tested from 50 bpm to 165 bpm in both simulated and real-world conditions.</p>
      <p class="test-criteria"><strong>Success Criteria:</strong> Device matches or is within ±5 bpm of the oximeter; alerts at 120+ or less than 50 bpm.</p>
    </div>
  
      <!-- Breathing-rate Test -->
      <div class="test-section mb-4">
        <h3 class="test-title">Breathing-rate Test</h3>
        <p class="test-description">Conducted with a medical-grade capaciflector at rest, during activity, and intense activity.</p>
        <p class="test-criteria"><strong>Success Criteria:</strong> Device matches or is within ±4 breaths per minute; safety alerts below 10 or above 25 breaths per minute.</p>
      </div>
  
      <!-- Water Resistance Test -->
      <div class="test-section mb-4">
        <h3 class="test-title">Water Resistance Test</h3>
        <p class="test-description">25 mL of water splashed at the device from various angles to test operational stability.</p>
        <p class="test-criteria"><strong>Success Criteria:</strong> Full operational capability during and after the test.</p>
      </div>
  
      <!-- Temperature Under Load Test -->
      <div class="test-section mb-4">
        <h3 class="test-title">Temperature Under Load Test</h3>
        <p class="test-description">Testing with simulated real-world activity at various intervals to monitor temperature.</p>
        <p class="test-criteria"><strong>Success Criteria:</strong> Device temperature stays below 35 degrees C.</p>
      </div>
  
      <!-- Exercise Tests -->
      <div class="test-section mb-4">
        <h3 class="test-title">Exercise Tests</h3>
        <p class="test-description">Five different exercises conducted by individuals of varying abilities to assess comfort and fit.</p>
        <p class="test-criteria"><strong>Success Criteria:</strong> At least 80% positive responses regarding comfort and fit.</p>
      </div>
  
      <!-- EMC Tests -->
      <div class="test-section mb-4">
        <h3 class="test-title">EMC Tests</h3>
        <p class="test-description">EMC testing and certification by UL Solutions.</p>
        <p class="test-criteria"><strong>Success Criteria:</strong> Obtaining EMC certification.</p>
      </div>
    </div>
  </div>
  
  <style>
    .test-section {
      background-color: #f9f9f9; /* Light gray background */
      border-radius: 12px; /* Rounded corners */
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Subtle shadow */
      padding: 20px; /* Spacing inside each section */
      margin-bottom: 20px; /* Spacing between sections */
    }
  
    .test-title {
      font-size: 1.5rem; /* Larger font size for titles */
      color: #333; /* Darker text for emphasis */
      margin-bottom: 10px; /* Spacing after titles */
    }
  
    .test-description {
      font-size: 1.1rem; /* Slightly larger font size for readability */
      margin-bottom: 15px; /* Spacing after description paragraph */
    }
  
    .test-criteria {
      font-size: 1.1rem; /* Slightly larger font size for criteria */
      font-weight: 600; /* Semi-bold font weight for criteria */
      color: #555; /* Dark gray for criteria text */
    }
  </style>