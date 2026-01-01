<script lang="ts">
  import { goto } from "$app/navigation";
  import {
    ArrowRight,
    ChevronDown,
    ChevronLeft,
    ChevronRight,
    CircleHelp,
    ExternalLink,
    ExternalLinkIcon,
    Film,
    House,
  } from "lucide-svelte";
  import Moon from "lucide-svelte/icons/moon";
  import Sun from "lucide-svelte/icons/sun";

  import { ModeWatcher, mode, toggleMode } from "mode-watcher";
  import { fade } from "svelte/transition";

  let currentSlide = $state(0);
  let p1Open = $state(true);
  let p2Open = $state(true);
</script>

<ModeWatcher defaultMode={"dark"} />

<div class="flex items-center justify-between">
  <div class="flex flex-col">
    <p class="text-tertiary text-sm">Hello, my name is</p>
    <p class="qtext-content text-3xl sm:text-4xl xl:text-5xl font-medium">
      Abdullah
    </p>
    <div
      class="flex items-center justify-start space-x-3 sm:space-x-4 mt-3 flex-wrap"
    >
      <button
        onclick={() =>
          window.open(
            "https://www.linkedin.com/in/abdullah-khan-49a876235/",
            "_blank"
          )}
        class="text-sm cursor-pointer flex items-center text-blue-400"
      >
        LinkedIn
      </button>
      <button
        onclick={() =>
          window.open("https://github.com/Abdullahkhan871", "_blank")}
        class="text-sm cursor-pointer flex items-center text-[#14A800]"
      >
        github
      </button>
      <div class="h-4 w-[1px] bg-tertiary/20 sm:hidden"></div>
      <button
        onclick={toggleMode}
        class="hover:bg-tertiary/20 transition cursor-pointer sm:hidden rounded-md h-8 w-8 p-1"
      >
        {#if mode.current === "dark"}
          <Moon class="h-full w-full" />
        {:else}
          <Sun class="h-full w-full p-[1px]" />
        {/if}
      </button>
    </div>
  </div>
  <div class="hidden sm:flex items-center space-x-4 z-10">
    <button
      onclick={toggleMode}
      class="hover:bg-tertiary/20 scale-125 mt-5 transition cursor-pointer rounded-md h-8 w-8 p-1"
    >
      {#if mode.current === "dark"}
        <Moon class="h-full w-full" />
      {:else}
        <Sun class="h-full w-full p-[1px]" />
      {/if}
    </button>
  </div>
</div>
<div class="my-8 h-[2px] w-full bg-tertiary/20 rounded-full"></div>
<div class="flex flex-col w-full">
  <div class="flex justify-between items-center">
    <div class="text-sm font-medium text-tertiary">Skillset</div>
  </div>
  <div class="flex items-center gap-y-2 space-x-2 flex-wrap mt-8">
    <div
      class="dark:bg-muted/20 bg-muted/10 text-sm sm:text-base h-8 px-2 sm:px-3 sm:py-2 sm:h-auto rounded-sm flex items-center select-none"
    >
      JavaScript
      <svg
        class="inline-block ml-1.5 sm:ml-2 h-3.5 w-3.5 sm:h-4.5 sm:w-4.5"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 32 32"
        ><path
          fill="currentColor"
          d="M0 0h32v32H0zm29.38 24.37c-.234-1.464-1.188-2.688-4.005-3.833c-.979-.458-2.073-.781-2.396-1.521c-.12-.438-.141-.677-.063-.938c.203-.865 1.219-1.12 2.021-.88c.521.161 1 .557 1.302 1.198c1.38-.901 1.38-.901 2.339-1.5c-.359-.557-.536-.802-.781-1.036c-.839-.943-1.958-1.422-3.776-1.38l-.943.12c-.901.219-1.76.698-2.281 1.339c-1.516 1.719-1.078 4.719.76 5.964c1.818 1.359 4.479 1.656 4.823 2.938c.318 1.563-1.161 2.063-2.625 1.88c-1.078-.24-1.677-.781-2.339-1.781l-2.438 1.401c.276.641.599.917 1.078 1.479c2.318 2.339 8.12 2.219 9.161-1.339c.036-.12.318-.943.099-2.198zm-11.979-9.662h-2.995c0 2.583-.016 5.151-.016 7.74c0 1.641.083 3.151-.182 3.615c-.443.917-1.573.802-2.089.641c-.526-.26-.797-.62-1.104-1.141c-.089-.141-.151-.26-.172-.26l-2.432 1.5c.406.839 1 1.563 1.766 2.021c1.141.682 2.672.901 4.276.542c1.042-.302 1.943-.922 2.411-1.88c.682-1.24.536-2.76.531-4.464c.016-2.74 0-5.479 0-8.24z"
        /></svg
      >
    </div>
    <div
      class="dark:bg-muted/20 bg-muted/10 text-sm sm:text-base h-8 px-2 sm:px-3 sm:py-2 sm:h-auto rounded-sm flex items-center select-none"
    >
      TypeScript
      <svg
        class="inline-block ml-1.5 sm:ml-2 h-3.5 w-3.5 sm:h-4.5 sm:w-4.5"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 24 24"
        ><g fill="none"
          ><g clip-path="url(#akarIconsTypescriptFill0)"
            ><path
              fill="currentColor"
              d="M23.429 0H.57A.57.57 0 0 0 0 .571V23.43a.57.57 0 0 0 .571.571H23.43a.57.57 0 0 0 .571-.571V.57a.57.57 0 0 0-.572-.57m-9.143 12.826h-2.857v8.888H9.143v-8.888H6.286v-1.969h8zm.64 8.38v-2.375s1.298.978 2.855.978s1.497-1.018 1.497-1.158c0-1.477-4.412-1.477-4.412-4.751c0-4.452 6.429-2.695 6.429-2.695l-.08 2.116s-1.078-.719-2.296-.719s-1.657.58-1.657 1.198c0 1.597 4.452 1.438 4.452 4.652c0 4.95-6.788 2.755-6.788 2.755"
            /></g
          ><defs
            ><clipPath id="akarIconsTypescriptFill0"
              ><path fill="#fff" d="M0 0h24v24H0z" /></clipPath
            ></defs
          ></g
        ></svg
      >
    </div>
    <div
      class="dark:bg-muted/20 bg-muted/10 text-sm sm:text-base h-8 px-2 sm:px-3 sm:py-2 sm:h-auto rounded-sm flex items-center select-none"
    >
      React.JS
      <svg
        class="inline-block ml-1.5 sm:ml-2 h-3.5 w-3.5 sm:h-4.5 sm:w-4.5"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 24 24"
        ><path
          fill="currentColor"
          d="M12 10.11c1.03 0 1.87.84 1.87 1.89c0 1-.84 1.85-1.87 1.85S10.13 13 10.13 12c0-1.05.84-1.89 1.87-1.89M7.37 20c.63.38 2.01-.2 3.6-1.7c-.52-.59-1.03-1.23-1.51-1.9a23 23 0 0 1-2.4-.36c-.51 2.14-.32 3.61.31 3.96m.71-5.74l-.29-.51c-.11.29-.22.58-.29.86c.27.06.57.11.88.16zm6.54-.76l.81-1.5l-.81-1.5c-.3-.53-.62-1-.91-1.47C13.17 9 12.6 9 12 9s-1.17 0-1.71.03c-.29.47-.61.94-.91 1.47L8.57 12l.81 1.5c.3.53.62 1 .91 1.47c.54.03 1.11.03 1.71.03s1.17 0 1.71-.03c.29-.47.61-.94.91-1.47M12 6.78c-.19.22-.39.45-.59.72h1.18c-.2-.27-.4-.5-.59-.72m0 10.44c.19-.22.39-.45.59-.72h-1.18c.2.27.4.5.59.72M16.62 4c-.62-.38-2 .2-3.59 1.7c.52.59 1.03 1.23 1.51 1.9c.82.08 1.63.2 2.4.36c.51-2.14.32-3.61-.32-3.96m-.7 5.74l.29.51c.11-.29.22-.58.29-.86c-.27-.06-.57-.11-.88-.16zm1.45-7.05c1.47.84 1.63 3.05 1.01 5.63c2.54.75 4.37 1.99 4.37 3.68s-1.83 2.93-4.37 3.68c.62 2.58.46 4.79-1.01 5.63c-1.46.84-3.45-.12-5.37-1.95c-1.92 1.83-3.91 2.79-5.38 1.95c-1.46-.84-1.62-3.05-1-5.63c-2.54-.75-4.37-1.99-4.37-3.68s1.83-2.93 4.37-3.68c-.62-2.58-.46-4.79 1-5.63c1.47-.84 3.46.12 5.38 1.95c1.92-1.83 3.91-2.79 5.37-1.95M17.08 12c.34.75.64 1.5.89 2.26c2.1-.63 3.28-1.53 3.28-2.26s-1.18-1.63-3.28-2.26c-.25.76-.55 1.51-.89 2.26M6.92 12c-.34-.75-.64-1.5-.89-2.26c-2.1.63-3.28 1.53-3.28 2.26s1.18 1.63 3.28 2.26c.25-.76.55-1.51.89-2.26m9 2.26l-.3.51c.31-.05.61-.1.88-.16c-.07-.28-.18-.57-.29-.86zm-2.89 4.04c1.59 1.5 2.97 2.08 3.59 1.7c.64-.35.83-1.82.32-3.96c-.77.16-1.58.28-2.4.36c-.48.67-.99 1.31-1.51 1.9M8.08 9.74l.3-.51c-.31.05-.61.1-.88.16c.07.28.18.57.29.86zm2.89-4.04C9.38 4.2 8 3.62 7.37 4c-.63.35-.82 1.82-.31 3.96a23 23 0 0 1 2.4-.36c.48-.67.99-1.31 1.51-1.9"
        /></svg
      >
    </div>
    <div
      class="dark:bg-muted/20 bg-muted/10 text-sm sm:text-base h-8 px-2 sm:px-3 sm:py-2 sm:h-auto rounded-sm flex items-center select-none"
    >
      React Native
      <svg
        class="inline-block ml-1.5 sm:ml-2 h-3.5 w-3.5 sm:h-4.5 sm:w-4.5"
        xmlns="http://www.w3.org/2000/svg"
        width="200"
        height="200"
        viewBox="0 0 24 24"
        fill="currentColor"
        ><g
          fill="none"
          stroke="currentColor"
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          ><path
            d="M6.357 9C3.72 9.68 2 10.845 2 12.175C2 14.282 6.405 16 11.85 16c.74 0 1.26-.039 1.95-.097"
          /><path
            d="M9.837 15.9c-.413-.596-.806-1.133-1.18-1.8c-2.751-4.9-3.488-9.77-1.63-10.873c1.15-.697 3.047.253 4.974 2.254"
          /><path
            d="M6.429 15.387c-.702 2.688-.56 4.716.56 5.395c1.783 1.08 5.387-1.958 8.043-6.804c.36-.67.683-1.329.968-1.978"
          /><path
            d="M12 18.52c1.928 2 3.817 2.95 4.978 2.253c1.85-1.102 1.121-5.972-1.633-10.873c-.384-.677-.777-1.204-1.18-1.8"
          /><path
            d="M17.66 15c2.612-.687 4.34-1.85 4.34-3.176C22 9.714 17.592 8 12.155 8c-.747 0-1.266.029-1.955.087"
          /><path
            d="M8 12c.285-.66.607-1.308.968-1.978c2.647-4.844 6.253-7.89 8.046-6.801c1.11.679 1.262 2.706.56 5.393m-5.314 3.401h-.01c-.01.13-.12.24-.26.24a.263.263 0 0 1-.25-.26c0-.14.11-.25.24-.25h-.01c.13-.01.25.11.25.24"
          /></g
        ></svg
      >
    </div>
    <div
      class="dark:bg-muted/20 bg-muted/10 text-sm sm:text-base h-8 px-2 sm:px-3 sm:py-2 sm:h-auto rounded-sm flex items-center select-none"
    >
      Tailwind
      <svg
        class="inline-block ml-1.5 sm:ml-2 h-4 w-4 sm:h-5 sm:w-5"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 24 24"
        ><path
          fill="currentColor"
          d="M12 6c-2.67 0-4.33 1.33-5 4c1-1.33 2.17-1.83 3.5-1.5c.76.19 1.31.74 1.91 1.35c.98 1 2.09 2.15 4.59 2.15c2.67 0 4.33-1.33 5-4c-1 1.33-2.17 1.83-3.5 1.5c-.76-.19-1.3-.74-1.91-1.35C15.61 7.15 14.5 6 12 6m-5 6c-2.67 0-4.33 1.33-5 4c1-1.33 2.17-1.83 3.5-1.5c.76.19 1.3.74 1.91 1.35C8.39 16.85 9.5 18 12 18c2.67 0 4.33-1.33 5-4c-1 1.33-2.17 1.83-3.5 1.5c-.76-.19-1.3-.74-1.91-1.35C10.61 13.15 9.5 12 7 12"
        /></svg
      >
    </div>
    <div
      class="dark:bg-muted/20 bg-muted/10 text-sm sm:text-base h-8 px-2 sm:px-3 sm:py-2 sm:h-auto rounded-sm flex items-center select-none"
    >
      Node.JS
      <svg
        class="inline-block ml-1.5 sm:ml-2 h-3.5 w-3.5 sm:h-4.5 sm:w-4.5"
        xmlns="http://www.w3.org/2000/svg"
        width="200"
        height="200"
        viewBox="0 0 24 24"
        ><path
          fill="currentColor"
          d="M11.899 24c-.322 0-.64-.084-.923-.247l-2.935-1.738c-.439-.245-.225-.332-.08-.382c.584-.204.703-.25 1.327-.605c.066-.037.152-.024.219.015l2.255 1.339a.298.298 0 0 0 .273 0l8.794-5.077a.277.277 0 0 0 .134-.237V6.919a.282.282 0 0 0-.136-.242l-8.79-5.072a.27.27 0 0 0-.271 0l-8.79 5.072a.28.28 0 0 0-.139.24v10.148c0 .097.053.19.137.236l2.408 1.391c1.308.654 2.107-.116 2.107-.891V7.785a.25.25 0 0 1 .255-.254h1.114c.139 0 .253.11.253.254v10.02c0 1.744-.95 2.745-2.604 2.745c-.509 0-.91 0-2.028-.55l-2.307-1.33a1.86 1.86 0 0 1-.922-1.605V6.917c0-.66.352-1.277.922-1.602L10.976.236a1.928 1.928 0 0 1 1.849 0l8.792 5.08c.568.329.922.943.922 1.603v10.149a1.86 1.86 0 0 1-.922 1.602l-8.792 5.079a1.848 1.848 0 0 1-.927.246V24Zm2.716-6.993c-3.848 0-4.654-1.766-4.654-3.248c0-.14.113-.253.254-.253h1.136c.126 0 .231.091.251.215c.172 1.158.683 1.742 3.01 1.742c1.853 0 2.641-.419 2.641-1.402c0-.566-.225-.986-3.104-1.268c-2.408-.238-3.896-.768-3.896-2.694c0-1.775 1.497-2.831 4.004-2.831c2.815 0 4.211.977 4.387 3.077a.256.256 0 0 1-.255.278h-1.143a.252.252 0 0 1-.246-.199c-.275-1.217-.94-1.607-2.747-1.607c-2.023 0-2.259.705-2.259 1.233c0 .64.277.828 3.007 1.189c2.703.359 3.987.865 3.987 2.765c0 1.915-1.599 3.014-4.385 3.014l.012-.01Z"
        /></svg
      >
    </div>

    <div
      class="dark:bg-muted/20 bg-muted/10 text-sm sm:text-base h-8 px-2 sm:px-3 sm:py-2 sm:h-auto rounded-sm flex items-center select-none"
    >
      Express.JS
      <svg
        class="inline-block ml-1.5 sm:ml-2 h-3.5 w-3.5 sm:h-4 sm:w-4"
        xmlns="http://www.w3.org/2000/svg"
        width="200"
        height="200"
        viewBox="0 0 24 24"
        ><path
          fill="currentColor"
          d="M24 18.588a1.529 1.529 0 0 1-1.895-.72l-3.45-4.771l-.5-.667l-4.003 5.444a1.466 1.466 0 0 1-1.802.708l5.158-6.92l-4.798-6.251a1.595 1.595 0 0 1 1.9.666l3.576 4.83l3.596-4.81a1.435 1.435 0 0 1 1.788-.668L21.708 7.9l-2.522 3.283a.666.666 0 0 0 0 .994l4.804 6.412zM.002 11.576l.42-2.075c1.154-4.103 5.858-5.81 9.094-3.27c1.895 1.489 2.368 3.597 2.275 5.973H1.116C.943 16.447 4.005 19.009 7.92 17.7a4.078 4.078 0 0 0 2.582-2.876c.207-.666.548-.78 1.174-.588a5.417 5.417 0 0 1-2.589 3.957a6.272 6.272 0 0 1-7.306-.933a6.575 6.575 0 0 1-1.64-3.858c0-.235-.08-.455-.134-.666A88.33 88.33 0 0 1 0 11.577zm1.127-.286h9.654c-.06-3.076-2.001-5.258-4.59-5.278c-2.882-.04-4.944 2.094-5.071 5.264z"
        /></svg
      >
    </div>
    <div
      class="dark:bg-muted/20 bg-muted/10 text-sm sm:text-base h-8 px-2 sm:px-3 sm:py-2 sm:h-auto rounded-sm flex items-center select-none"
    >
      Mongo Db
      <svg
        class="inline-block ml-1.5 sm:ml-2 h-3.5 w-3.5 sm:h-4 sm:w-4"
        xmlns="http://www.w3.org/2000/svg"
        width="200"
        height="200"
        viewBox="0 0 24 24"
        ><path
          fill="currentColor"
          fill-rule="evenodd"
          d="M7.294 11.804c0-3.966 2.14-6.417 3.533-8.014C11.501 3.02 12 2.447 12 2c0 .447.5 1.019 1.172 1.79c1.394 1.597 3.534 4.048 3.534 8.014c0 4.326-2.75 6.95-4.077 7.765L12.37 22h-.707l-.29-2.43c-1.326-.813-4.079-3.437-4.079-7.766m4.064 6.7L12 9.06l.649 9.446l-.65.75z"
          clip-rule="evenodd"
        /></svg
      >
    </div>
  </div>
</div>
<div class="my-8 h-[2px] w-full bg-tertiary/20 rounded-full"></div>

<div class="flex flex-col w-full">
  <!-- Coastal UI Project -->
  <!-- Preload images -->
  <!-- <div class="hidden">
    <img src="ecom" alt="preload" />
    <img src="coastal2.png" alt="preload" />
    <img src="clutch1.png" alt="preload" />
    <img src="clutch2.png" alt="preload" />
    <img src="clutch3.png" alt="preload" />
  </div> -->
  <div class="flex flex-col items-start">
    <div
      onclick={() => (p1Open = !p1Open)}
      class="flex items-center cursor-pointer transition rounded-md justify-between grow w-full"
    >
      <div class="flex flex-col">
        <div class="text-xl tracking-tight font-medium flex items-center">
          Forever Ecommerce
          <a
            href="https://forever-ecommerce-jet.vercel.app/"
            target="_blank"
            class="hidden sm:flex ml-1 items-center cursor-pointer group hover:bg-tertiary/10 p-1 rounded-md relative w-6.5"
          >
            <div
              class="absolute bottom-8 rounded-md border border-tertiary/30 left-1/2 -translate-x-1/2 whitespace-nowrap px-2 py-1 text-center text-xs opacity-0 bg-background group-hover:opacity-100 pointer-events-none transition"
            >
              Open Website
            </div>
            <ExternalLinkIcon strokeWidth={1.5} class="h-5 w-5" />
          </a>
        </div>
        <p class="text-content/80 sm:text-md text-sm mt-1">
          A library of modern, dark UI elements for Tailwind CSS + Svelte. Over
          4,000 unique visitors from Reddit and madewithsvelte.
        </p>
      </div>
      <div class={`ml-4 ${p1Open ? "rotate-180" : ""}`}>
        <ChevronDown strokeWidth={1.5} />
      </div>
    </div>
    {#if p1Open}
      <!-- Desktop Grid -->
      <div
        class="hidden sm:grid grid-cols-7 grid-rows-2 w-full mt-5 gap-1 h-[340px]"
      >
        <img
          src="ecom.png"
          class="row-span-2 col-span-5 rounded-md border border-secondary-muted/20 h-full object-contain"
        />
        <img
          src="coastal2.png"
          class="row-span-1 col-span-2 rounded-md object-cover border border-secondary-muted/20 h-full"
        />
        <img
          src="coastal2.png"
          class="row-span-1 col-span-2 rounded-md object-cover border border-secondary-muted/20 h-full"
        />
      </div>
      <!-- Mobile Single Image -->
      <div class="sm:hidden mt-5">
        <img
          src="ecom.png"
          class="w-full rounded-md border border-secondary-muted/20 object-cover"
        />
        <a
          href="https://www.coastalui.com"
          target="_blank"
          class="w-full bg-content rounded-md mt-3 flex items-center justify-center text-background py-3"
        >
          Open Live Website
          <ExternalLink class="h-4 w-4 ml-2" />
        </a>
      </div>
    {/if}
  </div>

  <!-- Clutch Maps Project -->
  <div class="flex flex-col items-start mt-12">
    <div
      onclick={() => (p2Open = !p2Open)}
      class="flex items-center cursor-pointer transition rounded-md justify-between grow w-full"
    >
      <div class="flex flex-col">
        <div class="text-xl tracking-tight font-medium flex items-center">
          Forever Ecommerce Admin
          <a
            href="https://forever-ecommerce-admin-psi.vercel.app/"
            target="_blank"
            class="hidden sm:flex ml-1 items-center cursor-pointer group hover:bg-tertiary/10 p-1 rounded-md relative w-6.5"
          >
            <div
              class="absolute bottom-8 rounded-md border border-tertiary/30 left-1/2 -translate-x-1/2 whitespace-nowrap px-2 py-1 text-center text-xs opacity-0 bg-background group-hover:opacity-100 pointer-events-none transition"
            >
              Open Website
            </div>
            <ExternalLinkIcon strokeWidth={1.5} class="h-5 w-5" />
          </a>
        </div>
        <p class="text-content/80 mt-1 sm:text-md text-sm">
          A web app for finding great driving routes near you. Currently built
          with Svelte + Mapbox, but currently in open beta.
        </p>
      </div>
      <div class={`ml-4 ${p2Open ? "rotate-180" : ""}`}>
        <ChevronDown strokeWidth={1.5} />
      </div>
    </div>
    {#if p2Open}
      <!-- Desktop Grid -->
      <div
        class="hidden sm:grid grid-cols-7 grid-rows-2 w-full mt-5 gap-1 h-[370px]"
      >
        <img
          src="clutch1.png"
          class="row-span-2 col-span-5 rounded-md border border-secondary-muted/30 h-full object-cover"
        />
        <img
          src="clutch2.png"
          class="row-span-1 col-span-2 rounded-md object-cover border border-secondary-muted/30 h-full"
        />
        <img
          src="clutch3.png"
          class="row-span-1 col-span-2 rounded-md object-cover border border-secondary-muted/30 h-full"
        />
      </div>
      <!-- Mobile Single Image -->
      <div class="sm:hidden mt-5">
        <img
          src="clutch1.png"
          class="w-full rounded-md border border-secondary-muted/30 object-cover"
        />
        <a
          href="https://www.clutchmaps.com"
          target="_blank"
          class="w-full bg-content rounded-md mt-3 flex items-center justify-center text-background py-3"
        >
          Open Live Website
          <ExternalLink class="h-4 w-4 ml-2" />
        </a>
      </div>
    {/if}
  </div>
</div>

<div class="mt-16 h-[2px] w-full bg-tertiary/20 rounded-full"></div>
