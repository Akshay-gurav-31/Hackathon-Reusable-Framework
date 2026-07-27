# Assets Folder

Store your hackathon images, logos, judge headshots, and sponsor logos here.

## File Organization Strategy:
```text
assets/
├── logo.png             <-- Hackathon Header Logo
├── judges/
│   ├── judge1.jpg       <-- Judge photo 1
│   ├── judge2.jpg       <-- Judge photo 2
│   └── judge3.jpg       <-- Judge photo 3
├── mentors/
│   ├── mentor1.jpg      <-- Mentor photo 1
│   └── mentor2.jpg      <-- Mentor photo 2
└── sponsors/
    ├── sponsor1.png     <-- Sponsor logo 1
    └── sponsor2.png     <-- Sponsor logo 2
```

## How to reference in `hackathon.config.yml`:

```yaml
hackathon:
  name: "Your Hackathon Name"
  logo: "./assets/logo.png"

judges:
  - name: "Judge Name"
    photo: "./assets/judges/judge1.jpg"
    linkedin: "https://linkedin.com/in/username"

mentors:
  enabled: true
  list:
    - name: "Mentor Name"
      photo: "./assets/mentors/mentor1.jpg"
      contact: "https://linkedin.com/in/username"

sponsors:
  enabled: true
  list:
    - name: "Sponsor Name"
      logo: "./assets/sponsors/sponsor1.png"
      url: "https://sponsor-website.com"
```
