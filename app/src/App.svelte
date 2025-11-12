<script>
  import ChatBoxProduction from "./options/ChatBoxProduction.svelte";
  import OptionSumary from "./options/OptionSumary.svelte";

  let optionChatBox = 0;
  function changeOptionChatBox(value) {
    optionChatBox = value;
  }
</script>

<div class="min-h-screen bg-gray-50 flex flex-col">
  <header
    class="bg-white radius-[8pxs] border-b border-gray-200 py-2 px-2 grind grind-cols-3">
    <button
      class="p-2 rounded-md hover:bg-gray-100"
      on:click={() => changeOptionChatBox(0)}>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        aria-hidden="true"
        role="img">
        <path
          d="M15 6 L9 12 L15 18"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round" />
      </svg>
    </button>

    <h1 class="text-[20px] font-bold text-green-600">Nông Lâm Viên ChatBox</h1>
  </header>
  <main class="flex-1 max-w-4xl w-full mx-auto p-4 flex flex-col">
    {#if optionChatBox === 0}
      <OptionSumary
        {optionChatBox}
        on:changeOptionChatBox={(e) => changeOptionChatBox(e.detail)} />
    {:else if optionChatBox === 1}
      <ChatBoxProduction />
    {/if}
  </main>
  <footer class="text-center py-4 text-sm text-gray-500">
    <p>Nông lâm viên chatbox &copy; 2025</p>
  </footer>
</div>
