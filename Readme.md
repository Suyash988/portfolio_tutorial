# Portfolio Website

A modern and responsive portfolio website showcasing projects, skills, and contact information.

## Features

- Smooth section transitions
- Responsive navigation bar
- Interactive project cards with hover effects
- Skills display with progress levels
- Timeline experience section
- Contact form with map integration
- Modern dark theme

## Technologies Used

- HTML5
- CSS3 (Flexbox, Grid, Transitions)
- JavaScript

## Sections

1. **Home**

   - Full-screen hero section with animated text
   - Decorative background image

2. **Projects**

   - Grid layout project showcase
   - Hoverable project cards with overlay effect
   - Live and Code buttons

3. **About**

   - Profile section with downloadable CV
   - Skills display with percentage indicators
   - Experience timeline

4. **Contact**
   - Responsive contact form
   - Integrated map
   - Form validation styling

## <a name="snippets">🕸️ Snippets</a>

<details>
<summary><code>Navbar CSS</code></summary>

```
.navbar{
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 9;
    background: #1a1a1a;
}

.link-group{
    list-style: none;
    display: flex;
}

.link a{
    color: #fff;
    opacity: 0.5;
    text-decoration: none;
    text-transform: capitalize;
    padding: 10px 30px;
    margin: 0 20px;
    line-height: 80px;
    transition: .5s;
    font-size: 20px;
}

.link a:hover, .link.active a{
    opacity: 1;
}
```

</details>
<details>
<summary><code>Hero Section CSS</code></summary>

```
.home-section{
    width: 100%;
    height: 100vh;
    padding: 0 150px;
    display: flex;
    align-items: center;
    /* position: relative; */
    position: fixed;
    top: 0;
    opacity: 0;
    transition: 1s;
}

.hero-heading{
    color: #fff;
    font-size: 120px;
    font-weight: 300;
}

.home-img{
    position: absolute;
    top: 0;
    right: 0;
    height: 100vh;
    width: 50%;
    object-fit: cover;
    opacity: 0.2;
}

.home-section.active,
.project-section.active,
.about-section.active,
.contact-section.active{
    position: relative;
    opacity: 1;
    z-index: 8;
}
```

</details>
<details>
<summary><code>Projects Section CSS</code></summary>

```
.project-section{
    width: 100%;
    min-height: 100vh;
    padding: 150px 100px 100px;
    position: fixed;
    top: 0;
    transition: 1s;
    opacity: 0;
}

.project-heading{
    font-size: 100px;
    background: #252525;
    text-transform: capitalize;
    text-align: center;
    margin-bottom: 50px;
    color: #514f4f;
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-stroke: 8px transparent;
}

.project-container{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-gap: 100px;
}

.project-card{
    height: 400px;
    position: relative;
}

.project-img{
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    object-fit: cover;
    transition: .5s;
}

.project-content{
    position: relative;
    padding: 40px;
    color: #fff;
    transition: .5s;
    opacity: 0;
}

.project-title{
    font-size: 50px;
    text-transform: capitalize;
    text-align: center;
    font-weight: 300;
}

.project-info{
    margin: 40px;
    font-size: 20px;
    line-height: 30px;
    text-align: center;
}

.project-btn-grp{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-gap: 20px;
}

.project-btn{
    height: 40px;
    text-transform: capitalize;
    font-size: 18px;
    border: none;
    background: #000;
    color: #fff;
    cursor: pointer;
}

.project-btn.live{
    background: none;
    border: 2px solid #fff;
}

.project-card:hover .project-img{
    filter: blur(20px);
}

.project-card:hover .project-content{
    opacity: 1;
}
```

</details>
<details>
<summary><code>About Section CSS</code></summary>

```
.about-section{
    width: 100%;
    min-height: 100vh;
    padding: 150px 100px 0;
    position: fixed;
    top: 0;
    opacity: 0;
    transition: 1s;
}

.about{
    width: 100%;
    display: grid;
    grid-template-columns: 30% 65%;
    grid-gap: 40px;
}

.about-img-container{
    position: relative;
}

.about-info{
    color: #fff;
    opacity: 0.6;
    font-size: 20px;
    line-height: 40px;
}

.about-img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 20px;
}

.download-cv-btn{
    position: absolute;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%);
    padding: 10px 20px;
    color: #fff;
    border: none;
    font-size: 16px;
    text-transform: capitalize;
    cursor: pointer;
    transition: .5s;
    background: rgba(0, 0, 0, 0.5);
}

.download-cv-btn:hover{
    background: #000;
}
```

</details>

<details>
<summary><code>Skills Section CSS</code></summary>

