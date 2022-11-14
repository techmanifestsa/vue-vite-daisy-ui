<template>
  <div class="drawer">
    <input id="my-drawer-3" type="checkbox" class="drawer-toggle" />
    <div class="drawer-content bg-gray-200 flex flex-col">
      <!-- Navbar -->
      <div class="w-full navbar bg-base-300">
        <div class="wrapper">
          <div class="flex-none lg:hidden">
            <label for="my-drawer-3" class="btn btn-square btn-ghost">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                class="inline-block w-6 h-6 stroke-current"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 6h16M4 12h16M4 18h16"
                ></path>
              </svg>
            </label>
          </div>
          <div class="flex-1 text-lg font-bold">Tech Box</div>
          <div class="flex-none hidden lg:block">
            <ul class="menu menu-horizontal">
              <!-- Navbar menu content here -->
              <li v-for="(link, index) in links" :key="index">
                <a :href="link.url">{{ link.name }}</a>
              </li>
            </ul>
          </div>
          <div class="dropdown dropdown-end">
            <label tabindex="0" class="btn btn-ghost btn-circle avatar">
              <div class="w-10 rounded-full">
                <img src="https://placeimg.com/80/80/people" />
              </div>
            </label>
            <ul
              tabindex="0"
              class="menu menu-compact dropdown-content mt-3 p-2 shadow bg-base-100 rounded-box w-52"
            >
              <li>
                <a class="justify-between">
                  Profile
                  <span class="badge">New</span>
                </a>
              </li>
              <li><a>Settings</a></li>
              <li><a>Logout</a></li>
            </ul>
          </div>
        </div>
      </div>

      <div class="wrapper">
        <div class="content">
          <h1>Content</h1>
        </div>
      </div>
    </div>
    <div class="drawer-side">
      <label for="my-drawer-3" class="drawer-overlay"></label>
      <ul class="menu p-4 w-80 bg-base-100">
        <!-- Sidebar content here -->
        <li v-for="(link, index) in links" :key="index">
          <a :href="link.url">{{ link.name }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      links: [
        { name: "Link 1", url: "/" },
        { name: "Link 2", url: "/" },
        { name: "Link 3", url: "/" },
      ],
    };
  },
};
</script>

<style scoped></style>
