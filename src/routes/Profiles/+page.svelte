<script lang="ts">
    import logo from "$lib/logo.png";
    import AudreyHeadshot from "$lib/Audrey_ProfilePic.png";
    import TimofeyHeadshot from "$lib/Timofey_ProfilePic.png";
  </script>
  
  <!-- Team Profiles Section -->
  <div class="bg-gray-100 py-8">
    <div class="container mx-auto px-4">
      <h1 class="text-4xl font-bold text-center mb-6">Our Team</h1>
      
      <!-- Mason's Profile -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mb-8">
        <!-- Team Member 1 -->
        <div class="bg-white shadow-lg rounded-lg p-4 text-center">
          <img src="https://gohuskies.com/images/2022/8/15/Wheeler_Mason_2022_UW_FB.jpg" alt="Mason Wheeler" class="w-32 h-32 object-contain mx-auto mb-4">
          <h2 class="font-semibold text-xl">Mason Wheeler</h2>
          <p class="text-gray-600">Project Manager</p>
          <p>Email: masewheeler@outlook.com</p>
          <p>Phone: (360)-975-8555 </p>
        </div>

        <!-- Audrey Profile  -->
        <div class="bg-white shadow-lg rounded-lg p-4 text-center">
          <img src={AudreyHeadshot} alt="Audrey" class="w-32 h-32 object-contain mx-auto mb-4">
          <h2 class="font-semibold text-xl">Audrey Chang</h2>
          <p class="text-gray-600">Software Developer</p>
          <p>Email: changaud@uw.edu</p>
          <p> Phone: (253)332-0407 </p>
        </div>

        <!-- Timofey Profile Timofey Popov
            Group Creative Director
            (425)-638-3555, popovt@uw.edu
              -->
        <div class="bg-white shadow-lg rounded-lg p-4 text-center">
          <img src={TimofeyHeadshot} alt="Timofey" class="w-32 h-32 object-contain mx-auto mb-4">
          <h2 class="font-semibold text-xl">Timofey Popov</h2>
          <p class="text-gray-600">Group Creative Director</p>
          <p>Email: popovt@uw.edu</p>
          <p>Phone: (425)-638-3555 </p>
          </div>
          

  
      </div>
  
      <!-- Team Charter Section -->
      <div class="bg-white shadow-lg rounded-lg p-6">
        <h2 class="text-3xl font-semibold text-center mb-4">Team Charter</h2>
        
        <!-- Team Name and Logo -->
        <div class="text-center mb-4">
          <img src={logo} alt="Team Logo" class="mx-auto mb-2 h-96 w-96">
          <h3 class="font-semibold text-xl">Innovators in VR Health</h3>
        </div>
  
        <!-- Team Rules and Expectations -->
        <h3 class="font-semibold text-lg mb-2">Team Rules and Expectations</h3>
        <ul class="list-disc list-inside mb-4">
            <li>Treat all team members with respect</li>
            <li>Be punctual and attend all meetings</li>
            <li>Keep User's at the center of all decisions</li>
            <li>Be open to new ideas and perspectives</li>
            <li>Be honest and transparent</li>
            <li>Be accountable for your actions</li>
            <li>Be willing to learn and grow</li>
            <li>Be willing to help others</li>
        </ul>
  
        <!-- Expertise and Deficiencies -->
        <h3 class="font-semibold text-lg mb-2">Areas of Expertise and Deficiencies</h3>
        <p>Our team has a wide range of expertise and skills, including but not limited to:</p>
        <ul class="list-disc list-inside mb-4">
          <li>Software Development</li>
          <li>Hardware Development</li>
          <li>Project Management</li>
          <li>Technical Writing</li>
          <li>Graphic Design</li>
          <li>Marketing</li>
          <li>Business Management</li>
          </ul>
  
        <!-- Role Assignments -->
        <h3 class="font-semibold text-lg mb-2">Role Assignments</h3>
        <ul class="list-disc list-inside">
          <li>Team Lead: Mason Wheeler</li>
          <li>Documentation Lead: Jane Smith</li>
          <!-- More roles here -->
        </ul>
      </div>
    </div>
  </div>
  
  <style>
    /* Additional styling if needed */
  </style>
  