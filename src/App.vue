<template>
  <div id="app" style="max-width: 800px; margin: auto; padding: 1rem">
    <header style="text-align: center">
      <h1>Sheet Maker</h1>
      <p>Add Chords to Your Music</p>
    </header>
    <main>
      <section style="padding: 0 20px;display:flex;justify-content:space-around">
          <el-button type="primary">New Lyrics</el-button>
          <el-button type="primary">Load Previous</el-button>
      </section>
      <el-row style="margin: 20px auto">
        <el-col style="padding: 10px 20px" :lg="12" :xl="12" :md="12" :sm="12">
          <div>
            <div class="view">
              <div class="iframe" >
                <header>
                  <h3 style="text-align:center;margin:0;">Wish You Were Here</h3>
                </header>
                <p style="text-align:center;margin:1px;">Pink Floyd</p>
              </div>
            </div>
          </div>
        </el-col>
        <el-col style="padding: 10px 20px" :lg="12" :xl="12" :md="12">
          <div><span>Header:</span></div>
          <div class="d-flex" style="display: flex; margin-top: 20px">
            <label style="line-height: 40px; margin-right: 10px">Title</label>
            <el-input placeholder="Please input"></el-input>
            <el-color-picker></el-color-picker>
          </div>
          <div style="display: flex; justify-content: center; margin-top: 20px">
            <span>Add Sub Header</span>
          </div>
          <div style="margin-top: 20px"><span>Body:</span></div>
          <div class="d-flex" style="display: flex; margin-top: 20px">
            <label style="line-height: 40px; margin-right: 10px">Verse:</label>
            <el-input placeholder="Please input"></el-input>
            <el-color-picker></el-color-picker>
          </div>
        </el-col>
      </el-row>
    </main>
  </div>
</template>

<script>
export default {
  name: "app",
};
</script>

<style>
.view {
  line-height: 1.5;
  --main-400: #7f9cf5;
  --opener: url("data:image/svg+xml;charset=utf-8,%3Csvg xmlns='http://www.w3.org/2000/svg' stroke='%23fff' stroke-width='2' fill='none' stroke-linecap='round' stroke-linejoin='round' viewBox='0 0 24 24'%3E%3Cpath d='M3 12h18M3 6h18M3 18h18'/%3E%3C/svg%3E");
  --opener-active: url("data:image/svg+xml;charset=utf-8,%3Csvg xmlns='http://www.w3.org/2000/svg' stroke='%23fff' stroke-width='2' fill='none' stroke-linecap='round' stroke-linejoin='round' class='css-i6dzq1' viewBox='0 0 24 24'%3E%3Cpath d='M19 12H5m7 7l-7-7 7-7'/%3E%3C/svg%3E");
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Roboto", "Oxygen",
    "Ubuntu", "Cantarell", "Fira Sans", "Droid Sans", "Helvetica Neue",
    sans-serif;
  -webkit-font-smoothing: antialiased;
  --main-500: #667eea;
  --base-500: #718096;
  --base-200: #2d3748;
  --base-300: #4a5568;
  --base-400: #4a5568;
  --main-200: #4a5568;
  --main-100: #2d3648;
  --solid: #1a202c;
  --solid-900: #d1dcec;
  --sidebar-bg: #2d3648;
  --sidebar-color: #fff;
  --shadow: 0 10px 15px -3px #1a202d, 0 4px 6px -2px #303a54;
  --shadow-active: 0 0 0 2px currentColor, 0 10px 15px -3px rgba(0, 0, 0, 0.35),
    0 4px 6px -2px #4c525a;
  box-sizing: border-box;
  border-width: 0;
  border-style: solid;
  border-color: #e2e8f0;
  position: relative;
  height: 600px;
  background-color: var(--sidebar-bg);
  border-radius: 30px;
  border: 2px solid var(--base-300);
}
.view::before {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  content: "";
  bottom: 20px;
  border: 2px solid #cbd5e0;
  border: 2px solid var(--base-400);
  width: 40px;
  border-radius: 50%;
  height: 40px;
}
.view::after {
  top: 23px;
  width: 100px;
  height: 16px;
  border-radius: 40px;
  border: 2px solid #cbd5e0;
  border: 2px solid var(--base-400);
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  content: "";
}
.iframe {
  height: 480px;
  width: 100%;
  margin-right: 38px;
  margin: 50px auto;
  background-image: url("./assets/pinkfloyd.jpg");
  background-size: cover;
  background-color: white;
}
</style>
