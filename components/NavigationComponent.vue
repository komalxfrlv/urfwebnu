<template>
  <header class="header">
    <nav class="navbar">
      <!-- LOGO -->
      <div class="logo">URFU</div>

      <!-- NAVIGATION MENU -->
      <ul class="nav-links">

        <!-- USING CHECKBOX HACK -->
        <input type="checkbox" id="checkbox_toggle" />
        <label for="checkbox_toggle" class="hamburger">&#9776;</label>

        <!-- NAVIGATION MENUS -->
        <div class="menu">
          <li><a href="/">Главная</a></li>
          <li><a href="/products">Продукция</a></li>
          <li><a href="/">Услуги</a></li>
          <li><a href="/">Новости</a></li>
          <li><a href="/about">О компании</a></li>
          <li><a href="/contacts">Контакты</a></li>
        </div>
      </ul>
    </nav>
  </header>
</template>
<style lang="scss" scoped>
/* NAVBAR STYLING STARTS */
.header {
  position: fixed;
  width: 100%;
  z-index: 1488;
  box-shadow: rgba(0, 0, 0, 0.16) 0px 10px 36px 0px, rgba(0, 0, 0, 0.06) 0px 0px 0px 1px;
}

.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20px;
  color: #2e2e2e;
  background-color: #fff;
}

.nav-links {
  margin-bottom: 0rem !important;
}

.nav-links a {
  font-weight: 300;
  color: #2e2e2e;
}

/* LOGO */
.logo {
  font-size: 32px;
  font-weight: 300;
}

/* NAVBAR MENU */
.menu {
  display: flex;
  gap: 1em;
  font-size: 18px;
}

.menu li:hover {
  text-decoration: underline;
  border-radius: 5px;
  transition: 0.3s ease;
}

.menu li {
  padding: 5px 14px;
}

/* DROPDOWN MENU */
.services {
  position: relative;
}

.dropdown {
  background-color: #fff;
  padding: 1em 0;
  position: absolute;
  /*WITH RESPECT TO PARENT*/
  display: none;
  border-radius: 8px;
  top: 35px;
}

.dropdown li+li {
  margin-top: 10px;
}

.dropdown li {
  padding: 0.5em 1em;
  width: 8em;
  text-align: center;
}

.dropdown li:hover {
  background-color: #fff;
}

.services:hover .dropdown {
  display: block;
}

/* RESPONSIVE NAVBAR MENU STARTS */

/* CHECKBOX HACK */

input[type=checkbox] {
  display: none;
}

/* HAMBURGER MENU */
.hamburger {
  display: none;
  font-size: 24px;
  user-select: none;
}

/* APPLYING MEDIA QUERIES */
@media (max-width: 768px) {
  .menu {
    display: none;
    position: absolute;
    background-color: #fff;
    right: 0;
    left: 0;
    text-align: center;
    padding: 16px 0;
  }

  .menu li:hover {
    display: inline-block;
    background-color: #fff;
    transition: 0.3s ease;
  }

  .menu li+li {
    margin-top: 12px;
  }

  input[type=checkbox]:checked~.menu {
    display: block;
  }

  .hamburger {
    display: block;
  }

  .dropdown {
    left: 50%;
    top: 30px;
    transform: translateX(35%);
  }

  .dropdown li:hover {
    background-color: #4c9e9e;
  }
}
</style>