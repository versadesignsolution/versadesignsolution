## Hi there 👋

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>VERSA DESIGN SOLUTIONS — Worker Check‑In</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet"> 

   <!-- optional nav/logo in top-left -->

  <style>
    :root{
      --bg1:#0f172a; /* midnight */
      --bg2:#097e7e; /* teal */
      --card: rgba(255,255,255,0.06);
      --glass: rgba(255,255,255,0.08);
      --accent: #010a07;
      --muted: rgba(197, 148, 14, 0.75);
    }
    *{box-sizing:border-box}
    body{font-family:Inter,system-ui,Arial; margin:0; min-height:100vh; color:rgb(255, 4, 4);
      background: radial-gradient(1200px 600px at 10% 20%, rgba(3, 250, 250, 0.12), transparent),
                  linear-gradient(180deg,var(--bg1),#006aff 60%);
      display:flex; align-items:center; justify-content:center; padding:32px;
    }

    .wrap{width:100%; max-width:980px; background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); border-radius:14px; padding:28px; box-shadow:0 10px 30px rgba(2,6,23,0.6); backdrop-filter: blur(6px);}

    header{display:flex; align-items:center; gap:18px}
    .logo{width:72px; height:72px; border-radius:12px; display:grid; place-items:center; font-weight:700; font-size:28px; color:var(--bg1); background:linear-gradient(135deg,#34d399,#06b6d4);}
    h1{margin:0; font-size:20px}
    p.lead{margin:4px 0 0 0; color:var(--muted); font-size:13px}

    .grid{display:grid; grid-template-columns: 1fr 420px; gap:20px; margin-top:18px}

    .panel{background:var(--card); padding:18px; border-radius:12px}

    .check{display:flex; gap:12px; align-items:center}
    .check input[type=text]{flex:1; padding:12px 14px; border-radius:10px; border:1px solid rgba(255,255,255,0.05); background:transparent; color:inherit; font-size:15px}
    .check button{padding:11px 14px; border-radius:10px; border:0; background:linear-gradient(90deg,#06b6d4,#10b981); color:#022; font-weight:600; cursor:pointer}
    .small{font-size:13px; color:var(--muted)}

    table{width:100%; border-collapse:collapse; margin-top:12px}
    th,td{padding:10px 8px; text-align:left; font-size:14px}
    th{opacity:0.8; font-size:13px; color:var(--muted)}
    tbody tr{border-top:1px solid rgba(255,255,255,0.03)}

    .controls{display:flex; gap:10px; margin-top:12px}
    .btn{padding:9px 12px; border-radius:10px; border:1px solid rgba(255,255,255,0.06); background:transparent; color:inherit; cursor:pointer}
    .btn.primary{background:linear-gradient(90deg,#782f02,#10b981); color:#022; border:0}

    footer{margin-top:14px; display:flex; justify-content:space-between; align-items:center}

    @media (max-width:880px){
      .grid{grid-template-columns:1fr;}
    }
  </style>
</head>
   <!-- HERO / header with background image -->
  <header class="hero" role="banner">
    <div class="container">
      <!-- left: company logo + name (white on top of image) -->
     
      <a class="logo" href="#">
       
        <img src="C:\Users\COBBY\Desktop\PSD\3832eec1-a2b7-4aa6-9de7-94d1e8d4549a copy.png" alt="Company logo"> 
    
        <span>Versa Design Solutions</span>
      </a>
      <!--move-->
       <style>
    .moving-text {
      position: top;
      white-space: nowrap;
      overflow: hidden;
      background: #7903cd;
      color: #ffffff;
      font-size: 30px;
      padding: 10px;
    }
    .moving-text span {
      display: inline-block;
      position: top;
      animation: moveText 15s linear infinite;
    }
    @keyframes moveText {
      0% { transform: translateX(100%); }
      100% { transform: translateX(-100%); }
    }
  </style>

  <div class="moving-text">
    <right>
    <span>Welcome to Versa Design Solutions —   WORKERS TIME SITE FOR EVERY DAY</span>
    </right>
  </div>

<body style="background-image: url(https://th.bing.com/th/id/OIP.u8Etwgm1ZHtL8xvmnnrI9gHaQC?&rs=1&pid=ImgDetMain&o=7&rm=3)">
  <div class="wrap">
    <header>
      <div class="logo">V</div>
      <div>
        <h1>VERSA DESIGN SOLUTIONS</h1>
        <p class="lead">CEO: ANANE ELVIS (POLITE) — Worker Check‑In • Instant timestamping</p>
      </div>
      <div style="margin-left:auto; text-align:right; color:var(--muted); font-size:13px">
        <div id="liveClock">Local time: --</div>
        <div style="font-size:11px; opacity:0.8">Timezone: Africa/Accra</div>
      </div>
    </header>

    <div class="grid">
      <div class="panel">
        <h3 style="margin:0 0 8px 0">Worker Check‑In</h3>
        <div class="small">Type your name and press <strong>Check In</strong>. The time and date are recorded immediately.</div>

        <div style="margin-top:12px" class="check">
          <input id="nameInput" type="text" placeholder="Type your full name here" autocomplete="off" />
          <button id="checkBtn">Check In</button>
        </div>

        <div class="controls">
          <button id="exportBtn" class="btn">Export CSV</button>
          <button id="clearBtn" class="btn">Clear All</button>
          <div style="margin-left:auto; font-size:13px; color:var(--muted); align-self:center">Entries: <span id="count">0</span></div>
        </div>

        <table aria-live="polite">
          <thead>
            <tr><th>#</th><th>Name</th><th>Time &amp; Date</th></tr>
          </thead>
          <tbody id="logBody">
          </tbody>
        </table>
      </div>

      <div class="panel">
        <h3 style="margin:0 0 8px 0">Session / Info</h3>
        <p class="small">This simple web sheet stores check‑ins locally on the device using your browser's storage. It's ideal for quick attendance or visitor sign‑in. If you need centralized logging (so all workers on different devices write to the same list), I can provide a small server example.</p>

        <h4 style="margin-top:12px">Recent check‑ins</h4>
        <div id="recentList" style="margin-top:8px"></div>

        <hr style="border:none; height:1px; background:rgba(255,255,255,0.03); margin:14px 0" />
        <div style="font-size:13px; color:var(--muted)">Company: <strong>VERSA DESIGN SOLUTIONS</strong><br/>CEO: <strong>ANANE ELVIS (POLITE)</strong></div>
      </div>

    </div>

    <footer>
      <div style="font-size:12px; color:var(--muted)">Built for quick check‑ins • Local storage mode</div>
      <div style="font-size:12px; color:var(--muted)">Designed by Versa Design Solutions</div>
    </footer>
  </div>

  <script>
    // Key for localStorage
    const STORAGE_KEY = 'versa_checkins_v1';

    const nameInput = document.getElementById('nameInput');
    const checkBtn = document.getElementById('checkBtn');
    const logBody = document.getElementById('logBody');
    const countEl = document.getElementById('count');
    const exportBtn = document.getElementById('exportBtn');
    const clearBtn = document.getElementById('clearBtn');
    const recentList = document.getElementById('recentList');
    const liveClock = document.getElementById('liveClock');

    // Load saved entries
    let entries = JSON.parse(localStorage.getItem(STORAGE_KEY) || '[]');

    function formatDate(d){
      // Use Africa/Accra timezone explicitly
      try{
        return new Intl.DateTimeFormat('en-GB', { dateStyle:'medium', timeStyle:'medium', timeZone:'Africa/Accra' }).format(d);
      }catch(e){
        return d.toLocaleString();
      }
    }

    function render(){
      logBody.innerHTML='';
      entries.slice().reverse().forEach((e, idx)=>{
        const tr = document.createElement('tr');
        const iCell = document.createElement('td');
        iCell.textContent = entries.length - idx;
        const nameCell = document.createElement('td');
        nameCell.textContent = e.name;
        const timeCell = document.createElement('td');
        timeCell.textContent = e.friendly;
        tr.appendChild(iCell);
        tr.appendChild(nameCell);
        tr.appendChild(timeCell);
        logBody.appendChild(tr);
      });
      countEl.textContent = entries.length;

      // recent
      recentList.innerHTML = '';
      entries.slice(-5).reverse().forEach(e=>{
        const d = document.createElement('div');
        d.style.padding='8px 6px';
        d.style.borderRadius='8px';
        d.style.marginBottom='6px';
        d.style.background='linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01))';
        d.textContent = e.name + ' — ' + e.friendly;
        recentList.appendChild(d);
      });

      // Save
      localStorage.setItem(STORAGE_KEY, JSON.stringify(entries));
    }

    function nowInAccra(){
      // create date then format accordingly
      return new Date();
    }

    checkBtn.addEventListener('click', ()=>{
      const name = nameInput.value.trim();
      if(!name){
        nameInput.focus();
        return alert('Please type your name before checking in.');
      }
      const d = nowInAccra();
      const friendly = formatDate(d);
      entries.push({name, ts: d.toISOString(), friendly});
      render();
      nameInput.value='';
      nameInput.focus();
    });

    nameInput.addEventListener('keydown', (e)=>{
      if(e.key === 'Enter') checkBtn.click();
    });

    exportBtn.addEventListener('click', ()=>{
      if(entries.length===0) return alert('No entries to export.');
      // CSV
      const header = ['No','Name','Timestamp'];
      const rows = entries.map((r,i)=>[i+1, '"'+r.name.replace(/"/g,'""')+'"', r.ts]);
      const csv = [header.join(','), ...rows.map(r=>r.join(','))].join('\n');
      const blob = new Blob([csv], {type:'text/csv;charset=utf-8;'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url; a.download = 'versa_checkins.csv'; document.body.appendChild(a); a.click(); a.remove();
      URL.revokeObjectURL(url);
    });

    clearBtn.addEventListener('click', ()=>{
      if(!confirm('Clear all stored entries? This cannot be undone.')) return;
      entries = [];
      render();
    });

    // Live clock
    function tick(){
      try{
        const d = new Date();
        liveClock.textContent = 'Local time: ' + new Intl.DateTimeFormat('en-GB', {dateStyle:'medium', timeStyle:'medium', timeZone:'Africa/Accra'}).format(d);
      }catch(e){
        liveClock.textContent = 'Local time: ' + new Date().toLocaleString();
      }
    }
    setInterval(tick, 1000);
    tick();

    // Initial render
    render();
  </script>

</body>
</html>
