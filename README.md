<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover" />
<meta name="theme-color" content="#0f1a24" />
<meta name="apple-mobile-web-app-capable" content="yes" />
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent" />
<meta name="format-detection" content="telephone=yes" />
<title>Sunruth Varma · Child Artist Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet" />
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
<style>
/* ========== RESET ========== */
*{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent}
html{-webkit-text-size-adjust:100%;text-size-adjust:100%}
body{
  background:#f0f5fa;
  font-family:'Inter',-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,sans-serif;
  display:flex;justify-content:center;
  padding:2rem 1rem;
  color:#1e2b3c;line-height:1.5;
  padding-left:max(1rem,env(safe-area-inset-left));
  padding-right:max(1rem,env(safe-area-inset-right));
  padding-top:max(2rem,env(safe-area-inset-top));
  padding-bottom:max(2rem,env(safe-area-inset-bottom));
}

/* ========== PORTFOLIO CONTAINER ========== */
.portfolio{
  max-width:1200px;width:100%;background:#fff;
  border-radius:2.5rem;
  box-shadow:0 30px 50px -20px rgba(0,20,30,.25);
  overflow:hidden;
}

/* ========== HEADER ========== */
.profile-header{
  display:flex;align-items:center;gap:2rem;
  background:linear-gradient(145deg,#0f1a24,#1e2b3c);
  padding:2rem 2.8rem;color:#fff;flex-wrap:wrap;
}
.profile-image-container{
  flex-shrink:0;width:140px;height:140px;border-radius:50%;
  border:5px solid #f7c948;
  box-shadow:0 10px 20px rgba(0,0,0,.35);
  overflow:hidden;background:#2e3f52;
  display:flex;align-items:center;justify-content:center;
}
.profile-image-container img{width:100%;height:100%;object-fit:cover;display:block}
.header-text{flex:1;min-width:0}
.header-text h1{
  font-size:2.7rem;font-weight:700;letter-spacing:-.5px;
  margin-bottom:.25rem;color:#f7c948;
  text-shadow:0 2px 5px rgba(0,0,0,.3);
}
.header-text .tagline{
  font-size:1.2rem;font-weight:400;opacity:.9;
  margin-bottom:1rem;border-left:4px solid #f7c948;
  padding-left:1rem;
}
.quick-info{
  display:flex;flex-wrap:wrap;gap:1.8rem;font-size:1rem;
  background:rgba(255,255,255,.08);
  padding:.8rem 1.8rem;border-radius:60px;
  backdrop-filter:blur(8px);
  border:1px solid rgba(255,255,255,.1);
}
.quick-info span{display:flex;align-items:center;gap:.5rem}
.quick-info i{color:#f7c948;font-size:1.1rem}

/* ========== TABS ========== */
.tab-bar{
  display:flex;flex-wrap:wrap;gap:.5rem;
  padding:1.5rem 2.8rem 0 2.8rem;
  background:#fff;border-bottom:2px solid #e6edf5;
  overflow-x:auto;-webkit-overflow-scrolling:touch;
  scrollbar-width:none;
}
.tab-bar::-webkit-scrollbar{display:none}
.tab-btn{
  background:transparent;border:none;
  padding:.9rem 1.6rem;font-size:1rem;font-weight:600;
  font-family:inherit;color:#5c6f82;cursor:pointer;
  border-radius:1rem 1rem 0 0;transition:.2s;
  display:inline-flex;align-items:center;gap:.5rem;
  position:relative;top:2px;flex-shrink:0;
  -webkit-appearance:none;appearance:none;
}
.tab-btn:hover{color:#1e2b3c;background:#f2f8ff}
.tab-btn.active{
  color:#0f1a24;background:#f2f8ff;
  border-bottom:3px solid #f7c948;font-weight:700;
}
.tab-btn.active i{color:#f7c948}

/* ========== TAB PANELS ========== */
.tab-panel{
  display:none;padding:2rem 2.8rem 2.8rem 2.8rem;
  animation:fadeIn .25s ease;
}
.tab-panel.active{display:block}
@keyframes fadeIn{from{opacity:0;transform:translateY(6px)}to{opacity:1;transform:translateY(0)}}

/* ========== GALLERY ========== */
.gallery-section h2{
  font-size:1.7rem;font-weight:700;color:#0f1a24;
  margin-bottom:1.5rem;display:flex;align-items:center;gap:.8rem;
}
.gallery-section h2 i{color:#f7c948;font-size:1.8rem}
.photo-grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(150px,1fr));
  gap:1.3rem;margin-bottom:.5rem;
}
.photo-card{
  background:#eef2f7;border-radius:1.6rem;overflow:hidden;
  box-shadow:0 8px 16px -6px rgba(0,0,0,.1);
  transition:transform .2s,box-shadow .2s;
  aspect-ratio:1/1;display:flex;
  align-items:center;justify-content:center;
  border:3px solid #fff;outline:1px solid #dbe4ed;
}
.photo-card:hover{
  transform:translateY(-4px) scale(1.01);
  box-shadow:0 18px 28px -8px rgba(0,30,50,.2);
}
.photo-card img{width:100%;height:100%;object-fit:cover;display:block}
.img-fallback{
  background:#d9e2ec;display:flex;
  align-items:center;justify-content:center;
  color:#2e3f52;font-weight:600;font-size:1rem;
  text-align:center;padding:.5rem;width:100%;height:100%;
  flex-direction:column;gap:.3rem;
}
.img-fallback i{font-size:2rem;opacity:.6}

/* ========== DETAILS & EXPERIENCE ========== */
.details-section{display:grid;grid-template-columns:1fr 2fr;gap:2rem}
.info-card{
  background:#f8fbfe;border-radius:2rem;padding:2rem 1.8rem;
  box-shadow:inset 0 0 0 1px #fff,0 10px 20px -10px rgba(0,0,0,.05);
  border:1px solid #e6edf5;
}
.info-card h3{
  font-size:1.4rem;font-weight:700;color:#0f1a24;
  margin-bottom:1.5rem;border-bottom:4px solid #f7c948;
  display:inline-block;padding-bottom:.4rem;
}
.info-list p{
  margin-bottom:.9rem;font-size:1.05rem;color:#2e3f52;
  display:flex;align-items:baseline;flex-wrap:wrap;
}
.info-list strong{width:110px;display:inline-block;font-weight:700;color:#0f1a24}
.info-list a{
  color:#0f1a24;text-decoration:none;font-weight:600;
  background:#f7c948;padding:.2rem 1rem;border-radius:40px;
  font-size:.95rem;transition:.2s;display:inline-block;margin-top:.2rem;
}
.info-list a:hover{background:#e0b130;transform:scale(1.02)}

/* Experience */
.experience-list{display:flex;flex-direction:column;gap:1.4rem}
.exp-item{
  background:#fff;border-radius:1.6rem;padding:1.4rem 1.8rem;
  box-shadow:0 6px 14px rgba(0,0,0,.02);
  border-left:6px solid #f7c948;
  transition:.15s;border:1px solid #e6edf5;border-left-width:6px;
}
.exp-item:hover{
  box-shadow:0 12px 24px -10px rgba(0,30,50,.15);
  border-color:#d0dfee;border-left-color:#f7c948;
}
.exp-item h4{
  font-size:1.2rem;font-weight:700;color:#0f1a24;
  margin-bottom:.25rem;display:flex;align-items:center;
  gap:.5rem;flex-wrap:wrap;
}
.exp-item h4 i{color:#f7c948;font-size:1rem}
.exp-item .role{
  font-weight:600;color:#1e5c8b;margin-bottom:.5rem;
  font-size:1rem;display:flex;flex-wrap:wrap;align-items:center;gap:.5rem;
}
.exp-item .role .badge{
  background:#e3eef9;padding:.2rem 1rem;border-radius:50px;
  font-size:.75rem;font-weight:700;letter-spacing:.3px;
  text-transform:uppercase;color:#0f1a24;
}
.exp-item .video-links{display:flex;flex-wrap:wrap;gap:.8rem;margin-top:.7rem}
.exp-item .video-links a{
  color:#0f1a24;text-decoration:none;background:#eef2f7;
  padding:.35rem 1.2rem;border-radius:40px;font-size:.88rem;
  font-weight:600;display:inline-flex;align-items:center;gap:.4rem;
  transition:.2s;border:1px solid #d0dfee;
}
.exp-item .video-links a i{color:#f7c948;font-size:.9rem}
.exp-item .video-links a:hover{
  background:#f7c948;border-color:#f7c948;transform:translateY(-2px);
}
.exp-item .video-links a:hover i{color:#0f1a24}
.award-tag{
  background:#f7c948;color:#0f1a24;font-weight:700;
  font-size:.8rem;padding:.25rem 1rem;border-radius:40px;
  display:inline-block;margin-left:.6rem;
}

/* ========== ABOUT ========== */
.about-content{max-width:900px;margin:0 auto}
.about-content h2{
  font-size:1.9rem;font-weight:700;color:#0f1a24;
  margin-bottom:1.5rem;display:flex;align-items:center;gap:.8rem;
}
.about-content h2 i{color:#f7c948;font-size:2rem}
.about-card{
  background:#f8fbfe;border-radius:2rem;
  padding:2rem 2.2rem;border:1px solid #e6edf5;
  box-shadow:0 10px 20px -12px rgba(0,0,0,.08);
  line-height:1.8;font-size:1.05rem;color:#2e3f52;
}
.about-card p{margin-bottom:1.2rem}
.about-card p:last-child{margin-bottom:0}
.about-card .highlight{
  background:#fff6d9;padding:.15rem .6rem;border-radius:30px;
  font-weight:600;color:#0f1a24;display:inline-block;
}
.about-card .quote-mark{
  color:#f7c948;font-size:1.4rem;
  margin-right:.4rem;vertical-align:middle;opacity:.8;
}
.about-card strong{color:#0f1a24}
.about-card em{color:#1e5c8b;font-style:italic}

/* ========== CONTACT ========== */
.contact-content{max-width:700px;margin:0 auto}
.contact-content h2{
  font-size:1.9rem;font-weight:700;color:#0f1a24;
  margin-bottom:1.5rem;display:flex;align-items:center;gap:.8rem;
}
.contact-content h2 i{color:#f7c948;font-size:2rem}
.contact-card{
  background:linear-gradient(145deg,#0f1a24,#1e2b3c);
  border-radius:2rem;padding:2.5rem 2.2rem;color:#fff;
  box-shadow:0 18px 30px -14px rgba(0,20,30,.4);
}
.contact-card .contact-row{
  display:flex;align-items:center;gap:1.2rem;
  padding:1.2rem 0;border-bottom:1px solid rgba(255,255,255,.1);
  flex-wrap:wrap;
}
.contact-card .contact-row:last-child{border-bottom:none}
.contact-card .contact-icon{
  width:52px;height:52px;background:rgba(247,201,72,.15);
  border-radius:50%;display:flex;align-items:center;justify-content:center;
  flex-shrink:0;border:1px solid rgba(247,201,72,.3);
}
.contact-card .contact-icon i{font-size:1.4rem;color:#f7c948}
.contact-card .contact-detail{flex:1;min-width:0}
.contact-card .contact-detail .label{
  font-size:.85rem;text-transform:uppercase;letter-spacing:1px;
  opacity:.7;margin-bottom:.2rem;font-weight:500;
}
.contact-card .contact-detail .value{
  font-size:1.25rem;font-weight:600;color:#fff;word-break:break-word;
}
.contact-card .contact-detail .value a{
  color:#f7c948;text-decoration:none;
  border-bottom:2px dotted rgba(247,201,72,.5);transition:.2s;
}
.contact-card .contact-detail .value a:hover{
  border-bottom:2px solid #f7c948;color:#ffdd77;
}
.contact-note{
  margin-top:1.8rem;background:#f2f8ff;border-radius:1.4rem;
  padding:1.2rem 1.6rem;font-size:.95rem;color:#2e3f52;
  border:1px dashed #b8cee4;text-align:center;
}
.contact-note i{color:#f7c948;margin-right:.4rem}

/* ============================================================
   MOBILE OPTIMIZATIONS — iOS (iPhone / iPad) & ANDROID
   ============================================================ */

/* ---------- Large tablets / small laptops ---------- */
@media (max-width: 900px) {
  .details-section{grid-template-columns:1fr}
}

/* ---------- Phones & small tablets ---------- */
@media (max-width: 768px) {
  body{padding:1rem .75rem}
  .portfolio{border-radius:2rem}

  /* Header becomes centered vertical stack */
  .profile-header{
    flex-direction:column;
    text-align:center;
    padding:2rem 1.25rem 1.75rem;
    gap:1.25rem;
  }
  .profile-image-container{
    width:130px;height:130px;
    border-width:4px;
  }
  .header-text h1{font-size:2rem;line-height:1.15}
  .header-text .tagline{
    border-left:none;
    padding-left:0;
    font-size:1.05rem;
    margin-bottom:.85rem;
  }
  .quick-info{
    justify-content:center;
    gap:1rem;
    padding:.7rem 1.2rem;
    font-size:.9rem;
    border-radius:50px;
  }

  /* Tabs scroll horizontally like iOS segmented control */
  .tab-bar{
    padding:1rem 1rem 0 1rem;
    gap:.35rem;
    justify-content:flex-start;
    flex-wrap:nowrap;
    overflow-x:auto;
    scroll-snap-type:x mandatory;
  }
  .tab-btn{
    padding:.75rem 1.1rem;
    font-size:.92rem;
    scroll-snap-align:start;
    white-space:nowrap;
  }

  /* Panels */
  .tab-panel{padding:1.5rem 1.1rem 2rem 1.1rem}
  .gallery-section h2{font-size:1.35rem;margin-bottom:1.1rem}
  .gallery-section h2 i{font-size:1.4rem}

  /* Two‑column photo grid on phones */
  .photo-grid{
    grid-template-columns:repeat(2,1fr);
    gap:.85rem;
  }
  .photo-card{border-radius:1.25rem;border-width:2px}

  /* Info cards */
  .info-card{padding:1.5rem 1.2rem;border-radius:1.6rem}
  .info-card h3{font-size:1.2rem;margin-bottom:1.1rem}
  .info-list p{
    flex-direction:column;
    gap:.1rem;
    margin-bottom:.85rem;
    font-size:.98rem;
  }
  .info-list strong{width:auto}
  .info-list a{font-size:.88rem;padding:.25rem .9rem}

  /* Experience cards */
  .exp-item{padding:1.15rem 1.25rem;border-radius:1.35rem}
  .exp-item h4{font-size:1.05rem}
  .exp-item .role{font-size:.92rem}
  .exp-item .video-links a{
    font-size:.82rem;
    padding:.35rem 1rem;
  }

  /* About */
  .about-content h2{font-size:1.45rem}
  .about-content h2 i{font-size:1.55rem}
  .about-card{
    padding:1.4rem 1.25rem;
    border-radius:1.5rem;
    font-size:.98rem;
    line-height:1.7;
  }

  /* Contact */
  .contact-content h2{font-size:1.45rem}
  .contact-content h2 i{font-size:1.55rem}
  .contact-card{
    padding:1.6rem 1.25rem;
    border-radius:1.5rem;
  }
  .contact-card .contact-row{gap:.9rem;padding:1rem 0}
  .contact-card .contact-icon{
    width:44px;height:44px;
  }
  .contact-card .contact-icon i{font-size:1.15rem}
  .contact-card .contact-detail .value{font-size:1.05rem}
  .contact-card .contact-detail .label{font-size:.75rem}
  .contact-note{
    padding:1rem 1.15rem;
    font-size:.9rem;
    border-radius:1.2rem;
  }
}

/* ---------- Small phones (iPhone SE, etc.) ---------- */
@media (max-width: 480px) {
  body{padding:.75rem .5rem}
  .portfolio{border-radius:1.5rem}

  .profile-header{padding:1.75rem 1rem 1.5rem}
  .profile-image-container{width:115px;height:115px}
  .header-text h1{font-size:1.75rem}
  .header-text .tagline{font-size:.95rem}
  .quick-info{
    gap:.75rem;
    padding:.6rem 1rem;
    font-size:.82rem;
  }
  .quick-info i{font-size:.95rem}

  .tab-btn{
    padding:.65rem .9rem;
    font-size:.85rem;
  }

  .tab-panel{padding:1.25rem .9rem 1.75rem .9rem}

  .gallery-section h2{font-size:1.2rem}

  .photo-grid{gap:.7rem}
  .photo-card{border-radius:1.1rem}

  .info-card{padding:1.25rem 1rem}
  .info-list p{font-size:.92rem}

  .exp-item{padding:1rem 1.05rem}
  .exp-item h4{font-size:1rem}
  .exp-item .role{font-size:.88rem}

  .about-card{padding:1.25rem 1.05rem;font-size:.94rem}
  .contact-card{padding:1.4rem 1.05rem}
  .contact-card .contact-detail .value{font-size:1rem}
}

/* ---------- iOS notched devices (iPhone X / 11 / 12 / 13 / 14 / 15) ---------- */
@supports (padding: max(0px)) {
  body{
    padding-left: max(1rem, env(safe-area-inset-left));
    padding-right: max(1rem, env(safe-area-inset-right));
    padding-bottom: max(2rem, env(safe-area-inset-bottom));
  }
  .tab-bar{
    padding-left: max(1rem, env(safe-area-inset-left));
    padding-right: max(1rem, env(safe-area-inset-right));
  }
}

/* ---------- Prevent iOS input zoom on tel links ---------- */
a[href^="tel"]{font-size:1rem}

/* ---------- Smooth momentum scrolling on iOS ---------- */
.tab-bar, .portfolio{-webkit-overflow-scrolling:touch}
</style>
</head>
<body>
<div class="portfolio">

  <!-- ===== HEADER · IMAGE 1 ===== -->
  <div class="profile-header">
    <div class="profile-image-container">
      <img src="https://raw.githubusercontent.com/RAJkumar123887/SUNRUTH_VARMA_PORTFOLIO-/main/SUNRUTH.jpeg" alt="Sunruth Varma profile photo" onerror="this.onerror=null; this.parentElement.innerHTML='<div class=\'img-fallback\'><i class=\'fas fa-user-circle\'></i>IMAGE 1</div>';" />
    </div>
    <div class="header-text">
      <h1>SUNRUTH VARMA</h1>
      <div class="tagline">Child Artist · Hyderabad</div>
      <div class="quick-info">
        <span><i class="fas fa-cake-candles"></i> Age: 15</span>
        <span><i class="fas fa-ruler-vertical"></i> 5 ft</span>
        <span><i class="fas fa-phone-alt"></i> 6301795784</span>
      </div>
    </div>
  </div>

  <!-- ===== TABS ===== -->
  <div class="tab-bar">
    <button class="tab-btn active" data-tab="portfolio"><i class="fas fa-images"></i> Portfolio</button>
    <button class="tab-btn" data-tab="about"><i class="fas fa-user"></i> About</button>
    <button class="tab-btn" data-tab="contact"><i class="fas fa-envelope"></i> Contact Us</button>
  </div>

  <!-- ===== TAB 1: PORTFOLIO ===== -->
  <div class="tab-panel active" id="panel-portfolio">

    <div class="gallery-section">
      <h2><i class="fas fa-camera-retro"></i> Photo Gallery</h2>
      <div class="photo-grid">

        <div class="photo-card">
          <img src="https://raw.githubusercontent.com/RAJkumar123887/SUNRUTH_VARMA_PORTFOLIO-/main/SUNRUTH1.jpeg" alt="Gallery image 2" onerror="this.onerror=null; this.parentElement.innerHTML='<div class=\'img-fallback\'><i class=\'fas fa-image\'></i>IMAGE 2</div>';" />
        </div>

        <div class="photo-card">
          <img src="https://raw.githubusercontent.com/RAJkumar123887/SUNRUTH_VARMA_PORTFOLIO-/main/SUNRUTH2.jpeg" alt="Gallery image 3" onerror="this.onerror=null; this.parentElement.innerHTML='<div class=\'img-fallback\'><i class=\'fas fa-image\'></i>IMAGE 3</div>';" />
        </div>

        <div class="photo-card">
          <img src="https://raw.githubusercontent.com/RAJkumar123887/SUNRUTH_VARMA_PORTFOLIO-/main/SUNRUTH3.jpeg" alt="Gallery image 4" onerror="this.onerror=null; this.parentElement.innerHTML='<div class=\'img-fallback\'><i class=\'fas fa-image\'></i>IMAGE 4</div>';" />
        </div>

        <div class="photo-card">
          <img src="https://raw.githubusercontent.com/RAJkumar123887/SUNRUTH_VARMA_PORTFOLIO-/main/SUNRUTH4.jpeg" alt="Gallery image 5" onerror="this.onerror=null; this.parentElement.innerHTML='<div class=\'img-fallback\'><i class=\'fas fa-image\'></i>IMAGE 5</div>';" />
        </div>

        <div class="photo-card">
          <img src="https://raw.githubusercontent.com/RAJkumar123887/SUNRUTH_VARMA_PORTFOLIO-/main/SUNRUTH5.jpeg" alt="Gallery image 6" onerror="this.onerror=null; this.parentElement.innerHTML='<div class=\'img-fallback\'><i class=\'fas fa-image\'></i>IMAGE 6</div>';" />
        </div>

        <div class="photo-card">
          <img src="https://raw.githubusercontent.com/RAJkumar123887/SUNRUTH_VARMA_PORTFOLIO-/main/SUNRUTH6.jpeg" alt="Gallery image 7" onerror="this.onerror=null; this.parentElement.innerHTML='<div class=\'img-fallback\'><i class=\'fas fa-image\'></i>IMAGE 7</div>';" />
        </div>

      </div>
    </div>

    <div class="details-section">
      <div class="info-card">
        <h3><i class="fas fa-id-card" style="margin-right:.6rem;color:#f7c948"></i>Details</h3>
        <div class="info-list">
          <p><strong>Name:</strong> Sunruth Varma</p>
          <p><strong>Age:</strong> 12 years</p>
          <p><strong>Location:</strong> Hyderabad</p>
          <p><strong>Height:</strong> 5 feet</p>
          <p><strong>Contact:</strong> <a href="tel:6301795784">6301795784</a></p>
          <p><strong>Career start:</strong> 2022</p>
        </div>
        <div style="margin-top:1.8rem;background:#e9f0f7;border-radius:1.2rem;padding:1rem 1.2rem">
          <p style="font-size:.95rem;color:#1e2b3c;display:flex;gap:.6rem">
            <i class="fas fa-star" style="color:#f7c948"></i>
            <span><strong>National Award</strong> for short film <em>Aksharabhyasam</em></span>
          </p>
        </div>
      </div>

      <div class="info-card">
        <h3><i class="fas fa-film" style="margin-right:.6rem;color:#f7c948"></i>Experience</h3>
        <div class="experience-list">

          <div class="exp-item">
            <h4><i class="fas fa-tv"></i> Yedaloyallo Indradanussu</h4>
            <div class="role">Minister's son — Major role <span class="badge">Serial</span></div>
            <div class="video-links">
              <a href="https://www.instagram.com/reel/CrchbGcPqqA" target="_blank" rel="noopener noreferrer"><i class="fas fa-play-circle"></i> Watch reel</a>
            </div>
          </div>

          <div class="exp-item">
            <h4><i class="fas fa-tv"></i> Krishnamukundamurari</h4>
            <div class="role">Child role — treatment & camping <span class="badge">Serial</span></div>
            <div class="video-links">
              <a href="https://www.instagram.com/reel/CwlyuztyXqL/?stkn=MXJqM2l1ZnFxNTJnYw==" target="_blank" rel="noopener noreferrer"><i class="fas fa-play-circle"></i> Watch reel</a>
            </div>
          </div>

          <div class="exp-item">
            <h4><i class="fas fa-tv"></i> Adhaliyalali Indra Dhanasu</h4>
            <div class="role">Heroine's brother — Traditional role <span class="badge">Serial</span></div>
            <div class="video-links">
              <a href="https://www.instagram.com/reel/CzFd54cSL0H/?stkn=MXR4bDJ1bzd1dzF3Mw==" target="_blank" rel="noopener noreferrer"><i class="fas fa-play-circle"></i> Watch reel</a>
            </div>
          </div>

          <div class="exp-item">
            <h4><i class="fas fa-award"></i> Aksharabhyasam <span class="award-tag">🏆 National Award</span></h4>
            <div class="role">Main role — Right to education <span class="badge">Short Film</span></div>
            <div class="video-links">
              <a href="https://youtu.be/GKuE11Y9uTo?si=1IazyNygO4kHs3Zu" target="_blank" rel="noopener noreferrer"><i class="fab fa-youtube"></i> Watch on YouTube</a>
            </div>
          </div>

          <div class="exp-item">
            <h4><i class="fas fa-film"></i> Peddi <span class="badge" style="background:#f7c948;color:#0f1a24">Movie</span></h4>
            <div class="role">Hero beside child artist — Cricket & Kabadi with Ram Charan sir</div>
            <div class="video-links">
              <a href="https://www.instagram.com/reel/DZfDbt0hFSU/?stkn=MTRzM2t0dXB3NWo1OA==" target="_blank" rel="noopener noreferrer"><i class="fas fa-play-circle"></i> Reel 1</a>
              <a href="https://www.instagram.com/reel/DZPzLjrhw18/?stkn=MTQzejBpdTIzNWI0dg==" target="_blank" rel="noopener noreferrer"><i class="fas fa-play-circle"></i> Reel 2</a>
            </div>
          </div>

        </div>
      </div>
    </div>
  </div>

  <!-- ===== TAB 2: ABOUT ===== -->
  <div class="tab-panel" id="panel-about">
    <div class="about-content">
      <h2><i class="fas fa-user-circle"></i> About Sunruth Varma</h2>
      <div class="about-card">
        <p><span class="quote-mark"><i class="fas fa-quote-left"></i></span> I started my career as a <strong>child actor in serials</strong>. My first serial was <em>Yedaloyallo Indradanussu</em>, where I played a <span class="highlight">major role</span> as a <strong>Minister's son</strong>.</p>
        <p>Then I worked in <em>Krishnamukundamurari</em> as a child artist, which gave me a <strong>good role and responsibility</strong> with a wonderful bond on set.</p>
        <p>I then worked for <em>Adhaliyalali Indra Dhanasu</em>, playing the <span class="highlight">heroine's brother</span> in a traditional manner — a major name in that serial.</p>
        <p>After that, the short film <em>Aksharabhyasam</em> earned me a <strong>National Award</strong> 🏆. The film spreads the message of the <span class="highlight">Right to Education</span> — every child has the right to study with dignity.</p>
        <p>Then I worked with <strong>Ram Charan sir</strong> in <em>Peddi</em> in <span class="highlight">cricket and kabadi sequences</span>. It was a major role with a great bond. I have also signed upcoming projects.</p>
        <p style="margin-top:1.5rem;font-weight:600;color:#0f1a24;text-align:right">— Thank you! 🙏</p>
      </div>
    </div>
  </div>

  <!-- ===== TAB 3: CONTACT ===== -->
  <div class="tab-panel" id="panel-contact">
    <div class="contact-content">
      <h2><i class="fas fa-address-book"></i> Contact Us</h2>
      <div class="contact-card">
        <div class="contact-row">
          <div class="contact-icon"><i class="fas fa-user"></i></div>
          <div class="contact-detail"><div class="label">Name</div><div class="value">Sunruth Varma</div></div>
        </div>
        <div class="contact-row">
          <div class="contact-icon"><i class="fas fa-phone-alt"></i></div>
          <div class="contact-detail"><div class="label">Phone</div><div class="value"><a href="tel:6301795784">6301795784</a></div></div>
        </div>
        <div class="contact-row">
          <div class="contact-icon"><i class="fas fa-map-marker-alt"></i></div>
          <div class="contact-detail"><div class="label">Location</div><div class="value">Hyderabad, India</div></div>
        </div>
        <div class="contact-row">
          <div class="contact-icon"><i class="fas fa-briefcase"></i></div>
          <div class="contact-detail"><div class="label">Profession</div><div class="value">Child Artist (Film & Television)</div></div>
        </div>
      </div>
      <div class="contact-note"><i class="fas fa-info-circle"></i> For casting inquiries, collaborations, or media requests, please reach out via the phone number above.</div>
    </div>
  </div>

</div>

<script>
(function(){
  const btns = document.querySelectorAll('.tab-btn');
  const panels = {
    portfolio: document.getElementById('panel-portfolio'),
    about: document.getElementById('panel-about'),
    contact: document.getElementById('panel-contact')
  };
  btns.forEach(b=>b.addEventListener('click',function(e){
    e.preventDefault();
    const t = this.dataset.tab;
    btns.forEach(x=>x.classList.toggle('active', x.dataset.tab===t));
    Object.keys(panels).forEach(k=>panels[k].classList.toggle('active', k===t));
  }));
})();
</script>
</body>
</html>
