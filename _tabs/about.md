---
# the default layout is 'page'
icon: fas fa-info-circle
order: 4
---

I am a Data Scientist and AI Engineer bridging the gap between quantitative economics and scalable machine learning. Growing up surrounded by a family home library of nearly 10,000 books instilled a deep appreciation for rigorous research, diverse narratives, and finding the underlying patterns in complex information. 

Today, I focus on architecting production-ready AI microservices, leveraging my foundation in game theory and econometrics to solve structural organizational bottlenecks.

---

## The Global Journey
My academic and professional trajectory has been defined by international mobility, adapting to new markets, and cross-cultural execution. Hover over the markers below to explore the timeline.

<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<div id="journey-map" style="height: 450px; border-radius: 12px; margin: 30px 0; border: 2px solid var(--link-color); z-index: 1;"></div>
<script>
var map = L.map('journey-map', { scrollWheelZoom: false }).setView([20.0, 80.0], 3);
L.tileLayer('https://{s}.basemaps.cartocdn.com/dark_all/{z}/{x}/{y}{r}.png', { attribution: '&copy; OpenStreetMap &copy; CARTO', subdomains: 'abcd', maxZoom: 19 }).addTo(map);
var violetIcon = new L.Icon({ iconUrl: 'https://raw.githubusercontent.com/pointhi/leaflet-color-markers/master/img/marker-icon-2x-violet.png', shadowUrl: 'https://cdnjs.cloudflare.com/ajax/libs/leaflet/0.7.7/images/marker-shadow.png', iconSize: [25, 41], iconAnchor: [12, 41], popupAnchor: [1, -34], shadowSize: [41, 41] });
var journeyPoints = [
  { coords: [28.6139, 77.2090], title: "Delhi, India", desc: "<b>Hometown</b><br>Born and raised<br>Formative years until 2019" },
  { coords: [24.4539, 54.3773], title: "Abu Dhabi, UAE", desc: "<b>NYU Abu Dhabi</b><br>B.A. Economics (Honours)<br>Full Scholarship & UAE Golden Visa" },
  { coords: [40.7128, -74.0060], title: "New York, USA", desc: "<b>NYU Study Away</b><br>Immersed in Applied Econometrics<br>Built quantitative research foundations" },
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
I focus on building end-to-end systems, moving from raw data extraction to robust, user-facing applications. 
* **Languages & Core:** Python, R, SQL, JavaScript (Node.js)
* **AI & Machine Learning:** PyTorch, LangChain, LlamaIndex, OpenAI/Gemini APIs, Hugging Face
* **Infrastructure & Data:** ChromaDB, Firebase, Pandas, Git, Google Colab Pro
* **Automation & Cloud:** Copilot Studio, Power Automate, n8n, Google Cloud (OAuth/APIs)

---

## Beyond the Code
I take a highly structured approach to life outside of work. When I am not fine-tuning models or analyzing enterprise workflows, I am usually tracking global markets and analyzing ETF compositions (like VGS and VDHG) to optimize personal finance strategies. 

Physical fitness is another core pillar; I treat the gym with the same focus as a deployment pipeline, consistently chasing progressive overload and vascularity. Most mornings start by hunting down the perfect iced long black or cold brew. 

I also enjoy exploring the creative intersections of technology. Most recently, this meant building a custom interactive "choose your own adventure" website for a Valentine's project, complete with Victorian settings, moors, haunted mansions, fog, and unreliable narrators. Ultimately, whether I am deploying local vector databases, managing index funds, or writing code, my drive remains the same: building systems that are functional, scalable, and structurally elegant.