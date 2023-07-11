<script>
    import { Menu } from 'svelte-headlessui-4';
    import { HomeIcon, UserGroupIcon } from 'heroicons-svelte/outline';
  </script>
  
  <style>
    @import 'https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap';
    
    :root {
      --primary: #0A192F;
      --accent: #FFC300;
      --light-blue: #88BEE3;
      --light-grey: #D8D8D8;
      --dark-grey: #565656;
      --black: #000000;
      --white: #FFFFFF;
    }
  
    body {
      font-family: 'Roboto', sans-serif;
      background-color: var(--primary);
      color: var(--white);
    }
  
    h1 {
      font-weight: bold;
      color: var(--accent);
      font-size: 2em;
      margin-bottom: 1em;
    }
  
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 2em;
    }
  
    .menu-item {
      color: var(--light-grey);
      padding: 1em;
      display: flex;
      align-items: center;
    }
  
    .menu-item:hover {
      background-color: var(--light-blue);
      color: var(--black);
    }
  
    .icon {
      margin-right: 0.5em;
    }
  </style>
  
  <div class="container">
    <h1>Welcome to AI Project Management System</h1>
    <Menu>
      <Menu.Button class="menu-button">Menu</Menu.Button>
      <Menu.Items class="menu-items">
        <Menu.Item>
          {({ active }) => (
            <a href="/home" class={`menu-item ${active ? 'active' : ''}`}>
              <HomeIcon class="icon" width={20} height={20} />
              Home
            </a>
          )}
        </Menu.Item>
        <Menu.Item>
          {({ active }) => (
            <a href="/teams" class={`menu-item ${active ? 'active' : ''}`}>
              <UserGroupIcon class="icon" width={20} height={20} />
              Teams
            </a>
          )}
        </Menu.Item>
        <!-- Add more menu items here -->
      </Menu.Items>
    </Menu>
    <!-- Add more content for homepage here -->
  </div>
  