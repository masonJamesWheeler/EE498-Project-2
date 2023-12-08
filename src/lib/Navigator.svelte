<script lang="ts">
  let isNavOpen = false;

  const menuItems = [
    { path: '/', label: 'Home' },
    { path: '/Background', label: 'Background' },
    { path: '/Profiles', label: 'Profiles' },
    { path: '/Plan', label: 'Plan' },
    { path: '/StakeholderAnalysis', label: 'Stakeholder Analysis' },
    { path: '/Requirements', label: 'Requirements' },
    { path: '/Conops', label: 'Conops' },
    { path: '/Pugh_Matrix', label: 'Pugh Matrix' },
    { path: '/Test_Plan', label: 'Test Plan' },
    { path: '/SystemDesign', label: 'System Design' },
];

  var currentPath = "Home";

  function updateCurrentPage(name: string) {
    currentPath = name;
  }

  function isActive(name: string) {
    return currentPath === name;
  }

</script>


<nav class="bg-white border-gray-200">
  <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
    <a href="/" class="flex items-center space-x-3 rtl:space-x-reverse">
      <img src="https://cdn-icons-png.flaticon.com/512/3197/3197712.png" class="h-8" alt="Flowbite Logo" />
      <span class="self-center text-2xl font-semibold whitespace-nowrap">EE 496</span>
    </a>
    <button on:click={() => isNavOpen = !isNavOpen} type="button" class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200">
      <span class="sr-only">Open main menu</span>
      <svg class="w-5 h-5" aria-hidden="true" fill="none" viewBox="0 0 17 14">
        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15"/>
      </svg>
    </button>
    <!-- Navigation items for mobile view -->
    {#if isNavOpen}
    <div class="w-full md:hidden">
      <ul class="font-medium flex flex-col p-4 mt-4 border border-gray-100 rounded-lg bg-gray-50">
        {#each menuItems as item}
          <li>
            <a href="{item.path}" class:active={isActive(item.path)} class="block py-2 px-3 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0" on:click={() => updateCurrentPage(item.path)}>
              {item.label}
          </li>
        {/each}
      </ul>
    </div>
  {/if}
     <!-- Regular Layout -->
  <div class="hidden w-full md:block md:w-auto" id="navbar-default">
    <ul class="font-medium flex flex-col p-4 md:p-0 mt-4 border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-8 rtl:space-x-reverse md:mt-0 md:border-0 md:bg-white">
      {#each menuItems as item}
        <li>
          <a href={item.path} class:active={isActive(item.path)} class="block py-2 px-3 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 " on:click={() => updateCurrentPage(item.path)}>
            {item.label}
          </a>
        </li>
      {/each}
    </ul>
  </div>
</nav>

<style>
  .active {
    background-color: #2563EB;
    color: white;
  }
</style>
  