```
.skill-section{
    position: relative;
    margin: 100px 0;
}

.heading{
    text-align: center;
    font-size: 60px;
    color: #fff;
    text-transform: capitalize;
    font-weight: 300;
    margin-bottom: 100px;
}

.skills-container{
    width: 95%;
    margin: auto;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 100px;
    color: #fff;
}

.skill-card{
    position: relative;
}

.skill-img{
    display: block;
    margin: auto;
    height: 200px;
}

.skill-name{
    font-size: 30px;
    font-weight: 300;
    text-align: center;
    text-transform: capitalize;
    margin: 30px 0 20px;
}

.skill-info{
    text-align: center;
    opacity: 0.5;
    font-size: 18px;
    line-height: 30px;
}

.skill-level{
    position: absolute;
    top: 80px;
    right: 0;
    width: 150px;
    height: 150px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 22px;
    border-radius: 50%;
    border: 10px solid;
}

.skill-card:nth-child(1) .skill-level{
    background: #ff4f4f28;
    border-color: #ff4f4f;
    color: #ff4f4f;
}

.skill-card:nth-child(2) .skill-level{
    background: #4fa0ff28;
    border-color: #4fa0ff;
    color: #4fa0ff;
}

.skill-card:nth-child(3) .skill-level{
    background: #ffed4f28;
    border-color: #ffed4f;
    color: #ffed4f;
}

.skill-card:nth-child(4) .skill-level{
    background: #52ff4f28;
    border-color: #52ff4f;
    color: #52ff4f;
}

.skill-card:nth-child(5) .skill-level{
    background: #4fdfff28;
    border-color: #4fdfff;
    color: #4fdfff;
}
```
</details>
<details>
<summary><code>Timeline Section CSS</code></summary>

```
.timeline{
    display: block;
    width: 80%;
    margin: 150px auto;
}

.timeline .heading{
    margin-bottom: 150px;
}

.card{
    width: 45%;
    padding: 30px;
    border-radius: 10px;
    color: #fff;
    display: block;
    margin: -80px 0;
    position: relative;
    background: #f00;
}

.card:nth-child(even){
    margin-left: auto;
}

.card:nth-child(even):before{
    content: '';
    position: absolute;
    left: -15%;
    top: 50%;
    transform: translateY(-50%);
    width: 20px;
    height: 20px;
    border: 5px solid #191919;
    border-radius: 50%;
}

.card:nth-child(even):after{
    content: '';
    position: absolute;
    left: -8.5%;
    top: 50%;
    transform: translateY(-50%);
    width: 7%;
    height: 2px;
    background: #fff;
    z-index: -1;
}

.card:nth-child(odd):before{
    content: '';
    position: absolute;
    right: -13%;
    top: 50%;
    transform: translateY(-50%);
    width: 20px;
    height: 20px;
    border: 5px solid #191919;
    border-radius: 50%;
}

.card:nth-child(odd):after{
    content: '';
    position: absolute;
    right: -8.5%;
    top: 50%;
    transform: translateY(-50%);
    width: 7%;
    height: 2px;
    background: #fff;
    z-index: -1;
}

.card:nth-child(2), .card:nth-child(2):before{
    background: #ff4f4f;
}
.card:nth-child(3), .card:nth-child(3):before{
    background: #ffb84f;
}
.card:nth-child(4), .card:nth-child(4):before{
    background: #3dca5c;
}
.card:nth-child(5), .card:nth-child(5):before{
    background: #565252;
}
.card:nth-child(6), .card:nth-child(6):before{
    background: #4fa0ff;
}

.card:nth-child(even) .card-body:before{
    content: '';
    position: absolute;
    left: -12%;
    top: 0;
    width: 0px;
    height: 100%;
    border: 1px dashed #fff;
    z-index: -1;
}

.card-title{
    font-size: 30px;
    font-weight: 300;
    margin-bottom: 20px;
}
```
</details>
<details>
<summary><code>Contact Section CSS</code></summary>

```
.contact-section{
    position: absolute;
    top: 0;
    opacity: 0;
    transition: 1s;
    padding: 100px 150px;
    height: 100vh;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-gap: 50px;
}

.contact-form input, .contact-form textarea{
    width: 100%;
    height: 40px;
    background: rgba(255, 255, 255, 0.2);
    border: 1px solid #fff;
    margin-bottom: 30px;
    border-radius: 5px;
    /* text-transform: capitalize; */
    color: #fff;
    padding: 5px 10px;
}

::placeholder{
    color: #fff;
}

#msg{
    height: 280px;
    resize: none;
    font-family: sans-serif;
}

.form-submit-btn{
    background: #ff4f4f;
    color: #fff;
    text-transform: capitalize;
    padding: 15px 40px;
    display: block;
    margin: auto;
    border: none;
    border-radius: 10px;
    cursor: pointer;
    font-weight: bold;
}

.form-submit-btn:hover {
    background-color: #fff;
    color: #ff4f4f;
   
}
```
</details>
<details>
<summary><code>Map CSS</code></summary>

```
.map{
    width: 100%;
    height: 100%;
    padding: 10px;
    border: 2px solid #fff;
    background: rgba(255, 255, 255, 0.2);
    border-radius: 10px;
}

.map iframe{
    width: 100%;
    height: 100%;
    border-radius: 5px;
}
```
</details>


## Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/portfolio_tutorial.git



```
