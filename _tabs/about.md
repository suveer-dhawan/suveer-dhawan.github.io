---
# the default layout is 'page'
icon: fas fa-info-circle
order: 4
---

I am a Data Scientist and AI Engineer bridging the gap between quantitative economics and scalable machine learning. Growing up surrounded by a family home library of nearly 10,000 books instilled a deep appreciation for rigorous research, diverse narratives, and finding the underlying patterns in complex information. 

Today, I focus on architecting production-ready AI microservices, leveraging my foundation in game theory and econometrics to solve structural organizational bottlenecks.

---

## 🗺️ The Global Journey
My academic and professional career has been defined by international mobility, adapting to new markets, and learning across distinct cultures. Hover over the markers below to explore the timeline.

<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<div id="journey-map" style="height: 450px; border-radius: 12px; margin: 30px 0; border: 2px solid var(--link-color); z-index: 1;"></div>
<script>
var map = L.map('journey-map', { scrollWheelZoom: false }).setView([25.0, 70.0], 2);
L.tileLayer('https://{s}.basemaps.cartocdn.com/dark_all/{z}/{x}/{y}{r}.png', { attribution: '&copy; OpenStreetMap &copy; CARTO', subdomains: 'abcd', maxZoom: 19 }).addTo(map);
var journeyPoints = [
  { coords: [24.4539, 54.3773], title: "📍 Abu Dhabi, UAE", desc: "<b>NYU Abu Dhabi</b><br>B.A. Economics (Honours)<br>Full Scholarship (3% acceptance) & UAE Golden Visa." },
  { coords: [40.7128, -74.0060], title: "📍 New York, USA", desc: "<b>NYU Study Away</b><br>Applied Econometrics<br>Catching Nets games at Barclays." },
  { coords: [43.7696, 11.2558], title: "📍 Florence, Italy", desc: "<b>NYU J-Term</b><br>Mediterranean Foodways<br>Intersection of history, culture, and Italian cuisine." },
  { coords: [25.2048, 55.2708], title: "📍 Dubai, UAE", desc: "<b>AlphaSights</b><br>Project Lead<br>Managed 70+ projects for tier-1 consultants (Bain, BCG)." },
  { coords: [-37.8136, 144.9631], title: "📍 Melbourne, Australia", desc: "<b>Monash University</b><br>Master of Data Science<br>Deep Neuron & Graduate Research." },
  { coords: [-31.9505, 115.8605], title: "📍 Perth, Australia", desc: "<b>Woodside Energy</b><br>Data & AI Intern<br>Architected 5 production-ready RAG AI workflows." },
  { coords: [-33.8688, 151.2093], title: "📍 Sydney, Australia", desc: "<b>Top 100 Future Leaders</b><br>Nationally recognized for technical and leadership potential." }
];
journeyPoints.forEach(function(point) {
  var marker = L.marker(point.coords).addTo(map);
  marker.bindPopup('<div style="font-family: inherit; text-align: center;"><span style="color: #7b43a1; font-weight: bold; font-size: 1.1em;">' + point.title + '</span><br><div style="margin-top: 5px;">' + point.desc + '</div></div>', { closeButton: false, offset: L.point(0, -20) });
  marker.on('mouseover', function (e) { this.openPopup(); });
  marker.on('mouseout', function (e) { this.closePopup(); });
});
</script>