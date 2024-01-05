<script lang="ts">
  import "../app.css";
  import { onMount } from 'svelte';
  let div1: HTMLDivElement;
  let div2: HTMLDivElement;
  let height: string;

  onMount(() => {
    height = `calc(100% - ${div2.offsetHeight}px)`;
  });
</script>

<body class="w-screen h-screen bg-stone-950 flex justify-center items-center">
  <wrapper class="h-5/6 w-5/6 max-h-[500px] max-w-[750px] aspect-auto relative bg-stone-950">
    <div class="h-full w-8/12 ml-2 absolute right-0 bg-[#303030] rounded-r-[4rem] rounded-tl-[3rem]">
      <div class="h-[calc(100%-1rem)] w-[calc(100%-1rem)] m-2 bg-[#f7f7e6] rounded-r-[3.5rem] rounded-tl-[2.5rem]"></div>
      <div bind:this={div1} class="h-[90%] w-1/2 bg-[#303030] absolute bottom-0 left-[-48.33333%] rounded-bl-[4rem] rounded-tl-[3rem]" style={`height: ${height}`}>
        <div class="h-[calc(100%-1rem)] w-[100%] m-2 bg-[#f7f7e6] absolute bottom-0 rounded-bl-[3.5rem] rounded-tl-[2.5rem]"></div>
      </div>
    </div>
    <div bind:this={div2} class="w-2/6 aspect-square bg-[#303030] absolute">
      <div class="h-full w-full rounded-br-[50%] bg-stone-950 absolute">
        <div class="h-[calc(100%-3rem)] max-h-[250px] m-6 aspect-square bg-[#dcdcc6] rounded-full overflow-hidden">
          <img src="/updated2@3x.png" alt="my pfp">
        </div>
      </div>
    </div>
  </wrapper>
</body>

<!-- #f7f7e6 -->