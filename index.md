---
layout: article
title: Welcome 
---

<button id="theme-toggle" onclick="modeSwitcher()"></button>

const theme = localStorage.getItem('theme');
	if (theme === "dark") {
		document.documentElement.setAttribute('data-theme', 'dark');
	}


### Hi there! I am a third-year undergradauate student @ NYU studying data science and sociology.

My passions lie in human-computer interaction, critical disability studies and digital accessibility. I am currently pursuing independent research on the effects of digital health tracking as a form of surveillance against disabled populations. I am also a disabled cyborg, amateur biohacker, and avid bookworm. Check out what I am currently reading [here.](https://www.goodreads.com/user/show/46515398-paige-h)

> "Disabled People are the original lifehackers. Our lives are spent cultivating intuitive creaitivity, because we navigate a world that isn't built for our bodies." 
>
> --- Liz Jackson 

Just put more text here so it looks nice

### You can read more about me on my "About" page or contact me below!

- Linkedin
- Github

const userPrefers = getComputedStyle(document.documentElement).getPropertyValue('content');	

if (theme === "dark") {
	document.getElementById("theme-toggle").innerHTML = "Light Mode";
} else if (theme === "light") {
	document.getElementById("theme-toggle").innerHTML = "Dark Mode";
} else if  (userPrefers === "dark") {
	document.documentElement.setAttribute('data-theme', 'dark');
	window.localStorage.setItem('theme', 'dark');
	document.getElementById("theme-toggle").innerHTML = "Light Mode";
} else {
	document.documentElement.setAttribute('data-theme', 'light');
	window.localStorage.setItem('theme', 'light');
	document.getElementById("theme-toggle").innerHTML = "Dark Mode";
}

function modeSwitcher() {
	let currentMode = document.documentElement.getAttribute('data-theme');
	if (currentMode === "dark") {
		document.documentElement.setAttribute('data-theme', 'light');
		window.localStorage.setItem('theme', 'light');
		document.getElementById("theme-toggle").innerHTML = "Dark Mode";
	} else {
		document.documentElement.setAttribute('data-theme', 'dark');
		window.localStorage.setItem('theme', 'dark');
		document.getElementById("theme-toggle").innerHTML = "Light Mode";
	}
}
