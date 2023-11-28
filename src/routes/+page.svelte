<script lang="ts">
    // TypeScript script part (if needed for interactivity)
  </script>
  
  <!-- A Div With A Centered Product Image -->
  <div class="w-screen h-screen flex flex-col justify-center items-center">
      <div class="flex justify-center items-center mb-8">
          <img src="src/lib/VR_IMAGE.png" alt="VR Health Monitoring System" class="max-w-xs md:max-w-sm lg:max-w-md xl:max-w-lg" />
      </div>
  
      <section class="helped text-center w-full px-4 md:px-8 lg:px-12 h-full" aria-hidden="true">
        <div class="container mx-auto">
          <div class="row">
            <div class="col-12">
              <div class="titleBlock">VR Health Monitoring System</div>
              <div class="helped__text">Integrating heart rate and breathing rate measurement with VR technology for a comprehensive user experience.</div>
            </div>
          </div>
        </div>
      </section>
  </div>
  
  <style>
    .helped {
      color: #fff;
      background: linear-gradient(#556dee 0, #833ee4 100%);
      padding: 40px 0;
      overflow: hidden;
    }
  
    .titleBlock {
      font-weight: 600;
      font-size: 48px; /* Adjusted for better readability */
      line-height: 1.2;
      margin-bottom: 20px; /* Adjusted margin */
    }
  
    .helped__text {
      font-size: 22px; /* Adjusted for better readability */
      line-height: 1.5;
      letter-spacing: 0.5px; /* Adjusted letter spacing */
      width: 80%; /* Increased width for better text distribution */
      margin: 0 auto;
      max-width: 600px; /* Max width added for larger screens */
    }
  
    .row {
      display: flex;
      flex-wrap: wrap;
      margin-right: -15px;
      margin-left: -15px;
    }
  
    .col-12 {
      flex: 0 0 100%;
      max-width: 100%;
    }
  
    /* Responsive adjustments */
    @media (max-width: 768px) {
      .titleBlock {
        font-size: 42px;
      }
  
      .helped__text {
        font-size: 14px;
        width: 100%;
      }
  
      .helped {
        padding: 30px 0;
      }
    }
  </style>
  