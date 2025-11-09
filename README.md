# MY-PORTFOLIO-WEB
<html lang="bn">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>SHAREA SOBUJ </title>
  <meta name="description" content="Portfolio of SHAREA SOBUJ — Web Developer / Designer" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&family=Montserrat:wght@600;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#0f1724;
      --card:#0b1220;
      --muted:#94a3b8;
      --accent:#00bcd4;
      --glass: rgba(255,255,255,0.04);
      --glass-2: rgba(255,255,255,0.02);
      color-scheme: dark;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background: linear-gradient(180deg,var(--bg),green 120%);
      color:#e6eef6;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.5;
      padding-bottom:60px;
    }

    /* container */
    .wrap{max-width:1100px;margin:36px auto;padding:28px;border-radius:14px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));box-shadow:0 8px 30px rgba(2,6,23,0.7);border:1px solid rgba(255,255,255,0.03)}
    header{display:flex;align-items:center;justify-content:space-between;gap:16px}
    .brand{display:flex;align-items:center;gap:12px}
    .logo{
      width:56px;height:56px;border-radius:12px;background:linear-gradient(135deg,var(--accent),#6be7ff);display:flex;align-items:center;justify-content:center;font-weight:700;color:#042123;font-family:Montserrat;font-size:18px;
      box-shadow:0 6px 18px rgba(0,188,212,0.12), inset 0 -8px 24px rgba(255,255,255,0.02);
    }
    .brand h1{margin:0;font-size:18px}
    .brand p{margin:0;font-size:12px;color:var(--muted)}

    nav ul{display:flex;gap:12px;list-style:none;padding:0;margin:0}
    nav a{color:var(--muted);text-decoration:none;padding:8px 12px;border-radius:10px;font-weight:600;font-size:14px}
    nav a:hover{color:#fff;background:var(--glass)}

    /* hero */
    .hero{display:grid;grid-template-columns:1fr 360px;gap:28px;margin-top:28px;align-items:center}
    .intro h2{margin:0;font-size:28px;font-family:Montserrat}
    .intro p{color:var(--muted);margin-top:8px}
    .cta{margin-top:18px;display:flex;gap:12px;flex-wrap:wrap}
    .btn{
      background:linear-gradient(90deg,var(--accent),#66e2ff);
      color:#012027;padding:10px 16px;border-radius:10px;border:0;font-weight:700;cursor:pointer;box-shadow:0 8px 30px rgba(0,188,212,0.08)
    }
    .btn.ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:var(--muted);font-weight:600}

    .profile-card{background:linear-gradient(180deg,var(--card),var(--glass));padding:20px;border-radius:12px;box-shadow:0 8px 30px rgba(2,6,23,0.6);text-align:center}
    .avatar{width:120px;height:120px;border-radius:14px;background:linear-gradient(180deg,#05232a,#08303b);display:inline-flex;align-items:center;justify-content:center;font-size:40px;font-weight:700;color:#9ff7ff;margin-bottom:12px}
    .small{font-size:13px;color:var(--muted);margin-top:6px}

    /* sections */
    section{margin-top:28px}
    .card{background:var(--glass-2);padding:18px;border-radius:12px;border:1px solid rgba(255,255,255,0.02)}
    .grid-2{display:grid;grid-template-columns:1fr 1fr;gap:18px}
    .skills-list{display:flex;flex-direction:column;gap:14px}
    .skill{display:flex;justify-content:space-between;align-items:center;gap:12px}
    .skill .bar{flex:1;height:10px;background:rgba(255,255,255,0.06);border-radius:999px;overflow:hidden;margin-left:12px}
    .skill .bar > i{display:block;height:100%;width:0;background:linear-gradient(90deg,var(--accent),#66e2ff);border-radius:999px;transition:width 1.1s ease}

    /* projects */
    .projects-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
    .project{
      padding:14px;border-radius:10px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border:1px solid rgba(255,255,255,0.03);cursor:pointer;min-height:120px;display:flex;flex-direction:column;justify-content:space-between;
    }
    .project h4{margin:0;font-size:16px}
    .project p{margin:8px 0 0 0;color:var(--muted);font-size:13px}

    /* experience / timeline */
    .timeline{display:flex;flex-direction:column;gap:12px}
    .entry{padding:12px;border-radius:10px;background:rgba(255,255,255,0.02);border:1px solid rgba(255,255,255,0.02)}
    .entry small{color:var(--muted)}

    /* contact */
    .contact-row{display:grid;grid-template-columns:1fr 1fr;gap:12px}
    .contact-card{display:flex;flex-direction:column;gap:8px}
    .input,textarea{background:transparent;border:1px solid rgba(255,255,255,0.04);padding:10px;border-radius:8px;color:#eaf6ff;outline:none}
    textarea{min-height:120px;resize:vertical}
    .muted{color:var(--muted);font-size:13px}

    footer{margin-top:28px;text-align:center;color:var(--muted);font-size:13px}

    /* modal */
    .modal-backdrop{position:fixed;inset:0;background:rgba(2,6,23,0.6);display:none;align-items:center;justify-content:center;padding:20px;z-index:1200}
    .modal{max-width:920px;width:100%;background:linear-gradient(180deg,#071021,#04101b);padding:20px;border-radius:12px;border:1px solid rgba(255,255,255,0.03)}
    .modal h3{margin:0}
    .close-btn{background:transparent;border:0;color:var(--muted);font-weight:700;cursor:pointer}

    /* responsive */
    @media (max-width:980px){
      .hero{grid-template-columns:1fr; text-align:center}
      .projects-grid{grid-template-columns:repeat(2,1fr)}
      .contact-row{grid-template-columns:1fr}
      nav ul{display:none}
    }
    @media (max-width:600px){
      .projects-grid{grid-template-columns:1fr}
      .wrap{margin:14px;padding:18px}
      .avatar{width:96px;height:96px;font-size:32px}
    }

    /* subtle animations */
    .fadeUp{opacity:0;transform:translateY(10px);transition:all 600ms ease}
    .in-view{opacity:1;transform:none}
  </style>
</head>
<body>
  <div class="wrap" id="top">
    <header>
      <div class="brand">
        <div class="logo">SS</div>
        <div>
          <h1>SHAREA SOBUJ</h1>
          <p>Web Developer • Frontend & Small Backend</p>
        </div>
      </div>

      <nav aria-label="Primary">
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#skills">Skills</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </header>

    <section class="hero">
      <div class="intro">
        <h2>Hello 👋, আমি <span style="color:var(--accent)">SHAREA SOBUJ</span></h2>
        <p class="muted">আমি ওয়েব ডেভেলপার — HTML, CSS, JavaScript দিয়ে সুন্দর ও রেস্পন্সিভ ওয়েবসাইট বানাই। এখানে আমার কাজ, দক্ষতা ও যোগাযোগর তথ্য দেখতে পাবেন।</p>
        <div class="cta">
          <button class="btn" onclick="downloadResume()">Download Resume</button>
          <a class="btn ghost" href="mailto:shareasobuj9829@gmail.com?subject=Hello%20Sharea%20Sobuj&body=Hi%20Sharea%2C%0A%0AI%20saw%20your%20portfolio%20and%20would%20like%20to%20connect.">Email: shareasobuj9829@gmail.com</a>
        </div>

        <div style="margin-top:18px" class="card fadeUp">
          <strong>Short bio</strong>
          <p class="muted" style="margin:8px 0 0 0">Frontend development, small-scale backend logic, localStorage apps, interactive UI and creative responsive layouts.</p>
        </div>
      </div>

      <aside class="profile-card fadeUp">
        <div class="avatar">SS</div>
        <div style="font-weight:700;font-size:16px">SHAREA SOBUJ</div>
        <div class="small">Web Developer</div>
        <div class="small" style="margin-top:10px">📧 shareasobuj9829@gmail.com</div>
        <div style="margin-top:12px">
          <a class="btn" href="#contact" style="display:inline-block">Contact Me</a>
        </div>
      </aside>
    </section>

    <section id="about" class="fadeUp">
      <div class="card">
        <h3>About Me</h3>
        <p class="muted">আমি ওয়েব ডেভেলপমেন্টে আগ্রহী — সুন্দর ইউআই, জাভাস্ক্রিপ্ট-ভিত্তিক ইন্টারঅ্যাকশন, এবং লোকাল-ডেটা ম্যানেজমেন্ট (localStorage) নিয়ে কাজ করি। আমার লক্ষ্য — সহজ, দ্রুত ও প্রফেশনাল ওয়েব প্রোডাক্ট তৈরি করা।</p>
      </div>
    </section>

    <section id="skills" class="fadeUp">
      <div class="grid-2">
        <div class="card">
          <h3>Skills</h3>
          <div class="skills-list">
            <div class="skill">
              <div style="min-width:110px">HTML / CSS</div>
              <div class="bar"><i data-width="95%"></i></div>
            </div>
            <div class="skill">
              <div style="min-width:110px">JavaScript</div>
              <div class="bar"><i data-width="88%"></i></div>
            </div>
            <div class="skill">
              <div style="min-width:110px">Responsive Design</div>
              <div class="bar"><i data-width="92%"></i></div>
            </div>
            <div class="skill">
              <div style="min-width:110px">LocalStorage Apps</div>
              <div class="bar"><i data-width="85%"></i></div>
            </div>
            <div class="skill">
              <div style="min-width:110px">Basic Backend (Node/Flask)</div>
              <div class="bar"><i data-width="60%"></i></div>
            </div>
          </div>
        </div>

        <div class="card">
          <h3>Experience & Education</h3>
          <div class="timeline">
            <div class="entry">
              <strong>Freelance Web Projects</strong>
              <div class="muted">2022 — Present</div>
              <small class="muted">Frontend projects, small web apps, landing pages.</small>
            </div>
            <div class="entry">
              <strong>Professional Learning</strong>
              <div class="muted">Online Courses & Self-study</div>
              <small class="muted">HTML/CSS/JS, UI/UX basics, small backend concepts.</small>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="projects" class="fadeUp">
      <h3>Selected Projects</h3>
      <div class="projects-grid" style="margin-top:12px">
        <div class="project" data-title="Project — Online Shop (Mock)" data-desc="একটি সাধারণ অনলাইন শপ প্রোটোটাইপ — প্রোডাক্ট লিস্ট, কার্ট, লোকালস্টোরেজ সেভ।" onclick="openModal(this)">
          <div>
            <h4>Online Shop (Mock)</h4>
            <p class="muted">LocalStorage-driven cart & product listing</p>
          </div>
          <div class="muted">HTML • JS • CSS</div>
        </div>

        <div class="project" data-title="Project — Portfolio Template" data-desc="এই পোর্টফোলিও টেমপ্লেটটি আপনার জন্য তৈরি: সব এক ফাইলে।" onclick="openModal(this)">
          <div>
            <h4>Portfolio Template</h4>
            <p class="muted">Single-file portfolio website</p>
          </div>
          <div class="muted">HTML • CSS</div>
        </div>

        <div class="project" data-title="Project — Task Manager" data-desc="স্ট্যান্ডঅ্যাক ফোন বা ব্রাউজারে কাজ করার জন্য টাস্ক ম্যানেজার, localStorage বেসড।" onclick="openModal(this)">
          <div>
            <h4>Task Manager</h4>
            <p class="muted">Tasks with add/edit/delete & local save</p>
          </div>
          <div class="muted">JS • localStorage</div>
        </div>

        <div class="project" data-title="Project — YouTube Style" data-desc="ভিডিও-লিস্টিং পেজ, কাস্টম প্লেয়ার UI (ডেমো)" onclick="openModal(this)">
          <div>
            <h4>Video Listing</h4>
            <p class="muted">Custom UI, responsive layout</p>
          </div>
          <div class="muted">HTML • CSS</div>
        </div>

        <div class="project" data-title="Project — Forms & CSV Export" data-desc="ফর্ম ডেটা সংগ্রহ করে CSV হিসেবে ডাউনলোড করার ডেমো" onclick="openModal(this)">
          <div>
            <h4>Form → CSV</h4>
            <p class="muted">Form save & CSV export</p>
          </div>
          <div class="muted">JS • CSV</div>
        </div>

        <div class="project" data-title="Project — Small Chat UI" data-desc="লোকাল-চ্যাট-স্টাইল UI (রিয়েল-টাইম নয়), UI প্রোটোটাইপ" onclick="openModal(this)">
          <div>
            <h4>Chat UI (Mock)</h4>
            <p class="muted">Messenger-style interface (UI only)</p>
          </div>
          <div class="muted">HTML • CSS</div>
        </div>
      </div>
    </section>

    <section id="contact" class="fadeUp">
      <h3>Contact</h3>
      <div class="card" style="margin-top:12px">
        <div class="contact-row">
          <div class="contact-card">
            <label class="muted">Email</label>
            <input class="input" type="email" id="c-email" value="shareasobuj9829@gmail.com" readonly>
            <label class="muted" style="margin-top:8px">Phone (optional)</label>
            <input class="input" type="text" id="c-phone" placeholder="01XXXXXXXXX">
            <p class="muted" style="margin-top:8px">অথবা সরাসরি মেইল করতে চাইলে নিচের বাটনে ক্লিক করুন।</p>
            <div style="margin-top:10px">
              <a class="btn" href="mailto:shareasobuj9829@gmail.com?subject=Contact%20from%20Portfolio" target="_blank">Send Email</a>
            </div>
          </div>

          <div>
            <label class="muted">Message</label>
            <textarea id="c-message" placeholder="আপনার বার্তা লিখুন..."></textarea>
            <div style="margin-top:8px;display:flex;gap:8px">
              <button class="btn" onclick="sendMail()">Send via Email</button>
              <button class="btn ghost" onclick="saveMessage()">Save Locally</button>
            </div>
            <p class="muted" style="margin-top:8px">Saved messages ডিভাইস-কম্পিউটারে localStorage এ সেভ হবে — আপনি চাইলে CSV হিসেবে এক্সপোর্ট করতে পারেন।</p>
          </div>
        </div>
      </div>
    </section>

    <footer>
      © <span id="year"></span> SHAREA SOBUJ — Built with ❤️ · <a href="#top" style="color:var(--muted);text-decoration:none">Back to top</a>
    </footer>
  </div>

  <!-- modal -->
  <div class="modal-backdrop" id="modal">
    <div class="modal" role="dialog" aria-modal="true" aria-labelledby="modal-title">
      <div style="display:flex;justify-content:space-between;align-items:center;gap:12px">
        <h3 id="modal-title">Project Title</h3>
        <button class="close-btn" onclick="closeModal()">Close ✕</button>
      </div>
      <p id="modal-desc" class="muted" style="margin-top:8px">Project description...</p>
      <div style="margin-top:14px;display:flex;gap:8px">
        <a class="btn" href="#" id="modal-live" target="_blank">Live Demo</a>
        <button class="btn ghost" onclick="copyProject()">Copy Info</button>
      </div>
    </div>
  </div>

  <script>
    // initial setup
    document.getElementById('year').textContent = new Date().getFullYear();

    // reveal on scroll
    const fades = document.querySelectorAll('.fadeUp');
    const io = new IntersectionObserver(entries=>{
      entries.forEach(e=>{
        if(e.isIntersecting) e.target.classList.add('in-view');
      });
    }, {threshold:0.12});
    fades.forEach(el=>io.observe(el));

    // animate skill bars
    window.addEventListener('load', ()=>{
      document.querySelectorAll('.skill .bar i').forEach((el,i)=>{
        const w = el.getAttribute('data-width') || '70%';
        setTimeout(()=> el.style.width = w, 300 + i*120);
      });
    });

    // projects modal
    function openModal(card){
      const title = card.getAttribute('data-title') || 'Project';
      const desc = card.getAttribute('data-desc') || '';
      document.getElementById('modal-title').textContent = title;
      document.getElementById('modal-desc').textContent = desc;
      document.getElementById('modal-live').setAttribute('href', '#');
      document.getElementById('modal').style.display = 'flex';
    }
    function closeModal(){ document.getElementById('modal').style.display = 'none'; }
    function copyProject(){
      const text = document.getElementById('modal-title').textContent + "\\n\\n" + document.getElementById('modal-desc').textContent;
      navigator.clipboard?.writeText(text).then(()=> alert('Project info copied to clipboard.'));
    }

    // contact: send mail via mailto
    function sendMail(){
      const email = encodeURIComponent(document.getElementById('c-email').value || 'shareasobuj9829@gmail.com');
      const message = encodeURIComponent(document.getElementById('c-message').value || '');
      const phone = encodeURIComponent(document.getElementById('c-phone').value || '');
      const subject = encodeURIComponent('Contact from Portfolio');
      const body = encodeURIComponent('Phone: ' + phone + '\\n\\nMessage:\\n' + decodeURIComponent(message));
      // open mail client
      const mailto = `mailto:${email}?subject=${subject}&body=${body}`;
      window.location.href = mailto;
    }

    // save message locally (localStorage)
    function saveMessage(){
      const msg = document.getElementById('c-message').value.trim();
      if(!msg){ alert('Message লিখুন আগে।'); return; }
      const list = JSON.parse(localStorage.getItem('ss_messages')||'[]');
      list.push({email: document.getElementById('c-email').value, phone: document.getElementById('c-phone').value, message: msg, at: new Date().toISOString()});
      localStorage.setItem('ss_messages', JSON.stringify(list));
      alert('Message saved locally। ডেটা localStorage এ সেভ হয়েছে।');
      document.getElementById('c-message').value = '';
    }

    // quick resume download (generates simple text resume as .txt)
    function downloadResume(){
      const content = [
        'SHAREA SOBUJ',
        'Email: shareasobuj9829@gmail.com',
        '',
        'Profile:',
        'Web Developer — Frontend & small backend tasks. Skilled in HTML, CSS, JavaScript, responsive design, and localStorage-based apps.',
        '',
        'Skills: HTML, CSS, JavaScript, Responsive Design, localStorage, simple backend (Node/Flask basics)',
        '',
        'Projects: Online Shop mock, Portfolio template, Task Manager, Video listing UI, Form→CSV demo, Chat UI (mock)',
        '',
        'Contact: shareasobuj9829@gmail.com'
      ].join('\\n');

      // create blob and download
      const blob = new Blob([content], {type:'text/plain;charset=utf-8'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url;
      a.download = 'SHAREA_SOBUJ_Resume.txt';
      document.body.appendChild(a);
      a.click();
      a.remove();
      URL.revokeObjectURL(url);
    }

    // smooth scroll for internal links
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click', e=>{
        const target = document.querySelector(a.getAttribute('href'));
        if(target){ e.preventDefault(); target.scrollIntoView({behavior:'smooth',block:'start'}); }
      });
    });

    // keyboard close modal
    document.addEventListener('keydown', (e)=>{
      if(e.key === 'Escape') closeModal();
    });

    // small helper: export saved messages as CSV
    // (user can open Console and run exportSavedMessages() or we can attach below)
    function exportSavedMessagesCSV(){
      const list = JSON.parse(localStorage.getItem('ss_messages')||'[]');
      if(!list.length){ alert('No saved messages found in localStorage.'); return; }
      const csv = ['email,phone,message,at'].concat(list.map(r=> {
        // escape quotes
        return [r.email, r.phone, '"'+(r.message||'').replace(/"/g,'""')+'"', r.at].join(',');
      })).join('\\n');
      const blob = new Blob([csv], {type:'text/csv;charset=utf-8'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url; a.download = 'ss_messages.csv'; document.body.appendChild(a); a.click(); a.remove(); URL.revokeObjectURL(url);
    }
    // expose to global for quick use in console if needed
    window.exportSavedMessagesCSV = exportSavedMessagesCSV;

  </script>

