<script>
  import { Menu } from 'svelte-headlessui-4@headlessui/svelte';
  import { HomeIcon, DashboardIcon } from 'heroicons-svelte/outline';
  import { goto } from '$app/navigation';
</script>

<!-- ... existing style rules ... -->

<div class="container">
  <h1>Welcome to AI Project Management System</h1>
  <Menu>
    <Menu.Button class="menu-button">Menu</Menu.Button>
    <Menu.Items class="menu-items">
      <Menu.Item>
        {({ active }) => (
          <a
            href="#"
            class={`menu-item ${active ? 'active' : ''}`}
            on:click|preventDefault={() => goto('/')}
          >
            <HomeIcon class="icon" width={20} height={20} />
            Home
          </a>
        )}
      </Menu.Item>
      <Menu.Item>
        {({ active }) => (
          <a
            href="#"
            class={`menu-item ${active ? 'active' : ''}`}
            on:click|preventDefault={() => goto('/dashboard')}
          >
            <DashboardIcon class="icon" width={20} height={20} />
            Dashboard
          </a>
        )}
      </Menu.Item>
      <!-- Add more menu items here -->
    </Menu.Items>
  </Menu>
  <slot></slot>
</div>