<script>
    // Any required script can be added here
  </script>
  
  <div class="container mx-auto p-4">
    <h1 class="text-4xl font-bold text-center mb-6">System Design</h1>
    
    <div class="mb-8 p-4 bg-green-100 rounded-lg shadow-md">
        <h2 class="text-3xl font-semibold mb-4">Smartphone Application</h2>
        
        <h3 class="text-2xl font-semibold">Security Handling</h3>
        <p>The smartphone application will employ state-of-the-art encryption protocols for both data transmission and storage. To ensure the highest level of security, the app will use AES-256 encryption, which is the gold standard for data protection. Furthermore, all communication between the VR headset and the smartphone app will be secured via SSL/TLS, safeguarding against any data breaches or eavesdropping.</p>
      
        <h3 class="text-2xl font-semibold">Data Storing</h3>
        <p>Data will be securely stored in the cloud, accessible only to authorized users. The app will employ OAuth 2.0 for user authentication, ensuring that only the legitimate user has access to their data. Furthermore, the application will support two-factor authentication for added security. All stored data will be anonymized and encrypted, providing both security and privacy to the user. The app will also feature customizable privacy settings, allowing users to control the sharing of their health data.</p>
      
        <h3 class="text-2xl font-semibold">User Interface & Experience</h3>
        <p>The application will feature an intuitive and user-friendly interface, designed to provide a seamless experience from onboarding to daily usage. Real-time syncing with the VR headset ensures that users have immediate access to their health metrics. The app will also include visualizations of health trends, personalized insights, and recommendations based on the user's biometric data.</p>
      </div>
      
  
    <!-- VR Headset Section -->
    <div class="mb-8 p-4 bg-orange-100 rounded-lg shadow-md">
        <h2 class="text-3xl font-semibold mb-4">VR Headset</h2>
        
        <h3 class="text-2xl font-semibold">Security Handling</h3>
        <p>The VR headset is designed with security as a priority. It features secure Bluetooth LE (Low Energy) connections to ensure efficient and secure communication with the smartphone application. Data channels between the headset and other devices are encrypted, preventing unauthorized access. The headset firmware will be regularly updated to address any potential security vulnerabilities and maintain compliance with the latest security standards.</p>
      
        <h3 class="text-2xl font-semibold">Design and Comfort</h3>
        <p>The VR headset is ergonomically designed for comfort during prolonged use. It includes adjustable straps for a custom fit and is made with lightweight materials to reduce strain on the head and neck. The headset's interior is lined with a soft, breathable fabric for additional comfort. It is also designed to accommodate different face shapes and sizes, ensuring a snug and comfortable fit for a wide range of users.</p>
      
        <h3 class="text-2xl font-semibold">Advanced Features</h3>
        <p>Along with standard VR capabilities, the headset incorporates advanced features such as adaptive focus for users with varying visual acuities and an ambient light sensor to adjust display brightness. It also includes built-in speakers and a microphone for a fully immersive experience. The headset is compatible with a range of VR content, making it suitable for both health monitoring and entertainment purposes.</p>
      </div>
      
  
    <!-- Bracelet Health Data Measurement Section -->
    <div class="mb-8 p-4 bg-violet-100 rounded-lg shadow-md">
      <h2 class="text-3xl font-semibold mb-4">Bracelet Health Data Measurement</h2>
      <p>The device will be in the form of a bracelet that uses sensors to collect biometric data, then prepares and transmits it to the VR headset for display.</p>
      <h3 class="text-2xl font-semibold">Bracelet Material</h3>
      <p>Available in Nylon, Silicone, and vegan leather, each offering different price points and user experiences.</p>
      <h3 class="text-2xl font-semibold">Heart-rate Sensor</h3>
      <p>Utilizes a pulse photoplethysmography sensor integrated into the bracelet material to track heart rate accurately.</p>
      <h3 class="text-2xl font-semibold">Breathing-rate Sensor</h3>
      <p>An accelerometer woven into the bracelet material to monitor breathing rate effectively.</p>
      <h3 class="text-2xl font-semibold">Transmitting Data</h3>
      <p>Data will be transmitted using a Bluetooth module, ensuring real-time updates to the VR headset.</p>
      <h3 class="text-2xl font-semibold">Battery</h3>
      <p>A lithium-ion rechargeable battery will be used, chargeable via USB-C for user convenience.</p>
    </div>
  </div>
  
  <style>
    /* Additional styling as needed */
    .section {
      background-color: #f9f9f9;
      border-radius: 10px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
      padding: 20px;
      margin-bottom: 20px;
    }
  
    .section-title {
      font-size: 1.5rem;
      margin-bottom: 15px;
    }
  
    .section-content {
      font-size: 1rem;
      line-height: 1.5;
    }
  
    .section-content h3 {
      font-size: 1.25rem;
      margin-top: 10px;
    }
  </style>
  