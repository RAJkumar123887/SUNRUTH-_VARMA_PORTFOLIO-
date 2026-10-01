<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover" />
<meta name="theme-color" content="#0f1a24" />
<title>Sunruth Varma · Child Artist Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet" />
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
<style>
/* ============ RESET ============ */
*{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent}
html{-webkit-text-size-adjust:100%}
body{
  font-family:'Inter',-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,sans-serif;
  background:#eef2f8;color:#1e2b3c;line-height:1.5;
  min-height:100vh;
}

/* ============ DESKTOP BASE ============ */
body{display:flex;justify-content:center;padding:2rem 1rem}
.portfolio{max-width:1200px;width:100%;background:#fff;border-radius:2.5rem;box-shadow:0 30px 50px -20px rgba(0,20,30,.25);overflow:hidden}

.profile-header{display:flex;align-items:center;gap:2rem;background:linear-gradient(145deg,#0f1a24,#1e2b3c);padding:2rem 2.8rem;color:#fff;flex-wrap:wrap}
.profile-image-container{flex-shrink:0;width:140px;height:140px;border-radius:50%;border:5px solid #f7c948;box-shadow:0 10px 20px rgba(0,0,0,.35);overflow:hidden;background:#2e3f52;display:flex;align-items:center;justify-content:center}
.profile-image-container img{width:100%;height:100%;object-fit:cover;display:block}
.header-text{flex:1}
.header-text h1{font-size:2.7rem;font-weight:700;letter-spacing:-.5px;margin-bottom:.25rem;color:#f7c948;text-shadow:0 2px 5px rgba(0,0,0,.3)}
.header-text .tagline{font-size:1.2rem;opacity:.9;margin-bottom:1rem;border-left:4px solid #f7c948;padding-left:1rem}
.quick-info{display:flex;flex-wrap:wrap;gap:1.8rem;font-size:1rem;background:rgba(255,255,255,.08);padding:.8rem 1.8rem;border-radius:60px;backdrop-filter:blur(8px);border:1px solid rgba(255,255,255,.1)}
.quick-info span{display:flex;align-items:center;gap:.5rem}
.quick-info i{color:#f7c948;font-size:1.1rem}

.tab-bar{display:flex;flex-wrap:wrap;gap:.5rem;padding:1.5rem 2.8rem 0 2.8rem;background:#fff;border-bottom:2px solid #e6edf5}
.tab-btn{background:transparent;border:none;padding:.9rem 1.6rem;font-size:1rem;font-weight:600;font-family:inherit;color:#5c6f82;cursor:pointer;border-radius:1rem 1rem 0 0;transition:.2s;display:inline-flex;align-items:center;gap:.5rem;position:relative;top:2px}
.tab-btn.active{color:#0f1a24;background:#f2f8ff;border-bottom:3px solid #f7c948;font-weight:700}
.tab-btn.active i{color:#f7c948}

.tab-panel{display:none;padding:2rem 2.8rem 2.8rem 2.8rem;animation:fadeIn .25s ease}
.tab-panel.active{display:block}
@keyframes fadeIn{from{opacity:0;transform:translateY(6px)}to{opacity:1;transform:translateY(0)}}

.gallery-section h2{font-size:1.7rem;font-weight:700;color:#0f1a24;margin-bottom:1.5rem;display:flex;align-items:center;gap:.8rem}
.gallery-section h2 i{color:#f7c948;font-size:1.8rem}
.photo-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));gap:1.3rem}
.photo-card{background:#eef2f7;border-radius:1.6rem;overflow:hidden;box-shadow:0 8px 16px -6px rgba(0,0,0,.1);aspect-ratio:1/1;display:flex;align-items:center;justify-content:center;border:3px solid #fff;outline:1px solid #dbe4ed}
.photo-card img{width:100%;height:100%;object-fit:cover;display:block}
.img-fallback{background:#d9e2ec;display:flex;align-items:center;justify-content:center;color:#2e3f52;font-weight:600;font-size:1rem;text-align:center;padding:.5rem;width:100%;height:100%;flex-direction:column;gap:.3rem}
.img-fallback i{font-size:2rem;opacity:.6}

.details-section{display:grid;grid-template-columns:1fr 2fr;gap:2rem}
.info-card{background:#f8fbfe;border-radius:2rem;padding:2rem 1.8rem;border:1px solid #e6edf5}
.info-card h3{font-size:1.4rem;font-weight:700;color:#0f1a24;margin-bottom:1.5rem;border-bottom:4px solid #f7c948;display:inline-block;padding-bottom:.4rem}
.info-list p{margin-bottom:.9rem;font-size:1.05rem;color:#2e3f52;display:flex;align-items:baseline;flex-wrap:wrap}
.info-list strong{width:110px;display:inline-block;font-weight:700;color:#0f1a24}
.info-list a{color:#0f1a24;text-decoration:none;font-weight:600;background:#f7c948;padding:.2rem 1rem;border-radius:40px;font-size:.95rem;display:inline-block}

.experience-list{display:flex;flex-direction:column;gap:1.4rem}
.exp-item{background:#fff;border-radius:1.6rem;padding:1.4rem 1.8rem;border-left:6px solid #f7c948;border:1px solid #e6edf5;border-left-width:6px}
.exp-item h4{font-size:1.2rem;font-weight:700;color:#0f1a24;margin-bottom:.25rem;display:flex;align-items:center;gap:.5rem;flex-wrap:wrap}
.exp-item h4 i{color:#f7c948;font-size:1rem}
.exp-item .role{font-weight:600;color:#1e5c8b;margin-bottom:.5rem;font-size:1rem;display:flex;flex-wrap:wrap;align-items:center;gap:.5rem}
.exp-item .role .badge{background:#e3eef9;padding:.2rem 1rem;border-radius:50px;font-size:.75rem;font-weight:700;text-transform:uppercase;color:#0f1a24}
.exp-item .video-links{display:flex;flex-wrap:wrap;gap:.8rem;margin-top:.7rem}
.exp-item .video-links a{color:#0f1a24;text-decoration:none;background:#eef2f7;padding:.35rem 1.2rem;border-radius:40px;font-size:.88rem;font-weight:600;display:inline-flex;align-items:center;gap:.4rem;border:1px solid #d0dfee}
.exp-item .video-links a i{color:#f7c948;font-size:.9rem}
.award-tag{background:#f7c948;color:#0f1a24;font-weight:700;font-size:.8rem;padding:.25rem 1rem;border-radius:40px;display:inline-block;margin-left:.6rem}

.about-content{max-width:900px;margin:0 auto}
.about-content h2{font-size:1.9rem;font-weight:700;color:#0f1a24;margin-bottom:1.5rem;display:flex;align-items:center;gap:.8rem}
.about-content h2 i{color:#f7c948;font-size:2rem}
.about-card{background:#f8fbfe;border-radius:2rem;padding:2rem 2.2rem;border:1px solid #e6edf5;line-height:1.8;font-size:1.05rem;color:#2e3f52}
.about-card p{margin-bottom:1.2rem}
.about-card .highlight{background:#fff6d9;padding:.15rem .6rem;border-radius:30px;font-weight:600;color:#0f1a24;display:inline-block}
.about-card .quote-mark{color:#f7c948;font-size:1.4rem;margin-right:.4rem;vertical-align:middle;opacity:.8}

.contact-content{max-width:700px;margin:0 auto}
.contact-content h2{font-size:1.9rem;font-weight:700;color:#0f1a24;margin-bottom:1.5rem;display:flex;align-items:center;gap:.8rem}
.contact-content h2 i{color:#f7c948;font-size:2rem}
.contact-card{background:linear-gradient(145deg,#0f1a24,#1e2b3c);border-radius:2rem;padding:2.5rem 2.2rem;color:#fff}
.contact-card .contact-row{display:flex;align-items:center;gap:1.2rem;padding:1.2rem 0;border-bottom:1px solid rgba(255,255,255,.1);flex-wrap:wrap}
.contact-card .contact-row:last-child{border-bottom:none}
.contact-card .contact-icon{width:52px;height:52px;background:rgba(247,201,72,.15);border-radius:50%;display:flex;align-items:center;justify-content:center;flex-shrink:0;border:1px solid rgba(247,201,72,.3)}
.contact-card .contact-icon i{font-size:1.4rem;color:#f7c948}
.contact-card .contact-detail{flex:1}
.contact-card .contact-detail .label{font-size:.85rem;text-transform:uppercase;letter-spacing:1px;opacity:.7;margin-bottom:.2rem;font-weight:500}
.contact-card .contact-detail .value{font-size:1.25rem;font-weight:600;color:#fff;word-break:break-word}
.contact-card .contact-detail .value a{color:#f7c948;text-decoration:none;border-bottom:2px dotted rgba(247,201,72,.5)}
.contact-note{margin-top:1.8rem;background:#f2f8ff;border-radius:1.4rem;padding:1.2rem 1.6rem;font-size:.95rem;color:#2e3f52;border:1px dashed #b8cee4;text-align:center}

/* ==================================================================
   MOBILE — CUSTOM FORMAT, FULLY CENTERED
   ================================================================== */
@media (max-width: 820px) {

  body{
    display:block;
    padding:0;
    background:#eef2f8;
    padding-bottom:calc(70px + env(safe-area-inset-bottom, 0px));
  }

  .portfolio{
    max-width:100%;
    border-radius:0;
    box-shadow:none;
    background:#eef2f8;
    overflow:visible;
  }

  /* ============== HEADER ============== */
  .profile-header{
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:1.75rem 1rem 1.5rem;
    padding-top:calc(1.75rem + env(safe-area-inset-top, 0px));
    gap:.85rem;
    background:linear-gradient(160deg,#0f1a24 0%,#1b2a3d 60%,#263a52 100%);
    border-radius:0 0 26px 26px;
    box-shadow:0 6px 22px -8px rgba(0,20,30,.35);
  }
  .profile-image-container{
    width:112px;height:112px;
    border:4px solid #f7c948;
    margin:0 auto;
    box-shadow:0 12px 24px rgba(0,0,0,.35);
  }
  .header-text{width:100%;text-align:center}
  .header-text h1{font-size:1.65rem;line-height:1.2;margin-bottom:.2rem;text-align:center}
  .header-text .tagline{
    border-left:none;
    padding-left:0;
    font-size:.88rem;
    margin-bottom:.85rem;
    text-align:center;
    opacity:.85;
  }
  .quick-info{
    display:flex;
    flex-wrap:wrap;
    justify-content:center;
    gap:.35rem .5rem;
    padding:.55rem .85rem;
    border-radius:40px;
    background:rgba(255,255,255,.1);
    border:1px solid rgba(255,255,255,.15);
    width:100%;
    max-width:340px;
    margin:0 auto;
  }
  .quick-info span{
    font-size:.75rem;
    font-weight:600;
    gap:.3rem;
    white-space:nowrap;
    color:#fff;
    display:inline-flex;
    align-items:center;
    padding:.15rem .3rem;
  }
  .quick-info i{font-size:.85rem}

  /* ============== TABS — Pill segmented control ============== */
  .tab-bar{
    position:sticky;
    top:0;
    z-index:100;
    display:flex;
    flex-wrap:nowrap;
    justify-content:center;
    gap:.35rem;
    padding:.65rem .75rem;
    background:rgba(255,255,255,.96);
    backdrop-filter:blur(20px);
    -webkit-backdrop-filter:blur(20px);
    border-bottom:1px solid #e6edf5;
    box-shadow:0 2px 12px rgba(0,0,0,.05);
  }
  .tab-btn{
    flex:1;
    min-width:0;
    justify-content:center;
    padding:.7rem .35rem;
    font-size:.82rem;
    border-radius:50px;
    top:0;
    background:transparent;
    border-bottom:none;
    color:#5c6f82;
    font-weight:600;
    transition:all .2s;
  }
  .tab-btn i{font-size:.92rem}
  .tab-btn.active{
    background:#0f1a24;
    color:#fff;
    border-bottom:none;
    font-weight:700;
    box-shadow:0 4px 12px rgba(15,26,36,.25);
  }
  .tab-btn.active i{color:#f7c948}

  /* ============== PANELS ============== */
  .tab-panel{
    padding:1.35rem 1rem 1.75rem;
  }

  /* ============== PORTFOLIO — GALLERY ============== */
  .gallery-section h2{
    font-size:1.15rem;
    justify-content:center;
    text-align:center;
    gap:.5rem;
    margin-bottom:1rem;
    display:flex;
  }
  .gallery-section h2 i{font-size:1.25rem}

  .photo-grid{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:.75rem;
    justify-items:center;
  }
  .photo-card{
    width:100%;
    border-radius:16px;
    border-width:0;
    outline:none;
    box-shadow:0 4px 12px rgba(0,20,30,.08);
    aspect-ratio:1/1;
  }
  .photo-card img{border-radius:16px}

  /* ============== PORTFOLIO — DETAILS ============== */
  .details-section{
    display:flex;
    flex-direction:column;
    gap:1rem;
    margin-top:1.5rem;
  }
  .info-card{
    width:100%;
    padding:1.25rem 1.1rem;
    border-radius:18px;
    background:#fff;
    border:1px solid #eaeff6;
    box-shadow:0 4px 14px rgba(0,20,30,.05);
    text-align:center;
  }
  .info-card h3{
    display:block;
    text-align:center;
    font-size:1.05rem;
    font-weight:700;
    margin:0 auto 1rem auto;
    padding-bottom:.45rem;
    border-bottom:3px solid #f7c948;
    width:fit-content;
    min-width:110px;
  }
  .info-list{
    display:flex;
    flex-direction:column;
    gap:0;
  }
  .info-list p{
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    text-align:center;
    gap:.15rem;
    margin-bottom:0;
    padding:.75rem 0;
    font-size:.92rem;
    border-bottom:1px solid #eef2f8;
    color:#1e2b3c;
    line-height:1.4;
  }
  .info-list p:last-child{border-bottom:none}
  .info-list strong{
    width:auto;
    display:block;
    font-size:.68rem;
    font-weight:700;
    color:#8a9bb0;
    text-transform:uppercase;
    letter-spacing:.7px;
    text-align:center;
    margin-bottom:.1rem;
  }
  .info-list a{
    font-size:.82rem;
    font-weight:700;
    padding:.35rem 1.1rem;
    background:#f7c948;
    color:#0f1a24;
    border-radius:40px;
    display:inline-block;
    margin-top:.3rem;
    box-shadow:0 2px 6px rgba(247,201,72,.35);
  }

  /* ============== PORTFOLIO — EXPERIENCE ============== */
  .experience-list{gap:.85rem}
  .exp-item{
    padding:1.05rem 1.1rem;
    border-radius:16px;
    border:1px solid #eaeff6;
    border-left:none;
    border-top:4px solid #f7c948;
    background:#fff;
    box-shadow:0 4px 12px rgba(0,20,30,.04);
    text-align:center;
  }
  .exp-item h4{
    font-size:.98rem;
    justify-content:center;
    text-align:center;
    gap:.4rem;
    margin-bottom:.35rem;
    line-height:1.3;
  }
  .exp-item h4 i{font-size:.9rem}
  .exp-item .role{
    font-size:.83rem;
    justify-content:center;
    text-align:center;
    margin-bottom:.6rem;
    color:#1e5c8b;
    gap:.4rem;
    line-height:1.45;
    display:flex;
    flex-wrap:wrap;
  }
  .exp-item .role .badge{
    font-size:.62rem;
    padding:.15rem .7rem;
  }
  .exp-item .video-links{
    justify-content:center;
    gap:.5rem;
    margin-top:.5rem;
  }
  .exp-item .video-links a{
    font-size:.78rem;
    padding:.45rem 1rem;
    border-radius:40px;
    background:#f2f6fb;
    border:1px solid #dde6f0;
    font-weight:600;
  }
  .exp-item .video-links a i{font-size:.82rem}
  .award-tag{
    font-size:.68rem;
    padding:.18rem .75rem;
    margin-left:.35rem;
  }

  /* ============== ABOUT — Custom format ============== */
  .about-content{max-width:100%;margin:0}
  .about-content h2{
    font-size:1.2rem;
    justify-content:center;
    text-align:center;
    gap:.5rem;
    margin-bottom:1.1rem;
  }
  .about-content h2 i{font-size:1.35rem}

  /* Intro card with avatar */
  .about-intro{
    display:flex;
    flex-direction:column;
    align-items:center;
    text-align:center;
    padding:1.4rem 1.1rem;
    background:linear-gradient(160deg,#0f1a24 0%,#1e2b3c 100%);
    border-radius:20px;
    color:#fff;
    margin-bottom:1.1rem;
    box-shadow:0 8px 20px -8px rgba(0,20,30,.35);
  }
  .about-intro .about-icon{
    width:64px;height:64px;
    border-radius:50%;
    background:rgba(247,201,72,.15);
    border:2px solid #f7c948;
    display:flex;
    align-items:center;
    justify-content:center;
    margin-bottom:.75rem;
  }
  .about-intro .about-icon i{font-size:1.6rem;color:#f7c948}
  .about-intro h3{
    font-size:1.05rem;
    font-weight:700;
    color:#f7c948;
    margin-bottom:.35rem;
  }
  .about-intro p{
    font-size:.85rem;
    color:rgba(255,255,255,.85);
    line-height:1.55;
  }

  /* Paragraph cards */
  .about-card{
    padding:0;
    border:none;
    background:transparent;
    box-shadow:none;
    text-align:left;
    font-size:.9rem;
  }
  .about-para{
    background:#fff;
    border-radius:16px;
    padding:1.15rem 1.1rem;
    margin-bottom:.75rem;
    border:1px solid #eaeff6;
    box-shadow:0 3px 12px rgba(0,20,30,.04);
    line-height:1.65;
    color:#2e3f52;
    position:relative;
    text-align:left;
  }
  .about-para::before{
    content:"";
    position:absolute;
    top:1.05rem;
    left:1.1rem;
    width:22px;height:3px;
    background:#f7c948;
    border-radius:3px;
  }
  .about-para{
    padding-top:1.75rem;
  }
  .about-para strong{color:#0f1a24}
  .about-para em{color:#1e5c8b;font-style:italic}
  .about-para .highlight{
    background:#fff6d9;
    padding:.1rem .5rem;
    border-radius:20px;
    font-weight:600;
    color:#0f1a24;
    display:inline-block;
    font-size:.85rem;
  }
  .about-para .quote-mark{
    color:#f7c948;
    font-size:1.05rem;
    margin-right:.25rem;
    vertical-align:middle;
    opacity:.9;
  }

  /* Signature */
  .about-sign{
    display:flex;
    align-items:center;
    justify-content:center;
    gap:.55rem;
    padding:1.1rem;
    background:linear-gradient(135deg,#f7c948 0%,#f5d97a 100%);
    border-radius:16px;
    margin-top:.4rem;
    font-weight:700;
    color:#0f1a24;
    font-size:.95rem;
    box-shadow:0 6px 16px -6px rgba(247,201,72,.5);
  }
  .about-sign i{font-size:1.05rem}

  /* ============== CONTACT — Custom format ============== */
  .contact-content{max-width:100%;margin:0}
  .contact-content h2{
    font-size:1.2rem;
    justify-content:center;
    text-align:center;
    gap:.5rem;
    margin-bottom:1.1rem;
  }
  .contact-content h2 i{font-size:1.35rem}

  /* Big "Call Now" CTA card */
  .contact-cta{
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    text-align:center;
    background:linear-gradient(160deg,#0f1a24 0%,#1e2b3c 100%);
    border-radius:22px;
    padding:1.8rem 1.2rem 1.6rem;
    color:#fff;
    margin-bottom:1.1rem;
    box-shadow:0 12px 30px -10px rgba(0,20,30,.4);
    position:relative;
    overflow:hidden;
  }
  .contact-cta::before{
    content:"";
    position:absolute;
    top:-40px;right:-40px;
    width:140px;height:140px;
    border-radius:50%;
    background:radial-gradient(circle,rgba(247,201,72,.18) 0%,transparent 70%);
  }
  .contact-cta-avatar{
    width:70px;height:70px;
    border-radius:50%;
    background:rgba(247,201,72,.15);
    border:2px solid #f7c948;
    display:flex;
    align-items:center;
    justify-content:center;
    margin-bottom:.85rem;
    position:relative;
    z-index:1;
  }
  .contact-cta-avatar i{font-size:1.7rem;color:#f7c948}
  .contact-cta h3{
    font-size:1.15rem;
    font-weight:700;
    color:#fff;
    margin-bottom:.2rem;
    position:relative;
    z-index:1;
  }
  .contact-cta p{
    font-size:.82rem;
    color:rgba(255,255,255,.7);
    margin-bottom:1.1rem;
    position:relative;
    z-index:1;
  }
  .contact-cta .call-btn{
    display:inline-flex;
    align-items:center;
    gap:.5rem;
    background:#f7c948;
    color:#0f1a24;
    font-weight:700;
    padding:.75rem 1.6rem;
    border-radius:50px;
    text-decoration:none;
    font-size:.92rem;
    box-shadow:0 8px 20px -6px rgba(247,201,72,.6);
    transition:transform .15s;
    position:relative;
    z-index:1;
  }
  .contact-cta .call-btn:active{transform:scale(.96)}
  .contact-cta .call-btn i{font-size:1rem}

  /* Info list */
  .contact-info-list{
    display:flex;
    flex-direction:column;
    gap:.7rem;
  }
  .contact-info-row{
    display:flex;
    align-items:center;
    gap:.9rem;
    padding:1rem 1.1rem;
    background:#fff;
    border-radius:16px;
    border:1px solid #eaeff6;
    box-shadow:0 3px 12px rgba(0,20,30,.04);
    text-align:left;
  }
  .contact-info-icon{
    width:42px;height:42px;
    border-radius:12px;
    background:rgba(247,201,72,.15);
    border:1px solid rgba(247,201,72,.4);
    display:flex;
    align-items:center;
    justify-content:center;
    flex-shrink:0;
  }
  .contact-info-icon i{font-size:1.05rem;color:#b98d0d}
  .contact-info-text{flex:1;min-width:0}
  .contact-info-text .label{
    font-size:.65rem;
    font-weight:700;
    color:#8a9bb0;
    letter-spacing:.7px;
    text-transform:uppercase;
    margin-bottom:.15rem;
  }
  .contact-info-text .value{
    font-size:.95rem;
    font-weight:700;
    color:#0f1a24;
    word-break:break-word;
  }

  .contact-note{
    margin-top:1.1rem;
    padding:1rem 1.1rem;
    font-size:.85rem;
    border-radius:14px;
    background:#fff;
    border:1px dashed #b8cee4;
    line-height:1.6;
    text-align:center;
    color:#2e3f52;
  }
  .contact-note i{color:#f7c948;margin-right:.35rem}
}

/* ============ SMALL PHONES ============ */
@media (max-width: 380px) {
  .header-text h1{font-size:1.4rem}
  .profile-image-container{width:96px;height:96px}
  .quick-info span{font-size:.68rem}
  .tab-btn{font-size:.76rem;padding:.6rem .3rem}
  .tab-btn i{font-size:.85rem}
  .gallery-section h2{font-size:1.05rem}
  .photo-grid{gap:.6rem}
  .photo-card{border-radius:14px}
  .photo-card img{border-radius:14px}
  .info-card{padding:1.1rem .9rem}
  .exp-item{padding:.95rem .9rem}
  .about-para{padding:.95rem .95rem;padding-top:1.6rem;font-size:.87rem}
  .contact-cta{padding:1.5rem 1rem 1.3rem}
  .contact-cta h3{font-size:1.05rem}
}

/* ============ iPAD ============ */
@media (min-width: 821px) and (max-width: 1024px) {
  .portfolio{border-radius:2rem}
  .profile-header{padding:2rem}
  .tab-panel{padding:1.75rem 2rem 2.25rem}
  .info-card{padding:1.75rem 1.5rem}
  .profile-image-container{width:130px;height:130px}
  .header-text h1{font-size:2.3rem}
}
</style>
</head>
<body>
<div class="portfolio">

  <!-- ===== HEADER ===== -->
  <div class="profile-header">
    <div class="profile-image-container">
      <img src="https://raw.githubusercontent.com/RAJkumar123887/SUNRUTH_VARMA_PORTFOLIO-/main/SUNRUTH.jpeg" alt="Sunruth Varma profile photo" onerror="this.onerror=null; this.parentElement.innerHTML='<div class=\'img-fallback\'><i class=\'fas fa-user-circle\'></i>IMAGE 1</div>';" />
    </div>
    <div class="header-text">
      <h1>SUNRUTH VARMA</h1>
      <div class="tagline">Child Artist · Hyderabad</div>
      <div class="quick-info">
        <span><i class="fas fa-cake-candles"></i> 12 years</span>
        <span><i class="fas fa-ruler-vertical"></i> 5 ft</span>
        <span><i class="fas fa-phone-alt"></i> 6301795784</span>
      </div>
    </div>
  </div>

  <!-- ===== TABS (pill segmented on mobile) ===== -->
  <div class="tab-bar">
    <button class="tab-btn active" data-tab="portfolio"><i class="fas fa-images"></i> Portfolio</button>
    <button class="tab-btn" data-tab="about"><i class="fas fa-user"></i> About</button>
    <button class="tab-btn" data-tab="contact"><i class="fas fa-envelope"></i> Contact</button>
  </div>

  <!-- ===== TAB 1: PORTFOLIO ===== -->
  <div class="tab-panel active" id="panel-portfolio">

    <div class="gallery-section">
      <h2><i class="fas fa-camera-retro"></i> Photo Gallery</h2>
      <div class="photo-grid">
        <div class="photo-card">
          <img src="https://raw.githubusercontent.com/RAJkumar123887/SUNRUTH_VARMA_PORTFOLIO-/main/SUNRUTH1.jpeg" alt="Gallery 2" onerror="this.onerror=null; this.parentElement.innerHTML='<div class=\'img-fallback\'><i class=\'fas fa-image\'></i>IMAGE 2</div>';" />
        </div>
        <div class="photo-card">
          <img src="https://raw.githubusercontent.com/RAJkumar123887/SUNRUTH_VARMA_PORTFOLIO-/main/SUNRUTH2.jpeg" alt="Gallery 3" onerror="this.onerror=null; this.parentElement.innerHTML='<div class=\'img-fallback\'><i class=\'fas fa-image\'></i>IMAGE 3</div>';" />
        </div>
        <div class="photo-card">
          <img src="https://raw.githubusercontent.com/RAJkumar123887/SUNRUTH_VARMA_PORTFOLIO-/main/SUNRUTH3.jpeg" alt="Gallery 4" onerror="this.onerror=null; this.parentElement.innerHTML='<div class=\'img-fallback\'><i class=\'fas fa-image\'></i>IMAGE 4</div>';" />
        </div>
        <div class="photo-card">
          <img src="https://raw.githubusercontent.com/RAJkumar123887/SUNRUTH_VARMA_PORTFOLIO-/main/SUNRUTH4.jpeg" alt="Gallery 5" onerror="this.onerror=null; this.parentElement.innerHTML='<div class=\'img-fallback\'><i class=\'fas fa-image\'></i>IMAGE 5</div>';" />
        </div>
        <div class="photo-card">
          <img src="https://raw.githubusercontent.com/RAJkumar123887/SUNRUTH_VARMA_PORTFOLIO-/main/SUNRUTH5.jpeg" alt="Gallery 6" onerror="this.onerror=null; this.parentElement.innerHTML='<div class=\'img-fallback\'><i class=\'fas fa-image\'></i>IMAGE 6</div>';" />
        </div>
        <div class="photo-card">
          <img src="https://raw.githubusercontent.com/RAJkumar123887/SUNRUTH_VARMA_PORTFOLIO-/main/SUNRUTH6.jpeg" alt="Gallery 7" onerror="this.onerror=null; this.parentElement.innerHTML='<div class=\'img-fallback\'><i class=\'fas fa-image\'></i>IMAGE 7</div>';" />
        </div>
      </div>
    </div>

    <div class="details-section">
      <div class="info-card">
        <h3><i class="fas fa-id-card" style="margin-right:.4rem;color:#f7c948"></i>Details</h3>
        <div class="info-list">
          <p><strong>Name</strong> <span>Sunruth Varma</span></p>
          <p><strong>Age</strong> <span>12 years</span></p>
          <p><strong>Location</strong> <span>Hyderabad</span></p>
          <p><strong>Height</strong> <span>5 feet</span></p>
          <p><strong>Contact</strong> <a href="tel:6301795784">Call Now</a></p>
          <p><strong>Started</strong> <span>2022</span></p>
        </div>
        <div style="margin-top:1.2rem;background:#fff8e6;border-radius:14px;padding:.85rem 1rem;border:1px solid #f7e6b0">
          <p style="font-size:.86rem;color:#0f1a24;display:flex;gap:.5rem;align-items:center;justify-content:center;text-align:center;flex-wrap:wrap">
            <i class="fas fa-star" style="color:#f7c948"></i>
            <span><strong>National Award</strong> for <em>Aksharabhyasam</em></span>
          </p>
        </div>
      </div>

      <div class="info-card">
        <h3><i class="fas fa-film" style="margin-right:.4rem;color:#f7c948"></i>Experience</h3>
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
            <h4><i class="fas fa-award"></i> Aksharabhyasam <span class="award-tag">🏆 Award</span></h4>
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

  <!-- ===== TAB 2: ABOUT (CUSTOM FORMAT) ===== -->
  <div class="tab-panel" id="panel-about">
    <div class="about-content">
      <h2><i class="fas fa-user-circle"></i> About Sunruth</h2>

      <!-- Intro card (mobile style) -->
      <div class="about-intro" style="display:none" id="aboutIntroMobile">
        <div class="about-icon"><i class="fas fa-star"></i></div>
        <h3>Sunruth Varma</h3>
        <p>Child artist from Hyderabad — acting in serials, short films, and movies since 2022.</p>
      </div>

      <div class="about-card">
        <div class="about-para">
          <span class="quote-mark"><i class="fas fa-quote-left"></i></span>
          I started my career as a <strong>child actor in serials</strong>. My first serial was
          <em>Yedaloyallo Indradanussu</em>, where I played a <span class="highlight">major role</span>
          as a <strong>Minister's son</strong>.
        </div>

        <div class="about-para">
          Then I worked in <em>Krishnamukundamurari</em> as a child artist, which gave me a
          <strong>good role and responsibility</strong> with a wonderful bond on set.
        </div>

        <div class="about-para">
          I then worked for <em>Adhaliyalali Indra Dhanasu</em>, playing the
          <span class="highlight">heroine's brother</span> in a traditional manner — a major name in that serial.
        </div>

        <div class="about-para">
          After that, the short film <em>Aksharabhyasam</em> earned me a
          <strong>National Award</strong> 🏆. The film spreads the message of the
          <span class="highlight">Right to Education</span> — every child has the right to study with dignity.
        </div>

        <div class="about-para">
          Then I worked with <strong>Ram Charan sir</strong> in <em>Peddi</em> in
          <span class="highlight">cricket and kabadi sequences</span>. It was a major role with a great bond.
          I have also signed upcoming projects.
        </div>

        <div class="about-sign">
          <i class="fas fa-heart"></i> Thank you! 🙏
        </div>
      </div>
    </div>
  </div>

  <!-- ===== TAB 3: CONTACT (CUSTOM FORMAT) ===== -->
  <div class="tab-panel" id="panel-contact">
    <div class="contact-content">
      <h2><i class="fas fa-address-book"></i> Contact</h2>

      <!-- CTA card (mobile style) -->
      <div class="contact-cta" style="display:none" id="contactCtaMobile">
        <div class="contact-cta-avatar"><i class="fas fa-user"></i></div>
        <h3>Sunruth Varma</h3>
        <p>Child Artist · Hyderabad, India</p>
        <a href="tel:6301795784" class="call-btn">
          <i class="fas fa-phone-alt"></i> Call Now
        </a>
      </div>

      <!-- Info list -->
      <div class="contact-info-list" style="display:none" id="contactListMobile">
        <div class="contact-info-row">
          <div class="contact-info-icon"><i class="fas fa-user"></i></div>
          <div class="contact-info-text">
            <div class="label">Name</div>
            <div class="value">Sunruth Varma</div>
          </div>
        </div>
        <div class="contact-info-row">
          <div class="contact-info-icon"><i class="fas fa-phone-alt"></i></div>
          <div class="contact-info-text">
            <div class="label">Phone</div>
            <div class="value">6301795784</div>
          </div>
        </div>
        <div class="contact-info-row">
          <div class="contact-info-icon"><i class="fas fa-map-marker-alt"></i></div>
          <div class="contact-info-text">
            <div class="label">Location</div>
            <div class="value">Hyderabad, India</div>
          </div>
        </div>
        <div class="contact-info-row">
          <div class="contact-info-icon"><i class="fas fa-briefcase"></i></div>
          <div class="contact-info-text">
            <div class="label">Profession</div>
            <div class="value">Child Artist</div>
          </div>
        </div>
      </div>

      <!-- Desktop contact card (unchanged) -->
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
          <div class="contact-detail"><div class="label">Profession</div><div class="value">Child Artist</div></div>
        </div>
      </div>

      <div class="contact-note"><i class="fas fa-info-circle"></i> For casting inquiries, collaborations, or media requests, please reach out via phone.</div>
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

  function switchTab(t){
    btns.forEach(x=>x.classList.toggle('active', x.dataset.tab===t));
    Object.keys(panels).forEach(k=>panels[k].classList.toggle('active', k===t));
    if (window.innerWidth <= 820) {
      window.scrollTo({top:0, behavior:'smooth'});
    }
  }

  btns.forEach(b=>b.addEventListener('click',function(e){
    e.preventDefault();
    switchTab(this.dataset.tab);
  }));

  /* Toggle mobile/desktop about & contact blocks */
  function applyMobileLayout(){
    const isMobile = window.innerWidth <= 820;

    // About
    document.getElementById('aboutIntroMobile').style.display = isMobile ? 'flex' : 'none';

    // Contact
    document.getElementById('contactCtaMobile').style.display  = isMobile ? 'flex' : 'none';
    document.getElementById('contactListMobile').style.display = isMobile ? 'flex' : 'none';
    document.querySelector('#panel-contact .contact-card').style.display = isMobile ? 'none' : 'flex';
  }

  applyMobileLayout();
  window.addEventListener('resize', applyMobileLayout);
  window.addEventListener('orientationchange', () => setTimeout(applyMobileLayout, 100));
})();
</script>
</body>
</html>
