

```javascript

const map = L.map("map").setView([0, 0], 1);

L.tileLayer("http://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
attribution:
'&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a>',
}).addTo(map);

const svgIcon = L.divIcon({
html: `
<svg
width="24"
height="40"
viewBox="0 0 100 100"
version="1.1"
preserveAspectRatio="none"
xmlns="http://www.w3.org/2000/svg">
<path d="M0 0 L50 100 L100 0 Z" fill="#7A8BE7"></path>
</svg>`,
className: "svg-icon",
iconSize: [24, 40],
iconAnchor: [12, 40],
});

L.marker([0, 0], { icon: svgIcon }).addTo(map);
```

```css
/* styles.css */
.svg-icon path {
fill: crimson;
}

.green path {

fill: darkgreen;

}

.blue path {

fill: navy;

}

.golden path {

fill: gold;

}
```

```javascript
/**  new markers and their references. **/
const greenMarker = L.marker([-50, 0], { icon: svgIcon }).addTo(map);
const blueMarker = L.marker([50, 50], { icon: svgIcon }).addTo(map);
const goldenMarker = L.marker([50, -50], { icon: svgIcon }).addTo(map);

/** corresponding CSS classes to the icon of each marker **/
greenMarker._icon.classList.add("green");
blueMarker._icon.classList.add("blue");
goldenMarker._icon.classList.add("golden");
```

