<html lang="en">
h1{margin:0;font-size:18px;letter-spacing:0.2px}
p.bio{margin:16px 0 18px;font-size:15px;line-height:1.5;color:#dbeafe}
.actions{display:flex;gap:12px;align-items:center}
button{background:transparent;border:1px solid rgba(125,211,252,0.12);padding:8px 12px;border-radius:8px;color:var(--accent);cursor:pointer;font-weight:600}
button.secondary{color:var(--muted);border-color:rgba(148,163,184,0.06)}
.footer{margin-top:12px;font-size:13px;color:var(--muted)}
code{background:rgba(255,255,255,0.03);padding:4px 8px;border-radius:6px}
</style>
</head>
<body>
<article class="card" role="article">
<div class="meta">
<div class="avatar">GH</div>
<div>
<h1>GitHub Bio — 80 words</h1>
<div class="footer">Polished short bio for your profile README</div>
</div>
</div>


<p class="bio" id="bioText">I believe every line of code tells a story. From simple projects that taught me the basics to high-level projects that push my limits, my journey is one of growth, persistence, and hope. Each repository shows experiments, learning curves, and milestones shaping me as a developer. This is more than coding—it's building, breaking, and rebuilding with purpose. A journey of hope where every project moves me one step closer to my vision. I code to learn, to share and inspire.</p>


<div class="actions">
<button id="copyBtn">Copy bio</button>
<button class="secondary" id="downloadBtn">Download HTML</button>
</div>


<div class="footer">Tip: Paste this into your <code>README.md</code> or GitHub profile bio. Want a shorter variant or different color theme? Ask me!</div>
</article>


<script>
const copyBtn = document.getElementById('copyBtn');
const bioText = document.getElementById('bioText');
copyBtn.addEventListener('click', async () => {
try{
await navigator.clipboard.writeText(bioText.textContent.trim());
copyBtn.textContent = 'Copied!';
setTimeout(()=> copyBtn.textContent = 'Copy bio', 1600);
}catch(e){
alert('Copy failed — select the text and copy manually.');
}
});


const downloadBtn = document.getElementById('downloadBtn');
downloadBtn.addEventListener('click', ()=>{
const blob = new Blob([document.documentElement.outerHTML], {type: 'text/html'});
const url = URL.createObjectURL(blob);
const a = document.createElement('a');
a.href = url; a.download = 'github_bio.html';
document.body.appendChild(a); a.click(); a.remove(); URL.revokeObjectURL(url);
});
</script>
</body>
</html>
