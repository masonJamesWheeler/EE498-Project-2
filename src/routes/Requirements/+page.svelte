 <script lang="ts">

  import BlockDiagram from "$lib/BlockDiagram.png";
  // Software Requirements (L0 and L1)
  const softwareRequirements = [
    { L0: "Device shall turn off", L1: ["Device shall have a power button on the interface.", "Device shall turn off after 10 minutes of non-use."] },
    { L0: "Should have good weight distribution on neck or head.", L1: ["Device shall not concentrate its weight asymmetrically on the neck or head.", "The majority of the weight shall not be on the neck (>50%)."] },
    { L0: "Device shall give alerts for out-of-normal biometrics", L1: ["Device shall give alerts on display if heartbeat is above 140 bpm for longer than 10 seconds.", "Device shall give alerts on display if heartbeat is less than 55 bpm.", "User shall be able to adjust which out-of-normal biometrics give alerts.", "User shall be able to turn off out-of-normal biometric alerts.", "Device shall give alerts if the breathing rate exceeds 20 breaths/min or goes below 10 breaths per minute."] },
    { L0: "Device shall be able to give option to store data", L1: ["Device shall communicate with the user if biometric data is to be stored.", "Device shall add software to organize heartbeat and breathing rate into charts via date for user."] },
    { L0: "Device shall display biometrics to user", L1: ["Device shall display biometric data on the VR headset or app."] },
    { L0: "User shall be notified about devices condition", L1: ["Device shall notify when device battery is less than 20%."] }
  ];

  // Hardware Requirements (L0 and L1)
  const hardwareRequirements = [
    { L0: "Device shall measure heart-rate", L1: ["Device shall be accurate to a +-5 beats per minute."], heading: "Sensor System Requirements" },
    { L0: "Device shall measure breathing-rate", L1: ["Device shall be have an uncertainty of (+-5) a minute."], heading: "Sensor System Requirements" },
    { L0: "Device shall prepare raw data for transmission", L1: [], heading:"Data Transmission Subsystem Requirements"},
    { L0: "Device shall transmit heart-rate data to the VR display", L1: ["Device shall use a wireless module for breathing-rate data transmission.", "The device shall include a haptic feedback system for real-time user alerts."], heading:"Data Transmission Subsystem Requirements"},
    { L0: "Device shall transmit breathing-rate data to the VR display", L1: ["The device shall include a haptic feedback system for real-time user alerts.", "Device shall use a wireless module for breathing-rate data transmission."] , heading:"Data Transmission Subsystem Requirements"},
    { L0: "Device shall operate 4 hours continuously on a single charge", L1:[], heading: "Power Subsystem Requirements"},
    { L0: "Device shall minimize power consumption when turned on but not in use", L1: [] , heading: "Power Subsystem Requirements"},
    { L0: "Device shall be capable of recharging", L1: ["Device shall use usb-C for recharging the battery."], heading: "Power Subsystem Requirements"},
    { L0: "Device shall implement smart charging protection", L1: ["Device shall prevent overcharge."] , heading: "Power Subsystem Requirements"},
    { L0: "Shall be cheap enough to manufacture to still profit on device", L1: ["Device shall not cost more than 10$ to manufacture."], heading: "General Hardware Requirements"},
    { L0: "Should be environmentally friendly when scrapped", L1: ["Device should have at least 10% recyclable parts."] , heading: "General Hardware Requirements"},
    { L0: "Device shall be water resistant", L1: ["Device shall not use sticky solutions (tape, glue) to attach to user.", "Device shall not short circuit when splashed with water (simulate sweating)."] , heading: "General Hardware Requirements"},
    { L0: "Should be safe for use for humans for long periods of time", L1: ["Device should not get hotter than 35 degrees C.", "Device shall turn off when above 35 degrees C.", "Device shall not have any dangerous chemicals or metals to humans according to the FDA.", "Device shall not emit dangerous electromagnetic wavelengths or frequencies."], heading: "General Hardware Requirements"},
    { L0: "Device Shall physically stay on user", L1: ["Device Shall not fall off user during intense usage (sprints, rapid hand motions, tested via demonstrations).", "Device shall Implement adjustable straps for a secure fit on different body sizes.", "Device Shall have easy and quick attachment and removal for user convenience.", "Device should be in the form of a bracelet."] , heading: "General Hardware Requirements"},
    { L0: "Device shall be designed with materials that are non-irritating to the skin", L1: ["Device shall not use allergenic materials."] }
  ];

  const SensorSubSystemRequirements = hardwareRequirements.filter(req => req.heading === "Sensor System Requirements");
  const DataTransmissionSubSystemRequirements = hardwareRequirements.filter(req => req.heading === "Data Transmission Subsystem Requirements");
  const PowerSubSystemRequirements = hardwareRequirements.filter(req => req.heading === "Power Subsystem Requirements");
  const GeneralHardwareRequirements = hardwareRequirements.filter(req => req.heading === "General Hardware Requirements");

