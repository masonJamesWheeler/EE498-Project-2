<!-- Software Requirements:
User Interface Subsystem Requirements:
L0.1) Device shall turn off
1. Device shall have a power button on the interface.
2. Device shall turn off after 10 minutes of non-use.
	L0.2) Should have good weight distribution on neck or head.
1. Device shall not concentrate it’s weight asymmetrically on the neck or head
2. The majority of the weight shall not be on the neck (>50%)
	L0.3) Device shall give alerts for out-of-normal biometrics
1. Device shall give alerts on display if heartbeat is above 140 bpm for longer than 10 seconds.
2. Device shall give alerts on display if heartbeat is less than 55 bpm
		3. User shall be able to adjust which out-of-normal biometrics give alerts
		4. User shall be able to turn off out-of-normal biometric alerts
5. Device shall give alerts if the breathing rate exceeds 20 breaths/min or goes below 10 breaths per minute.
	L0.4) Device shall be able to give option to store data
1. Device shall communicate with the user if biometric data is to be stored.
2. Device shall add software to organize heartbeat and  breathing rate into charts via date for user
	L0.5) (O) Device shall display biometrics to user
1. Device shall display biometric data on the VR headset or app.
L0.6) User shall be notified about devices condition 
	1) Device shall notify when device battery is less than 20%

Hardware Requirements:
Sensor Subsystem Requirements:
L0.1) Device shall measure heart-rate
		L1.0 Device shall be accurate to a +-5 beats per minute
	L0.2) Device shall measure breathing-rate
		L1.1 Device shall be have an uncertainty of (+-4) a minute
Data Transmission Subsystem Requirements:
	L0.3) Device shall prepare raw data for transmission
L0.4) Device shall transmit heart-rate data to the VR display
		1.Device shall use a wireless module for breathing-rate  data transmission
		2. The device shall include a haptic feedback system for real-time user alerts.
	L0.5) Device shall transmit breathing-rate data to the VR display
1. The device shall include a haptic feedback system for real-time user alerts.
2. Device shall use a wireless module for breathing-rate data transmission	

Power Subsystem Requirements:
	L0.6) Device shall operate 4 hours continuously on a single charge 
	L0.7) Device shall minimize power consumption when turned on but not in use
	L0.8) Device shall be capable of recharging 
1. Device shall use usb-C for recharging the battery
	L0.9) Device shall implement smart charging protection
2. Device shall prevent overcharge 

General Hardware Requirements:
	L0.10) Shall be cheap enough to manufacture to still profit on device.
1. Device shall not cost more than 10$ to manufacture.
L0.11) Should be environmentally friendly when scrapped.
1. Device should have at least 10% recyclable parts
	L0.12) Device shall be water resistant
1. Device shall not use sticky solutions (tape, glue) to attach to user.
2. Device shall not short circuit when splashed with water (simulate sweating)
L0.13) Should be safe for use for humans for long periods of time.
1. Device should not get hotter than 35 degrees C.
2. Device shall turn off when above 35 degrees C.
3. Device shall not have any dangerous chemicals or metals to humans according to the FDA.
4. Device shall not emit dangerous electromagnetic wavelengths or frequencies
L0.14) Device Shall physically stay on user
1. Device Shall not fall off user during intense usage (sprints, rapid hand motions,
tested via demonstrations)
2. Device shall Implement adjustable straps for a secure fit on different body sizes.
3. Device Shall have easy and quick attachment and removal for user convenience.
4. Device should be in the form of a bracelet
L0.15) Device shall be designed with materials that are non-irritating to the skin
	1. Device shall not use allergenic materials 
 -->
 <script lang="ts">
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
    { L0: "Device shall measure heart-rate", L1: ["Device shall be accurate to a +-5 beats per minute."] },
    { L0: "Device shall measure breathing-rate", L1: ["Device shall be have an uncertainty of (+-4) a minute."] },
    { L0: "Device shall prepare raw data for transmission", L1: [] },
    { L0: "Device shall transmit heart-rate data to the VR display", L1: ["Device shall use a wireless module for breathing-rate data transmission.", "The device shall include a haptic feedback system for real-time user alerts."] },
    { L0: "Device shall transmit breathing-rate data to the VR display", L1: ["The device shall include a haptic feedback system for real-time user alerts.", "Device shall use a wireless module for breathing-rate data transmission."] },
    { L0: "Device shall operate 4 hours continuously on a single charge", L1:[] },
    { L0: "Device shall minimize power consumption when turned on but not in use", L1: [] },
    { L0: "Device shall be capable of recharging", L1: ["Device shall use usb-C for recharging the battery."] },
    { L0: "Device shall implement smart charging protection", L1: ["Device shall prevent overcharge."] },
    { L0: "Shall be cheap enough to manufacture to still profit on device", L1: ["Device shall not cost more than 10$ to manufacture."] },
    { L0: "Should be environmentally friendly when scrapped", L1: ["Device should have at least 10% recyclable parts."] },
    { L0: "Device shall be water resistant", L1: ["Device shall not use sticky solutions (tape, glue) to attach to user.", "Device shall not short circuit when splashed with water (simulate sweating)."] },
    { L0: "Should be safe for use for humans for long periods of time", L1: ["Device should not get hotter than 35 degrees C.", "Device shall turn off when above 35 degrees C.", "Device shall not have any dangerous chemicals or metals to humans according to the FDA.", "Device shall not emit dangerous electromagnetic wavelengths or frequencies."] },
    { L0: "Device Shall physically stay on user", L1: ["Device Shall not fall off user during intense usage (sprints, rapid hand motions, tested via demonstrations).", "Device shall Implement adjustable straps for a secure fit on different body sizes.", "Device Shall have easy and quick attachment and removal for user convenience.", "Device should be in the form of a bracelet."] },
    { L0: "Device shall be designed with materials that are non-irritating to the skin", L1: ["Device shall not use allergenic materials."] }
  ];
</script>

<div class="bg-gray-100 py-8">
  <div class="container mx-auto px-4">
    <h1 class="text-4xl font-bold text-center mb-6">System Requirements</h1>

    <!-- Software Requirements -->
    <div class="mb-8">
      <h2 class="text-3xl font-semibold mb-4">Software Requirements</h2>
      {#each softwareRequirements as req}
        <div class="mb-4">
          <h3 class="text-2xl font-semibold">{req.L0}</h3>
          <ol class="list-decimal ml-4">
            {#each req.L1 as item}
              <li>{item}</li>
            {/each}
          </ol>
        </div>
      {/each}
    </div>

    <!-- Hardware Requirements -->
    <div class="mb-8">
      <h2 class="text-3xl font-semibold mb-4">Hardware Requirements</h2>
      {#each hardwareRequirements as req}
        <div class="mb-4">
          <h3 class="text-2xl font-semibold">{req.L0}</h3>
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

<style>
  /* Additional styling as needed */
</style>
