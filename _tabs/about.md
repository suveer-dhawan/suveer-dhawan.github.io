---
# the default layout is 'page'
icon: fas fa-info-circle
order: 1
title: About Me
---

I am a Data Scientist and AI Engineer bridging the gap between quantitative economics and scalable machine learning. Growing up surrounded by a family home library of nearly 10,000 books instilled a deep appreciation for rigorous research, diverse narratives, and finding the underlying patterns in complex information. 

Today, I focus on architecting production-ready AI microservices, leveraging my foundation in game theory and econometrics to solve structural organizational bottlenecks.

---

<style>
.cv-button {
  display: inline-flex;
  align-items: center;
  padding: 12px 24px;
  background-color: #57068c !important; /* Solid NYU Violet for visibility */
  color: #ffffff !important;
  border-radius: 8px;
  text-decoration: none !important;
  font-weight: bold;
  font-size: 1rem;
  transition: all 0.3s ease;
  border: 2px solid #57068c;
  margin: 20px 0;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.cv-button:hover {
  background-color: #7b43a1 !important; /* Slightly lighter purple on hover */
  border-color: #7b43a1;
  transform: translateY(-2px);
  box-shadow: 0 6px 15px rgba(87, 6, 140, 0.3);
  color: #ffffff !important;
}

.cv-icon { 
  margin-right: 10px;
  font-size: 1.2rem;
}
</style>

<a href="/assets/Suveer_Dhawan_CV.pdf" target="_blank" class="cv-button">
  <i class="fas fa-file-pdf cv-icon"></i> Download CV
</a>

---

## The Global Journey
My academic and professional trajectory has been defined by international mobility, adapting to new markets, and cross-cultural execution. Hover over the markers below to explore the timeline.

<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<div id="journey-map" style="height: 450px; border-radius: 12px; margin: 30px 0; border: 2px solid var(--link-color); z-index: 1;"></div>
<script>
var map = L.map('journey-map', { scrollWheelZoom: false }).setView([5.0, 100.0], 2);
L.tileLayer('https://{s}.basemaps.cartocdn.com/dark_all/{z}/{x}/{y}{r}.png', { attribution: '&copy; OpenStreetMap &copy; CARTO', subdomains: 'abcd', maxZoom: 19 }).addTo(map);
var violetIcon = new L.Icon({ iconUrl: 'https://raw.githubusercontent.com/pointhi/leaflet-color-markers/master/img/marker-icon-2x-violet.png', shadowUrl: 'https://cdnjs.cloudflare.com/ajax/libs/leaflet/0.7.7/images/marker-shadow.png', iconSize: [25, 41], iconAnchor: [12, 41], popupAnchor: [1, -34], shadowSize: [41, 41] });
var journeyPoints = [
  { coords: [28.6139, 77.2090], title: "Delhi, India", desc: "<b>Hometown</b><br>Born and raised<br>Home until 2019" },
  { coords: [24.4539, 54.3773], title: "Abu Dhabi, UAE", desc: "<b>NYU Abu Dhabi</b><br>B.A. Economics (Honours)<br>Full Scholarship & UAE Golden Visa" },
  { coords: [40.7128, -74.0060], title: "New York, USA", desc: "<b>NYU Study Away</b><br>Creative Coding + Finance<br>Evenings watching Nets at Barclays Center" },
  { coords: [43.7696, 11.2558], title: "Florence, Italy", desc: "<b>NYU J-Term</b><br>Studied Mediterranean Foodways<br>Explored historical cultural intersections" },
  { coords: [25.2048, 55.2708], title: "Dubai, UAE", desc: "<b>AlphaSights</b><br>Project Lead<br>Facilitated research for tier-1 strategy consultants" },
  { coords: [-37.8136, 144.9631], title: "Melbourne, Australia", desc: "<b>Monash University</b><br>Master of Data Science<br>Active in Deep Neuron & applied research" },
  { coords: [-31.9505, 115.8605], title: "Perth, Australia", desc: "<b>Woodside Energy</b><br>Data & AI Intern<br>Architected enterprise-grade RAG workflows" },
  { coords: [-33.8688, 151.2093], title: "Sydney, Australia", desc: "<b>Top 100 Future Leaders</b><br>Recognized for technical and leadership potential" }
];
journeyPoints.forEach(function(point) {
  var marker = L.marker(point.coords, {icon: violetIcon}).addTo(map);
  marker.bindPopup('<div style="font-family: inherit; text-align: center;"><span style="color: #7b43a1; font-weight: bold; font-size: 1.1em;">' + point.title + '</span><br><div style="margin-top: 5px;">' + point.desc + '</div></div>', { closeButton: false, offset: L.point(0, -20) });
  marker.on('mouseover', function (e) { this.openPopup(); });
  marker.on('mouseout', function (e) { this.closePopup(); });
});
</script>

---

## Technical Arsenal

<style>
.mac-terminal {
  background-color: #111111;
  border-radius: 8px;
  padding: 15px;
  font-family: 'Courier New', Courier, monospace;
  margin-bottom: 30px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.5);
  border: 1px solid #333;
}
.mac-header {
  display: flex;
  gap: 8px;
  margin-bottom: 15px;
}
.mac-btn {
  width: 12px;
  height: 12px;
  border-radius: 50%;
}
.close-btn { background-color: #ff5f56; }
.min-btn { background-color: #ffbd2e; }
.max-btn { background-color: #27c93f; }
.term-text { color: #e0e0e0; font-size: 0.95rem; line-height: 1.6; }
.term-prompt { color: #b28be6; font-weight: bold; } 
.term-command { color: #ffffff; }
.term-string { color: #a392b3; }
.term-key { color: #d1bdf7; }
</style>

<div class="mac-terminal">
  <div class="mac-header">
    <div class="mac-btn close-btn"></div>
    <div class="mac-btn min-btn"></div>
    <div class="mac-btn max-btn"></div>
  </div>
  <div class="term-text">
    <span class="term-prompt">suveer@macbook-pro:~$</span> <span class="term-command">cat stack.json</span><br><br>
    {<br>
    &nbsp;&nbsp;<span class="term-key">"Languages"</span>: <span class="term-string">["Python", "SQL", "R"]</span>,<br>
    &nbsp;&nbsp;<span class="term-key">"AI_and_ML"</span>: <span class="term-string">["PyTorch", "LangChain", "scikit-learn", "Deep Learning", "NLP", "RAG Architecture"]</span>,<br>
    &nbsp;&nbsp;<span class="term-key">"Data_and_Infra"</span>: <span class="term-string">["Pandas", "NumPy", "ChromaDB", "Docker", "Git", "Azure"]</span>,<br>
    &nbsp;&nbsp;<span class="term-key">"Automation_and_Tools"</span>: <span class="term-string">["n8n", "OpenAI API", "Ollama", "Power BI", "Power Automate", "Copilot Studio"]</span><br>
    }<br>
    <span class="term-prompt">suveer@macbook-pro:~$</span> <span class="term-command animate-pulse">_</span>
  </div>
</div>

---

---

## Beyond the Code
I take a highly structured approach to life outside of work. Physical fitness is a core pillar; I treat the gym with the same focus as a deployment pipeline, consistently chasing progressive overload. My mornings invariably start by hunting down the perfect iced long black or cold brew, and I actively track global markets and ETF compositions (like VGS and VDHG) to optimize personal finance strategies. 

When I am not fine-tuning models, you will likely find me agonizing over Tottenham Hotspur, or following Luka Dončić's magic across the Mavericks and now the Lakers. My weekly routine is soundtracked by a specific rotation of podcasts: staying sharp on the shifting AI landscape with *Hard Fork* and keeping up with the NBA via the *Hoop Collective*.

I also enjoy exploring the creative intersections of technology, which recently meant building a custom interactive "choose your own adventure" website for a Valentine's project. Finally, music is my constant runtime environment. My Spotify algorithm is a chaotic but perfect split between an absolute obsession with Lin-Manuel Miranda's *Hamilton* and the songwriting of Taylor Swift and Gracie Abrams. Ultimately, whether I am deploying local vector databases, managing index funds, or writing code, my drive remains the same: building systems that are functional, scalable, and structurally elegant.

<br>
<iframe style="border-radius:12px" src="https://open.spotify.com/embed/album/1kCHru7uhxBUdzkm4gzRQc?utm_source=generator&theme=0" width="100%" height="152" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>