</script>

<div class="bg-white py-8 text-slate-800">
  <div class="container mx-auto px-4 bg-gray-100 p-8 rounded-3xl">
    <h1 class="text-4xl font-bold text-center mb-6">System Requirements</h1>

    <!-- Software Requirements -->
    <div class="mb-8">
      <h2 class="text-3xl font-semibold mb-4">Software Requirements</h2>
      <h2 class = "text-2xl font-semibold mb-4 ml-4">User Interface Subsystem Requirements</h2>
      {#each softwareRequirements as req}
        <div class="mb-4 ml-12">
          <h3 class="text-2xl">{req.L0}</h3>
          <ol class="list-decimal ml-4">
            {#each req.L1 as item}
              <li>{item}</li>
            {/each}
          </ol>
        </div>
      {/each}
    </div>

    <!-- Image of Block Diagram -->
    <div class="mb-8 mx-auto bg-white rounded-3xl">
      <img class = "p-8 my-6" src={BlockDiagram} alt="Block Diagram" />
    </div>

    <!-- Hardware Requirements -->
    <div class="mb-8">
      <h2 class="text-3xl font-semibold mb-4">Hardware Requirements</h2>
      <h2 class = "text-2xl font-semibold mb-4 ml-4">Sensor Subsystem Requirements</h2>
      {#each SensorSubSystemRequirements as req}
        <div class="mb-4 ml-12">
          <h3 class="text-2xl ">{req.L0}</h3>
          <ol class="list-decimal ml-4">
            {#each req.L1 as item}
              <li>{item}</li>
            {/each}
          </ol>
        </div>
      {/each}

      <h2 class = "text-2xl font-semibold mb-4 ml-4">Data Transmission Subsystem Requirements</h2>
      {#each DataTransmissionSubSystemRequirements as req}
        <div class="mb-4 ml-12">
          <h3 class="text-2xl">{req.L0}</h3>
          <ol class="list-decimal ml-4">
            {#each req.L1 as item}
              <li>{item}</li>
            {/each}
          </ol>
        </div>
      {/each}

      <h2 class = "text-2xl font-semibold mb-4 ml-4">Power Subsystem Requirements</h2>
      {#each PowerSubSystemRequirements as req}
        <div class="mb-4 ml-12">
          <h3 class="text-2xl ">{req.L0}</h3>
          <ol class="list-decimal ml-4">
            {#each req.L1 as item}
              <li>{item}</li>
            {/each}
          </ol>
        </div>
      {/each}

      <h2 class = "text-2xl font-semibold mb-4 ml-4">General Hardware Requirements</h2>
      {#each GeneralHardwareRequirements as req}
        <div class="mb-4 ml-12">
          <h3 class="text-2xl">{req.L0}</h3>
          <ol class="list-decimal ml-4">
            {#each req.L1 as item}
              <li>{item}</li>
            {/each}
          </ol>
        </div>
      {/each}
    </div>
  </div>
</div>

      



 <div class = "inputs">
  <h1>Device Inputs:</h1>
  <ul>
    <li>Heart-rate sensor</li>
    <li>Breathing-rate sensor</li>
    <li>Power source</li>
  </ul>
 </div>

  <div class = "outputs">
    <h1>Device Outputs:</h1>
    <ul>
      <li>Wireless data transmission module</li>
    </ul>
  </div>

  <div class = "behavior">
    <h1>Subsystem Behavior:</h1>
    <ul>
      <li>Data will be gathered using the breathing and heart rate sensors which are powered by the power subsystem. The data will be processed and transmitted to the VR headset which will display the data and communicate with the user.</li>
    </ul>
  </div>

<style>
  .inputs {
    background-color: #f2f2f2;
    padding: 20px;
    margin: 20px;
  }

  .outputs {
    background-color: #f2f2f2;
    padding: 20px;
    margin: 20px;
  }

  .behavior {
    background-color: #f2f2f2;
    padding: 20px;
    margin: 20px;
  }
</style>
