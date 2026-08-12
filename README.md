# Ex02 Commercial Website
## Date:11/08/2026
## Name: DEEPIKA G
## Reg no:212224040060

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
## HTML
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <link rel="icon" href="%PUBLIC_URL%/favicon.ico" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <meta name="theme-color" content="#000000" />
    <meta
      name="description"
      content="Web site created using create-react-app"
    />
    <link rel="apple-touch-icon" href="%PUBLIC_URL%/logo192.png" />
    <!--
      manifest.json provides metadata used when your web app is installed on a
      user's mobile device or desktop. See https://developers.google.com/web/fundamentals/web-app-manifest/
    -->
    <link rel="manifest" href="%PUBLIC_URL%/manifest.json" />
    <!--
      Notice the use of %PUBLIC_URL% in the tags above.
      It will be replaced with the URL of the `public` folder during the build.
      Only files inside the `public` folder can be referenced from the HTML.

      Unlike "/favicon.ico" or "favicon.ico", "%PUBLIC_URL%/favicon.ico" will
      work correctly both with client-side routing and a non-root public URL.
      Learn how to configure a non-root public URL by running `npm run build`.
    -->
    <title>React App</title>
  </head>
  <body>
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
    <!--
      This HTML file is a template.
      If you open it directly in the browser, you will see an empty page.

      You can add webfonts, meta tags, or analytics to this file.
      The build step will place the bundled scripts into the <body> tag.

      To begin the development, run `npm start` or `yarn start`.
      To create a production bundle, use `npm run build` or `yarn build`.
    -->
  </body>
</html>
```
## CSS
## login.css
```
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, Helvetica, sans-serif;
}

body{

    background:#f4f7fb;

}

