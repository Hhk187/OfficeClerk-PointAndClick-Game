<nav class="navbar">
    <div class="nav-content">
    <a href="#landing" class="nav-left">About the Project</a>
    <div class="nav-right">
        <a href="#">Guide</a>
        <a href="#">Get some Prints</a>
    </div>
    </div>
</nav>

<style>
.navbar {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 63px;
  background-color: #FFDAB2;
  border-bottom: 2px solid black;
  z-index: 200;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 12px;
  transition: transform 0.6s ease-out, opacity 0.6s ease-in-out;
}

.navbar a,
.nav-left,
.nav-right a {
  font-size: clamp(8px, 1.2vw, 18px);
}
</style>
