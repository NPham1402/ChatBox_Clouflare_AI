<script>
  import ChatBoxProduction from "./options/ChatBoxProduction.svelte";
  import OptionSumary from "./options/OptionSumary.svelte";

  let optionChatBox = 0;
</script>

<div class="min-h-screen bg-gray-50 flex flex-col">
  <header
    class="bg-white radius-[8pxs] border-b border-gray-200 py-2 px-2 text-center"
  >
    <h1 class="text-[20px] font-bold text-green-600">Nông Lâm Viên ChatBox</h1>
  </header>
  <main class="flex-1 max-w-4xl w-full mx-auto p-4 flex flex-col">
    {#if optionChatBox === 0}
      <OptionSumary />
    {:else if optionChatBox === 1}
      <ChatBoxProduction />
    {/if}
  </main>
  <footer class="text-center py-4 text-sm text-gray-500">
    <p>Nông lâm viên chatbox &copy; 2025</p>
  </footer>
</div>