.login-page{

    min-height:100vh;

    display:flex;

    justify-content:center;

    align-items:center;

    background:linear-gradient(135deg,#2563eb,#7c3aed);

}

.login-card{

    width:400px;

    background:white;

    padding:45px;

    border-radius:20px;

    box-shadow:0 20px 40px rgba(0,0,0,.25);

    text-align:center;

    animation:popup .5s ease;

}

@keyframes popup{

    from{

        opacity:0;

        transform:translateY(40px);

    }

    to{

        opacity:1;

        transform:translateY(0);

    }

}

.logo{

    width:90px;

    height:90px;

    margin:auto;

    border-radius:50%;

    background:#2563eb;

    color:white;

    font-size:42px;

    display:flex;

    justify-content:center;

    align-items:center;

    margin-bottom:20px;

}

.login-card h1{

    color:#1e293b;

    margin-bottom:8px;

}

.login-card p{

    color:#64748b;

    margin-bottom:30px;

}

.login-card input{

    width:100%;

    padding:15px;

    margin-bottom:18px;

    border:1px solid #ddd;

    border-radius:10px;

    font-size:16px;

    transition:.3s;

}

.login-card input:focus{

    outline:none;

    border-color:#2563eb;

    box-shadow:0 0 8px rgba(37,99,235,.3);

}

.login-card button{

    width:100%;

    padding:15px;

    border:none;

    border-radius:10px;

    background:#2563eb;

    color:white;

    font-size:18px;

    cursor:pointer;

    transition:.3s;

}

.login-card button:hover{

    background:#1d4ed8;

    transform:translateY(-2px);

}

.error{

    background:#fee2e2;

    color:#b91c1c;

    padding:10px;

    margin-bottom:18px;

    border-radius:8px;

}

.demo{

    margin-top:25px;

    background:#eff6ff;

    padding:15px;

    border-radius:10px;

    color:#1e40af;

    font-size:15px;

}
```
## product-card.css
```
/* ===========================
   PRODUCT CARD
=========================== */

.product-card{
    position:relative;
    width:320px;
    background:#fff;
    border-radius:18px;
    overflow:hidden;
    box-shadow:0 8px 25px rgba(0,0,0,.08);
    transition:all .4s ease;
    cursor:pointer;
}

.product-card:hover{
    transform:translateY(-12px);
    box-shadow:0 18px 45px rgba(0,0,0,.18);
}

/* Gradient Border Effect */

.product-card::before{
    content:"";
    position:absolute;
    inset:0;
    border-radius:18px;
    padding:2px;
    background:linear-gradient(
        135deg,
        #00b894,
        #00cec9,
        #74b9ff,
        #0984e3
    );
    -webkit-mask:
      linear-gradient(#fff 0 0) content-box,
      linear-gradient(#fff 0 0);
    -webkit-mask-composite:xor;
            mask-composite:exclude;
    opacity:0;
    transition:.4s;
}

.product-card:hover::before{
    opacity:1;
}

/* ===========================
   IMAGE
=========================== */

.product-image{
    overflow:hidden;
    height:220px;
}

.product-image img{
    width:100%;
    height:100%;
    object-fit:cover;
    transition:transform .5s ease;
}

.product-card:hover .product-image img{
    transform:scale(1.12) rotate(2deg);
}

/* ===========================
   CONTENT
=========================== */

.product-content{
    padding:20px;
}

.product-title{
    font-size:22px;
    font-weight:700;
    margin-bottom:10px;
    color:#222;
    transition:.3s;
}

.product-card:hover .product-title{
    color:#0984e3;
}

.product-description{
    color:#666;
    line-height:1.6;
    margin-bottom:18px;
    font-size:15px;
}

/* ===========================
   PRICE
=========================== */

.product-price{
    font-size:24px;
    color:#16a085;
    font-weight:bold;
    transition:.4s;
}

.product-card:hover .product-price{
    transform:scale(1.08);
    letter-spacing:1px;
}

/* ===========================
   BUTTON
=========================== */

.product-btn{
    margin-top:20px;
    width:100%;
    padding:12px;
    border:none;
    border-radius:10px;
    font-size:16px;
    font-weight:bold;
    color:white;
    background:linear-gradient(
        135deg,
        #00b894,
        #00cec9
    );
    cursor:pointer;
    transition:.35s;
}

.product-btn:hover{
    background:linear-gradient(
        135deg,
        #0984e3,
        #6c5ce7
    );
    transform:translateY(-3px);
    box-shadow:0 10px 20px rgba(9,132,227,.35);
}

/* ===========================
   BADGE
=========================== */

.product-badge{
    position:absolute;
    top:15px;
    left:15px;
    background:#ff4757;
    color:white;
    padding:6px 14px;
    border-radius:20px;
    font-size:13px;
    font-weight:bold;
    z-index:10;
    animation:pulse 2s infinite;
}

@keyframes pulse{

    0%{
        transform:scale(1);
    }

    50%{
        transform:scale(1.08);
    }

    100%{
        transform:scale(1);
    }

}

/* ===========================
   FAVORITE ICON
=========================== */

.favorite{
    position:absolute;
    right:18px;
    top:18px;
    width:40px;
    height:40px;
    background:white;
    border-radius:50%;
    display:flex;
    align-items:center;
    justify-content:center;
    box-shadow:0 5px 15px rgba(0,0,0,.12);
    transition:.3s;
}

.favorite:hover{
    background:#ff4757;
    color:white;
    transform:rotate(360deg);
}

/* ===========================
   RESPONSIVE
=========================== */

@media(max-width:768px){

.product-card{
    width:100%;
}

.product-image{
    height:200px;
}

}
```
## product.css
```
/* ===========================
   Products Container
=========================== */

.products-container{
    width: 95%;
    max-width: 1400px;
    margin: 40px auto;

    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    gap: 30px;

    padding: 20px;
}

/* Animation */

.products-container > *{
    animation: fadeUp .6s ease;
}

@keyframes fadeUp{
    from{
        opacity:0;
        transform:translateY(30px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}


/* Tablet */

@media(max-width:992px){

    .products-container{
        grid-template-columns:repeat(2,1fr);
        gap:20px;
    }

}

/* Mobile */

@media(max-width:700px){

    .products-container{
        grid-template-columns:1fr;
        width:95%;
        padding:10px;
    }

}
```
## register.css
```
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,Helvetica,sans-serif;
}

body{

    background:#f4f7fb;

}

/* ===========================
   PAGE
=========================== */
.register-page{

    min-height:calc(100vh - 80px);

    width:100%;
    
    background:#2563eb;

    display:flex;

    justify-content:center;

    align-items:center;

    padding:40px;

}

/* ===========================
   CARD
=========================== */

.register-card{

    width:500px;

    background:white;

    padding:40px;

    border-radius:20px;

    box-shadow:0 20px 40px rgba(0,0,0,.25);

    animation:popup .5s ease;

}

@keyframes popup{

    from{

        opacity:0;

        transform:translateY(40px);

    }

    to{

        opacity:1;

        transform:translateY(0);

    }

}

/* ===========================
   LOGO
=========================== */

.logo{

    width:90px;

    height:90px;

    margin:auto;

    margin-bottom:20px;

    border-radius:50%;

    background:#2563eb;

    color:white;

    display:flex;

    justify-content:center;

    align-items:center;

    font-size:42px;

}

/* ===========================
   TITLE
=========================== */

.register-card h2{

    text-align:center;

    color:#1e293b;

    margin-bottom:8px;

}

.register-card p{

    text-align:center;

    color:#64748b;

    margin-bottom:25px;

}

/* ===========================
   INPUTS
=========================== */

.register-card input,
.register-card select{

    width:100%;

    padding:14px;

    margin-bottom:15px;

    border:1px solid #d1d5db;

    border-radius:10px;

    font-size:15px;

    transition:.3s;

}

.register-card input:focus,
.register-card select:focus{

    outline:none;

    border-color:#2563eb;

    box-shadow:0 0 8px rgba(37,99,235,.3);

}

/* ===========================
   PASSWORD BOX
=========================== */

.password-box{

    display:flex;

    gap:10px;

    margin-bottom:10px;

}

.password-box input{

    flex:1;

    margin-bottom:0;

}

.password-box button{

    width:90px;

    border:none;

    border-radius:10px;

    background:#2563eb;

    color:white;

    cursor:pointer;

    transition:.3s;

}

.password-box button:hover{

    background:#1d4ed8;

}

/* ===========================
   PASSWORD STRENGTH
=========================== */

small{

    display:block;

    margin-bottom:15px;

    font-weight:bold;

}

.Weak{

    color:red;

}

.Medium{

    color:orange;

}

.Strong{

    color:green;

}

/* ===========================
   GENDER
=========================== */

.radio-group{

    display:flex;

    justify-content:space-around;

    margin:15px 0;

}

.radio-group label{

    display:flex;

    align-items:center;

    gap:6px;

    color:#334155;

    font-weight:600;

}

.radio-group input{

    width:auto;

    margin:0;

}

/* ===========================
   TERMS
=========================== */

.terms{

    display:flex;

    align-items:center;

    gap:10px;

    margin:15px 0;

    color:#334155;

    font-size:15px;

}

.terms input{

    width:auto;

    margin:0;

}

/* ===========================
   BUTTON
=========================== */

.register-btn{

    width:100%;

    padding:15px;

    border:none;

    border-radius:10px;

    background:#2563eb;

    color:white;

    font-size:18px;

    cursor:pointer;

    transition:.3s;

}

.register-btn:hover{

    background:#1d4ed8;

    transform:translateY(-2px);

}

/* ===========================
   ERRORS
=========================== */

span{

    display:block;

    color:#dc2626;

    font-size:13px;

    margin-top:-10px;

    margin-bottom:12px;

}

/* ===========================
   INFO BOX
=========================== */

.info-box{

    margin-top:25px;

    background:#eff6ff;

    padding:15px;

    border-radius:10px;

    color:#1e40af;

    text-align:center;

    font-size:15px;

}

/* ===========================
   HOVER EFFECT
=========================== */

.register-card:hover{

    transform:translateY(-3px);

    transition:.3s;

}

/* ===========================
   RESPONSIVE
=========================== */

@media(max-width:600px){

.register-card{

    width:100%;

    padding:25px;

}

.logo{

    width:70px;
    height:70px;
    font-size:32px;

}

.register-card h2{

    font-size:24px;

}

}
```
## JAVASCRIPT
## Home.jsx
```
function Home() {
  return (
    <>
      <section className="hero">
        <h1>Welcome to ShopSphere</h1>

        <p>
          Build a complete React Product Review Application from scratch.
        </p>

        <button>Browse Products</button>
      </section>

      <section>

        <h2 className="section-title">
          Featured Products
        </h2>

        <div className="card-container">

          <div className="card">
            <h3>💻 Laptop</h3>
            <p>High Performance</p>
          </div>

          <div className="card">
            <h3>📱 Mobile</h3>
            <p>Latest Smartphones</p>
          </div>

          <div className="card">
            <h3>🎧 Headphones</h3>
            <p>Crystal Clear Sound</p>
          </div>

          <div className="card">
            <h3>⌚ Smart Watch</h3>
            <p>Fitness Tracking</p>
          </div>

        </div>

      </section>

      <section>

        <h2 className="section-title">
          Why ShopSphere?
        </h2>

        <div className="card-container">

          <div className="card">
            ⭐ Trusted Reviews
          </div>

          <div className="card">
            🚚 Fast Delivery
          </div>

          <div className="card">
            🔒 Secure Shopping
          </div>

        </div>

      </section>

      <section className="cta">

        <h2>
          Start Learning React with Real Projects
        </h2>

        <button>Get Started</button>

      </section>

    </>
  );
}

export default Home;
```
## Login.jsx
```
import { useState } from "react";
import { useNavigate } from "react-router-dom";
import "../css/login.css";

function Login() {

    const navigate = useNavigate();

    const [username, setUsername] = useState("");
    const [password, setPassword] = useState("");
    const [error, setError] = useState("");

    const login = (e) => {

        e.preventDefault();

        if (username === "admin" && password === "admin") {

            navigate("/");

        } else {

            setError("Invalid Username or Password");

        }

    };

    return (

        <div className="login-page">

            <div className="login-card">

                <div className="logo">

                    🛍️

                </div>

                <h1>Welcome Back</h1>

                <p>Login to continue shopping</p>

                <form onSubmit={login}>

                    <input
                        type="text"
                        placeholder="Username"
                        value={username}
                        onChange={(e) => setUsername(e.target.value)}
                    />

                    <input
                        type="password"
                        placeholder="Password"
                        value={password}
                        onChange={(e) => setPassword(e.target.value)}
                    />

                    {error && <div className="error">{error}</div>}

                    <button>

                        Login

                    </button>

                </form>

                <div className="demo">

                    Demo Login

                    <br />

                    <strong>admin / admin</strong>

                </div>

            </div>

        </div>

    );

}

export default Login;
```

## OUTPUT

<img width="1917" height="1077" alt="image" src="https://github.com/user-attachments/assets/e8884615-1df8-46df-ab63-9a436400eac6" />


<img width="1916" height="1083" alt="image" src="https://github.com/user-attachments/assets/cee9988c-29ac-42ae-8798-79673f51b56d" />

<img width="1917" height="1086" alt="image" src="https://github.com/user-attachments/assets/4beb0ea2-736e-4d63-ab36-fba27f56a03d" />

## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
