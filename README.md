# amazon-website
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Lokendra Jimidar — Everything Store</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
/* ─── RESET & BASE ─── */
*, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }
body { font-family: 'Inter', Arial, sans-serif; font-size: 14px; background: #EAEDED; color: #0F1111; }
a { text-decoration: none; color: inherit; }
ul { list-style: none; }
button { font-family: inherit; cursor: pointer; border: none; }
img { max-width: 100%; }

/* ─── COLOURS ─── */
:root {
  --orange:     #FF9900;
  --orange-dk:  #E47911;
  --orange-lt:  #FFF4E0;
  --navy:       #131921;
  --navy2:      #232F3E;
  --navy3:      #37475A;
  --teal:       #007185;
  --teal-dk:    #005E6E;
  --green:      #067D62;
  --red:        #CC0C39;
  --yellow:     #FFD700;
  --bg:         #EAEDED;
  --white:      #FFFFFF;
  --border:     #DDD;
  --text:       #0F1111;
  --muted:      #565959;
  --shadow:     0 2px 8px rgba(0,0,0,0.12);
}

/* ─── NAV TOP BAR ─── */
.nav-top {
  background: var(--navy);
  color: #fff;
  display: flex;
  align-items: stretch;
  height: 60px;
  padding: 0 8px;
  gap: 2px;
  position: sticky;
  top: 0;
  z-index: 200;
}

.nav-logo {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 4px 10px;
  border: 2px solid transparent;
  border-radius: 3px;
  cursor: pointer;
  line-height: 1;
  transition: border-color 0.15s;
  white-space: nowrap;
}
.nav-logo:hover { border-color: #fff; }
.nav-logo .brand-top { font-size: 10px; color: #ccc; }
.nav-logo .brand-main {
  font-size: 20px;
  font-weight: 700;
  color: var(--orange);
  letter-spacing: -0.5px;
}
.nav-logo .brand-dot { color: var(--orange); }

.nav-deliver {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 4px 10px;
  border: 2px solid transparent;
  border-radius: 3px;
  cursor: pointer;
  font-size: 12px;
  color: #ccc;
  white-space: nowrap;
}
.nav-deliver:hover { border-color: #fff; }
.nav-deliver span { font-size: 13px; font-weight: 700; color: #fff; }

.nav-search {
  flex: 1;
  display: flex;
  align-items: center;
  height: 40px;
  margin: auto 8px;
  border-radius: 4px;
  overflow: hidden;
  background: #fff;
  border: 2px solid var(--orange);
}

.search-cat {
  background: #F3F3F3;
  border: none;
  border-right: 1px solid #ccc;
  padding: 0 8px;
  height: 100%;
  font-size: 12px;
  color: #555;
  cursor: pointer;
  min-width: 80px;
  outline: none;
}

.search-input {
  flex: 1;
  border: none;
  padding: 0 12px;
  height: 100%;
  font-size: 15px;
  outline: none;
  color: #0F1111;
  background: #fff;
}

.search-btn {
  background: var(--orange);
  border: none;
  padding: 0 14px;
  height: 100%;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: background 0.15s;
}
.search-btn:hover { background: var(--orange-dk); }
.search-btn svg { width: 20px; height: 20px; fill: #333; }

.nav-lang {
  display: flex;
  align-items: center;
  gap: 4px;
  padding: 0 8px;
  border: 2px solid transparent;
  border-radius: 3px;
  cursor: pointer;
  font-size: 13px;
  white-space: nowrap;
}
.nav-lang:hover { border-color: #fff; }
.nav-flag { font-size: 16px; }

.nav-account {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 4px 10px;
  border: 2px solid transparent;
  border-radius: 3px;
  cursor: pointer;
  white-space: nowrap;
}
