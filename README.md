
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>B2B Sales Portfolio — 헥토파이낸셜 모바일쿠폰 영업 지원</title>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700;900&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
/* ═══════════════════════════════════════
   헥토파이낸셜 브랜드 컬러 시스템
   Primary  : #FF6B00  (헥토 오렌지 — 태양)
   Secondary: #FF9500  (밝은 오렌지)
   Dark     : #1A1410  (딥 브라운-블랙)
   서체     : Noto Sans KR
═══════════════════════════════════════ */
:root {
  --bg:      #faf8f5;
  --bg2:     #f2ede6;
  --bg3:     #ebe4da;
  --ink:     #1a1410;
  --ink2:    #4a4038;
  --ink3:    #9a8f84;
  --h-pri:   #FF6B00;   /* 헥토 프라이머리 오렌지 */
  --h-sec:   #FF9500;   /* 세컨더리 오렌지 */
  --h-deep:  #CC4E00;   /* 다크 오렌지 (강조) */
  --h-pale:  #FFF0E6;   /* 오렌지 팔레트 라이트 */
  --border:  rgba(26,20,16,.1);
  --fb: 'Noto Sans KR', sans-serif;
  --fm: 'DM Mono', monospace;
  --r: 14px;
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--ink);font-family:var(--fb);line-height:1.7;overflow-x:hidden}

/* grain */
body::after{content:'';position:fixed;inset:0;background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 512 512' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='g'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23g)' opacity='0.022'/%3E%3C/svg%3E");pointer-events:none;z-index:8000;opacity:.5}

/* cursor */
#cur{width:8px;height:8px;background:var(--h-pri);border-radius:50%;position:fixed;top:0;left:0;pointer-events:none;z-index:9999;transform:translate(-50%,-50%);transition:width .15s,height .15s;mix-blend-mode:multiply}
#cur.big{width:22px;height:22px;opacity:.5}

/* ── NAV ── */
nav{position:fixed;top:0;left:0;right:0;z-index:500;padding:1.2rem 4vw;display:flex;justify-content:space-between;align-items:center;background:rgba(250,248,245,.93);backdrop-filter:blur(20px);border-bottom:1px solid var(--border)}
.nl{font-size:1rem;font-weight:900;letter-spacing:-.02em;color:var(--ink)}
.nl em{font-style:normal;color:var(--h-pri)}
.nr{display:flex;align-items:center;gap:2rem}
.nr a{font-family:var(--fm);font-size:.64rem;color:var(--ink3);text-decoration:none;letter-spacing:.14em;text-transform:uppercase;transition:color .2s}
.nr a:hover{color:var(--h-pri)}
.nr .cta-nav{padding:.48rem 1.3rem;background:var(--h-pri);color:#fff;border-radius:50px;font-family:var(--fm);font-size:.63rem;letter-spacing:.1em;text-transform:uppercase;text-decoration:none;transition:background .2s}
.nr .cta-nav:hover{background:var(--h-deep)}

/* ══════════════════════════════════════
   HERO
══════════════════════════════════════ */
#hero{min-height:100vh;padding:8.5rem 4vw 5rem;display:grid;grid-template-columns:1.2fr .8fr;gap:4rem;align-items:center;position:relative;overflow:hidden}

/* 배경 — 오렌지 그라디언트 원 */
.hbg-circle{position:absolute;right:-8vw;top:50%;transform:translateY(-50%);width:min(55vw,700px);height:min(55vw,700px);border-radius:50%;background:radial-gradient(circle,rgba(255,107,0,.12) 0%,rgba(255,149,0,.06) 50%,transparent 70%);pointer-events:none;z-index:1}
.hbg-lines{position:absolute;inset:0;background:repeating-linear-gradient(-52deg,transparent,transparent 58px,rgba(26,20,16,.014) 58px,rgba(26,20,16,.014) 59px);pointer-events:none;z-index:0}

.hl{position:relative;z-index:2}

/* 지원 칩 */
.chip{display:inline-flex;align-items:center;gap:.5rem;padding:.28rem .9rem .28rem .5rem;background:rgba(255,107,0,.09);border:1px solid rgba(255,107,0,.3);border-radius:50px;margin-bottom:1.4rem}
.chip-dot{width:6px;height:6px;border-radius:50%;background:var(--h-pri);animation:blink 1.8s ease-in-out infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.25}}
.chip-txt{font-family:var(--fm);font-size:.64rem;color:var(--h-pri);letter-spacing:.14em;text-transform:uppercase}

/* 타이틀 — Noto Sans KR 헤비 웨이트 활용 */
.htitle{font-size:clamp(3.5rem,7.5vw,7.5rem);font-weight:900;line-height:.9;letter-spacing:-.04em;margin-bottom:1.8rem}
.htitle .outline{-webkit-text-stroke:2.5px var(--ink);color:transparent}
.htitle .o{color:var(--h-pri)}

.hpitch{font-size:.98rem;color:var(--ink2);line-height:1.92;max-width:460px;margin-bottom:1.6rem;border-left:3px solid var(--h-pri);padding-left:1.1rem}
.hpitch strong{color:var(--ink)}

/* stat strip */
.hstrip{display:grid;grid-template-columns:repeat(4,1fr);border:1px solid var(--border);border-radius:var(--r);overflow:hidden;background:var(--bg2);margin-bottom:2rem}
.hs{padding:.85rem .6rem;text-align:center;border-right:1px solid var(--border)}
.hs:last-child{border-right:none}
.hs-n{font-size:1.7rem;font-weight:900;line-height:1;color:var(--h-pri);letter-spacing:-.03em}
.hs-l{font-family:var(--fm);font-size:.52rem;color:var(--ink3);letter-spacing:.06em;text-transform:uppercase;margin-top:.2rem;line-height:1.35}

.hbtns{display:flex;gap:.8rem;flex-wrap:wrap}
.btn-f{padding:.82rem 2rem;background:var(--h-pri);color:#fff;font-family:var(--fm);font-size:.73rem;letter-spacing:.1em;text-transform:uppercase;text-decoration:none;border-radius:50px;transition:background .2s,transform .2s;box-shadow:0 6px 20px rgba(255,107,0,.3)}
.btn-f:hover{background:var(--h-deep);transform:translateY(-2px)}
.btn-o{padding:.82rem 2rem;border:1.5px solid var(--ink);color:var(--ink);font-family:var(--fm);font-size:.73rem;letter-spacing:.1em;text-transform:uppercase;text-decoration:none;border-radius:50px;transition:all .2s}
.btn-o:hover{background:var(--ink);color:var(--bg);transform:translateY(-2px)}

/* hero right */
.hr{position:relative;z-index:2}
.fit-card{background:var(--ink);color:var(--bg);border-radius:20px;padding:2rem;margin-bottom:1rem}
.fc-head{font-family:var(--fm);font-size:.58rem;color:rgba(250,248,245,.28);letter-spacing:.18em;text-transform:uppercase;margin-bottom:1.1rem;padding-bottom:.7rem;border-bottom:1px solid rgba(255,255,255,.07)}
.fc-rows{display:flex;flex-direction:column;gap:.42rem}
.fc-row{display:grid;grid-template-columns:28px 1fr auto;gap:.7rem;align-items:center;padding:.62rem .82rem;border-radius:9px;background:rgba(255,255,255,.04);transition:background .2s}
.fc-row:hover{background:rgba(255,107,0,.1)}
.fc-ico{font-size:.95rem;text-align:center}
.fc-lbl{font-size:.76rem;font-weight:500;line-height:1.25}
.fc-lbl small{display:block;font-size:.62rem;color:rgba(250,248,245,.33);font-family:var(--fm);margin-top:.06rem}
.fc-ok{font-family:var(--fm);font-size:.6rem;font-weight:500;color:#6ee7b7;letter-spacing:.04em}

.ticker{background:var(--bg2);border:1px solid var(--border);border-radius:10px;padding:.75rem 1.1rem;display:flex;gap:.75rem;align-items:center;overflow:hidden}
.tl{font-family:var(--fm);font-size:.58rem;color:var(--h-pri);letter-spacing:.14em;text-transform:uppercase;white-space:nowrap;flex-shrink:0}
.tt{display:flex;gap:1.6rem;animation:tick 26s linear infinite;white-space:nowrap}
.tt span{font-size:.7rem;color:var(--ink2);font-family:var(--fm)}
@keyframes tick{from{transform:translateX(0)}to{transform:translateX(-50%)}}

/* ══════════════════════════════════════
   SHARED
══════════════════════════════════════ */
section{padding:7rem 4vw}
.sh{margin-bottom:3.8rem}
.sh-eye{font-family:var(--fm);font-size:.63rem;color:var(--h-pri);letter-spacing:.2em;text-transform:uppercase;margin-bottom:.5rem}
.sh-title{font-size:clamp(2.2rem,4vw,3.5rem);font-weight:900;letter-spacing:-.04em;line-height:.95}

/* ══════════════════════════════════════
   WHY ME — 오렌지 풀 블리드
══════════════════════════════════════ */
#why{background:var(--h-pri);padding:0}
.why-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:2px;background:rgba(255,255,255,.18)}
.wc{padding:3rem 2.2rem}
.wc:nth-child(1){background:var(--h-pri)}
.wc:nth-child(2){background:rgba(0,0,0,.07)}
.wc:nth-child(3){background:rgba(0,0,0,.13)}
.wc-ico{font-size:2rem;margin-bottom:.75rem}
.wc-title{font-size:1.8rem;font-weight:900;letter-spacing:-.04em;color:#fff;margin-bottom:.55rem}
.wc-body{font-size:.83rem;color:rgba(255,255,255,.6);line-height:1.82}
.wc-body strong{color:#fff}

/* ══════════════════════════════════════
   ABOUT
══════════════════════════════════════ */
#about{background:var(--bg2)}
.ag{display:grid;grid-template-columns:3fr 2fr;gap:5rem;align-items:start}
.ab p{font-size:.96rem;color:var(--ink2);line-height:1.92;margin-bottom:1.25rem}
.ab p strong{color:var(--ink)}

/* motivation quote */
.mq{background:var(--ink);color:var(--bg);border-radius:15px;padding:1.7rem 1.8rem;margin:1.5rem 0;position:relative;overflow:hidden}
.mq::before{content:'"';position:absolute;top:-1rem;left:1rem;font-size:9rem;font-weight:900;color:rgba(255,107,0,.18);line-height:1;pointer-events:none}
.mq-txt{font-size:.88rem;line-height:1.85;position:relative;z-index:1}
.mq-txt em{font-style:normal;color:var(--h-sec);font-weight:700}

.kw-row{display:flex;flex-wrap:wrap;gap:.42rem;margin-top:1.4rem}
.kw{padding:.3rem .78rem;border-radius:5px;font-family:var(--fm);font-size:.64rem;font-weight:500;letter-spacing:.04em}
.kw.o{background:rgba(255,107,0,.09);color:var(--h-deep);border:1px solid rgba(255,107,0,.25)}
.kw.k{background:rgba(26,20,16,.06);color:var(--ink2);border:1px solid var(--border)}
.kw.w{background:var(--h-pale);color:var(--h-deep);border:1px solid rgba(255,107,0,.18)}

.istack{display:flex;flex-direction:column;gap:.68rem}
.ir{background:var(--bg);border:1px solid var(--border);border-radius:12px;padding:.95rem 1.25rem;display:flex;justify-content:space-between;align-items:center;gap:1rem}
.ik{font-family:var(--fm);font-size:.59rem;color:var(--ink3);letter-spacing:.1em;text-transform:uppercase;min-width:68px}
.iv{font-size:.83rem;font-weight:500;text-align:right;line-height:1.35}
.iv.hl{color:var(--h-pri);font-weight:700}

/* ══════════════════════════════════════
   SKILLS
══════════════════════════════════════ */
#skills{}
.sg-wrap{display:grid;grid-template-columns:repeat(3,1fr);gap:1.3rem}
.sg{background:var(--bg2);border:1px solid var(--border);border-radius:15px;padding:1.65rem;transition:transform .25s,box-shadow .25s}
.sg:hover{transform:translateY(-5px);box-shadow:0 16px 42px rgba(255,107,0,.1)}
.sg-head{font-family:var(--fm);font-size:.59rem;letter-spacing:.16em;text-transform:uppercase;margin-bottom:1.05rem;padding-bottom:.72rem;border-bottom:2px solid var(--h-pri)}
.sg-tags{display:flex;flex-wrap:wrap;gap:.38rem}
.stag{font-size:.74rem;padding:.26rem .68rem;background:var(--bg);border:1px solid var(--border);border-radius:50px;color:var(--ink2);transition:all .2s;cursor:default}
.stag:hover{background:var(--h-pri);color:#fff;border-color:var(--h-pri)}

/* ══════════════════════════════════════
   CAREER TIMELINE
══════════════════════════════════════ */
#career{background:var(--bg2)}
.timeline{display:flex;flex-direction:column}
.cb{position:relative;padding-left:2.5rem;margin-bottom:5rem}
.cb::before{content:'';position:absolute;left:8px;top:22px;bottom:-5rem;width:2px;background:linear-gradient(to bottom,var(--h-pri),var(--border))}
.cb:last-child::before{display:none}
.cdot{position:absolute;left:0;top:16px;width:18px;height:18px;border-radius:50%;background:var(--h-pri);border:3px solid var(--bg2);box-shadow:0 0 0 3px rgba(255,107,0,.35)}

.co-name{font-size:1.7rem;font-weight:900;letter-spacing:-.03em;line-height:1}
.co-meta{font-family:var(--fm);font-size:.64rem;color:var(--ink3);letter-spacing:.08em;margin-top:.25rem}
.co-badges{display:flex;flex-wrap:wrap;gap:.45rem;margin-top:.7rem;margin-bottom:1.8rem}
.cbadge{display:inline-flex;align-items:center;gap:.28rem;padding:.26rem .75rem;border-radius:50px;font-family:var(--fm);font-size:.58rem;font-weight:500;letter-spacing:.07em;text-transform:uppercase}
.cb-period{background:var(--h-pri);color:#fff}
.cb-special{background:var(--h-pale);color:var(--h-deep);border:1px solid rgba(255,107,0,.3)}
.cb-note{background:rgba(26,20,16,.06);color:var(--ink2);border:1px solid var(--border);font-size:.56rem}

/* 파트리더 보조 notice */
.co-notice{background:var(--h-pale);border:1px solid rgba(255,107,0,.25);border-radius:10px;padding:.85rem 1.1rem;margin-bottom:1.6rem;font-size:.78rem;color:var(--ink2);line-height:1.65}
.co-notice strong{color:var(--h-deep)}

.pg{display:grid;grid-template-columns:repeat(auto-fill,minmax(300px,1fr));gap:1rem}
.pc{background:var(--bg);border:1px solid var(--border);border-radius:13px;overflow:hidden;transition:all .25s;position:relative}
.pc:hover{transform:translateY(-4px);box-shadow:0 12px 36px rgba(255,107,0,.13);border-color:var(--h-pri)}
.pc.key{border:2px solid var(--h-pri)}
.pc.key::after{content:'KEY';position:absolute;top:.8rem;right:.8rem;background:var(--h-pri);color:#fff;font-family:var(--fm);font-size:.49rem;font-weight:500;letter-spacing:.15em;padding:.14rem .48rem;border-radius:3px}
.pt{padding:1.15rem 1.4rem 0;display:flex;justify-content:space-between;align-items:flex-start}
.pseq{font-family:var(--fm);font-size:.57rem;color:var(--h-pri);letter-spacing:.14em}
.pper{font-family:var(--fm);font-size:.55rem;color:var(--ink3);background:var(--bg2);padding:.13rem .48rem;border-radius:3px}
.pname{padding:.4rem 1.4rem 0;font-size:1.08rem;font-weight:700;letter-spacing:-.02em;line-height:1.15}
.prole{padding:.2rem 1.4rem 0;font-size:.68rem;color:var(--ink3);font-family:var(--fm)}
.ptype{margin:.62rem 1.4rem 0;display:inline-flex;align-items:center;gap:.26rem;padding:.2rem .58rem;border-radius:4px;font-family:var(--fm);font-size:.57rem;font-weight:500;letter-spacing:.07em;text-transform:uppercase;background:var(--h-pale);color:var(--h-deep);border:1px solid rgba(255,107,0,.28)}
.ptype::before{content:'▶';font-size:.48em}
.pdiv{height:1px;background:var(--border);margin:.68rem 1.4rem 0}
.plist{padding:.78rem 1.4rem 1.15rem;list-style:none;display:flex;flex-direction:column;gap:.55rem}
.plist li{display:flex;gap:.58rem;font-size:.78rem;color:var(--ink2);line-height:1.55}
.plist li::before{content:'';flex-shrink:0;width:4px;height:4px;border-radius:50%;background:var(--h-pri);margin-top:.5rem}
.num{display:inline;font-family:var(--fm);font-size:.78em;font-weight:700;padding:.06em .36em;border-radius:3px;background:var(--h-pale);color:var(--h-deep)}

.presult{margin:.2rem 1.4rem 1.1rem;display:flex;align-items:center;gap:.5rem;padding:.6rem .9rem;background:var(--h-pale);border-radius:8px;border:1px solid rgba(255,107,0,.15)}
.presult-ico{font-size:.85rem}
.presult-txt{font-size:.76rem;color:var(--ink2);line-height:1.45}
.presult-txt strong{color:var(--h-deep);font-family:var(--fm)}

/* ══════════════════════════════════════
   HECTO CONNECT — 다크 배경에 오렌지 강조
══════════════════════════════════════ */
#hecto{background:var(--ink);color:var(--bg);padding:6rem 4vw}
.hc-grid{display:grid;grid-template-columns:1fr 1fr;gap:5rem;align-items:start}
.hc-l h2{font-size:clamp(2.4rem,5vw,4.2rem);font-weight:900;letter-spacing:-.04em;line-height:.9;margin-bottom:1.4rem}
.hc-l h2 em{font-style:normal;color:var(--h-sec)}
.hc-l p{color:rgba(250,248,245,.5);font-size:.9rem;line-height:1.9;margin-bottom:1.3rem}
.hc-l p strong{color:rgba(250,248,245,.9)}

/* diff table */
.diff-table{border:1px solid rgba(255,255,255,.08);border-radius:12px;overflow:hidden;margin-top:1.8rem}
.diff-row{display:grid;grid-template-columns:1fr 1fr}
.diff-row:not(:last-child){border-bottom:1px solid rgba(255,255,255,.06)}
.diff-cell{padding:.8rem 1.1rem;font-size:.78rem;line-height:1.6}
.diff-cell:first-child{color:rgba(250,248,245,.35);border-right:1px solid rgba(255,255,255,.06)}
.diff-cell:last-child{color:rgba(250,248,245,.85)}
.diff-head .diff-cell{font-family:var(--fm);font-size:.58rem;letter-spacing:.12em;text-transform:uppercase;background:rgba(255,107,0,.15);color:rgba(250,248,245,.5)!important;padding:.65rem 1.1rem}

.hc-r{display:flex;flex-direction:column;gap:1rem}
.hcc{background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.07);border-radius:13px;padding:1.3rem 1.5rem;transition:background .2s,border-color .2s}
.hcc:hover{background:rgba(255,107,0,.08);border-color:rgba(255,107,0,.25)}
.hcc-top{display:flex;align-items:center;gap:.8rem;margin-bottom:.65rem}
.hcc-ico{width:34px;height:34px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:.95rem;flex-shrink:0;background:rgba(255,107,0,.15)}
.hcc-title{font-size:.85rem;font-weight:700;color:var(--bg)}
.hcc-sub{font-size:.68rem;color:rgba(250,248,245,.32);font-family:var(--fm);margin-top:.06rem}
.hcc-body{font-size:.78rem;color:rgba(250,248,245,.5);line-height:1.72}
.hcc-body strong{color:rgba(250,248,245,.88)}

/* ══════════════════════════════════════
   CONTACT
══════════════════════════════════════ */
#contact{}
.ct-wrap{display:grid;grid-template-columns:1fr 1fr;gap:5rem;align-items:start}
.ct-l h3{font-size:2.2rem;font-weight:900;letter-spacing:-.04em;line-height:1;margin-bottom:1rem}
.ct-l p{color:var(--ink2);font-size:.9rem;line-height:1.88;margin-bottom:1.9rem}
.ctlinks{display:flex;flex-direction:column;gap:.68rem}
.cta-link{display:flex;align-items:center;gap:1rem;padding:.95rem 1.25rem;background:var(--bg2);border:1px solid var(--border);border-radius:12px;text-decoration:none;color:var(--ink);transition:all .2s;font-size:.84rem}
.cta-link:hover{background:var(--h-pri);color:#fff;border-color:var(--h-pri);transform:translateX(5px)}
.cta-ico{width:35px;height:35px;background:var(--bg);border:1px solid var(--border);border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:.88rem;flex-shrink:0;transition:all .2s}
.cta-link:hover .cta-ico{background:rgba(255,255,255,.2);border-color:transparent}
.cta-info{flex:1}
.cta-lbl{font-family:var(--fm);font-size:.56rem;color:var(--ink3);letter-spacing:.12em;text-transform:uppercase}
.cta-link:hover .cta-lbl{color:rgba(255,255,255,.6)}
.cta-val{font-weight:500;font-size:.81rem}

.ct-r{background:var(--h-pri);color:#fff;border-radius:20px;padding:2.8rem;position:relative;overflow:hidden}
.ct-r::before{content:'';position:absolute;right:-4rem;bottom:-4rem;width:200px;height:200px;border-radius:50%;background:rgba(255,255,255,.08);pointer-events:none}
.ct-r::after{content:'';position:absolute;right:2rem;top:-3rem;width:140px;height:140px;border-radius:50%;background:rgba(255,255,255,.06);pointer-events:none}
.ct-r h4{font-size:2rem;font-weight:900;letter-spacing:-.04em;line-height:1.05;margin-bottom:.9rem;position:relative;z-index:1}
.ct-r p{color:rgba(255,255,255,.68);font-size:.83rem;line-height:1.82;margin-bottom:1.9rem;position:relative;z-index:1}
.ct-btn{display:inline-block;padding:.9rem 2.2rem;background:#fff;color:var(--h-pri);font-family:var(--fm);font-size:.75rem;letter-spacing:.1em;text-transform:uppercase;text-decoration:none;border-radius:50px;font-weight:700;transition:opacity .2s,transform .2s;box-shadow:0 8px 24px rgba(0,0,0,.15);position:relative;z-index:1}
.ct-btn:hover{opacity:.9;transform:scale(1.03)}

footer{padding:1.6rem 4vw;border-top:1px solid var(--border);display:flex;justify-content:space-between;align-items:center}
footer span{font-family:var(--fm);font-size:.62rem;color:var(--ink3);letter-spacing:.08em}

/* REVEAL */
.rv{opacity:0;transform:translateY(22px);transition:opacity .6s ease,transform .6s ease}
.rv.on{opacity:1;transform:none}
.d1{transition-delay:.08s}.d2{transition-delay:.16s}.d3{transition-delay:.24s}

@media(max-width:960px){
  #hero{grid-template-columns:1fr}.hr{display:none}
  .ag,.hc-grid,.ct-wrap{grid-template-columns:1fr;gap:2.5rem}
  .why-grid,.sg-wrap{grid-template-columns:1fr 1fr}
}
@media(max-width:600px){
  .nr a{display:none}
  section{padding:4.5rem 5vw}
  .why-grid,.sg-wrap{grid-template-columns:1fr}
  .hstrip{grid-template-columns:1fr 1fr}
  .htitle{font-size:3.2rem}
}
</style>
</head>
<body>
<div id="cur"></div>

<!-- NAV -->
<nav>
  <div class="nl">HECTO<em>.</em>SALES</div>
  <div class="nr">
    <a href="#why">Why Me</a>
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#career">Career</a>
    <a href="#hecto">헥토핏</a>
    <a href="#contact" class="cta-nav">지원 연락</a>
  </div>
</nav>

<!-- ══════════════════════════════════════
     HERO
══════════════════════════════════════ -->
<section id="hero">
  <div class="hbg-lines"></div>
  <div class="hbg-circle"></div>

  <div class="hl">
    <div class="chip">
      <div class="chip-dot"></div>
      <span class="chip-txt">헥토파이낸셜 모바일쿠폰 B2B 영업 지원</span>
    </div>

    <h1 class="htitle">
      B2B<br>
      <span class="outline">SALES</span><br>
      <span class="o">CLOSER</span>
    </h1>

    <p class="hpitch">
      고객사의 <strong>예산·KPI에 맞는 판을 짜주는</strong> 영업인입니다.<br>
      단가 싸움 대신 <strong>리워드 솔루션 제안서</strong>로 승부하고,<br>
      데이터로 성과를 증명하며 <strong>재계약을 만들어냅니다.</strong>
    </p>

    <div class="hstrip">
      <div class="hs"><div class="hs-n">+32%</div><div class="hs-l">브랜드스토어<br>월 매출 상승</div></div>
      <div class="hs"><div class="hs-n">+28%</div><div class="hs-l">광고주<br>유입 증대</div></div>
      <div class="hs"><div class="hs-n">+24%</div><div class="hs-l">CVR<br>개선</div></div>
      <div class="hs"><div class="hs-n">4건</div><div class="hs-l">제안서<br>채택</div></div>
    </div>

    <div class="hbtns">
      <a href="#career" class="btn-f">영업 성과 보기</a>
      <a href="#hecto" class="btn-o">헥토파이낸셜 적합성</a>
    </div>
  </div>

  <div class="hr">
    <div class="fit-card">
      <div class="fc-head">// 헥토파이낸셜 B2B 쿠폰영업 — 요구 역량 매칭</div>
      <div class="fc-rows">
        <div class="fc-row"><div class="fc-ico">🎯</div><div class="fc-lbl">아웃바운드 신규 수주<small>잠재 법인 발굴·제안·클로징</small></div><div class="fc-ok">✓ 보유</div></div>
        <div class="fc-row"><div class="fc-ico">📊</div><div class="fc-lbl">데이터 기반 제안서<small>ROAS·ROI 수치로 설득</small></div><div class="fc-ok">✓ 보유</div></div>
        <div class="fc-row"><div class="fc-ico">🔄</div><div class="fc-lbl">계정 관리 & 재계약<small>이탈 방지·유지율 관리</small></div><div class="fc-ok">✓ 보유</div></div>
        <div class="fc-row"><div class="fc-ico">🏢</div><div class="fc-lbl">법인 고객 커뮤니케이션<small>B2B·B2G 다양한 고객군</small></div><div class="fc-ok">✓ 보유</div></div>
        <div class="fc-row"><div class="fc-ico">🎙</div><div class="fc-lbl">진정성 중심 소통<small>경청·공감 → 신뢰 구축</small></div><div class="fc-ok">✓ 보유</div></div>
      </div>
    </div>
    <div class="ticker">
      <span class="tl">TRACK</span>
      <div class="tt">
        <span>아웃바운드 영업</span><span>·</span><span>리워드 제안서</span><span>·</span>
        <span>계정 관리</span><span>·</span><span>CVR +24%</span><span>·</span>
        <span>ROAS 개선</span><span>·</span><span>탑퍼포머</span><span>·</span>
        <span>법인 수주</span><span>·</span><span>이탈 방지</span><span>·</span>
        <span>아웃바운드 영업</span><span>·</span><span>리워드 제안서</span><span>·</span>
        <span>계정 관리</span><span>·</span><span>CVR +24%</span><span>·</span>
        <span>ROAS 개선</span><span>·</span><span>탑퍼포머</span><span>·</span>
        <span>법인 수주</span><span>·</span><span>이탈 방지</span><span>·</span>
      </div>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════════
     WHY ME
══════════════════════════════════════ -->
<section id="why" style="padding:0">
  <div class="why-grid rv">
    <div class="wc"><div class="wc-ico">🎯</div><div class="wc-title">CLOSE</div><div class="wc-body">광고주·가맹점주·기관을 직접 설득해 계약을 따낸 경험. 현장 방문객 <strong>+150%</strong>, 제안서 채택 <strong>4건</strong>, 신규 수주 다수.</div></div>
    <div class="wc"><div class="wc-ico">📈</div><div class="wc-title">GROW</div><div class="wc-body">데이터로 성과를 증명하고 추가 예산·업셀을 이끌어낸 경험. 브랜드스토어 <strong>+32%</strong>, 유입 <strong>+28%</strong>, CVR <strong>+24%</strong>.</div></div>
    <div class="wc"><div class="wc-ico">🤝</div><div class="wc-title">RETAIN</div><div class="wc-body">경청·공감·컨설팅으로 비용 저항 고객을 붙잡아 이탈을 막고 장기 파트너십을 만든 경험. 탑퍼포머 인정.</div></div>
  </div>
</section>

<!-- ══════════════════════════════════════
     ABOUT
══════════════════════════════════════ -->
<section id="about">
  <div class="sh rv"><div class="sh-eye">// 01 · About Me</div><div class="sh-title">이런 B2B 영업인입니다</div></div>
  <div class="ag rv">
    <div class="ab">
      <p><strong>B2B 솔루션 영업 전문가</strong>입니다. 영업은 단순히 상품의 장점을 나열하는 게 아니라, <strong>고객사의 상황에 맞는 판을 짜주는 일</strong>이라 생각합니다. 대학 시절 시장 조사 프로젝트에서 상대방의 숨은 니즈를 파악하는 법을 배웠고, 그것이 영업을 선택한 이유입니다.</p>
      <p>예지솔루션에서는 <strong>신규 광고주를 직접 발굴하고 데이터 기반 제안서로 계약을 성사</strong>시켰습니다. 쿠팡에서는 비용에 민감한 점주들을 <strong>경청·공감 중심의 소통으로 먼저 마음을 열고</strong>, 상권 데이터 기반 매출 시뮬레이션으로 설득해 이탈을 막았습니다. 탑퍼포머로 인정받아 <strong>파트리더 역할을 보조</strong>하며 팀의 거절 대응 스크립트를 표준화했습니다.</p>
      <p>가격 경쟁이 아닌 <strong>솔루션의 가치로 계약을 따내고, 진정성으로 고객을 유지하는 것</strong>이 저의 영업 방식입니다.</p>
      <div class="mq">
        <div class="mq-txt">"헥토파이낸셜은 PG부터 내통장결제까지 완벽히 내재화된 <em>유일한 기업</em>입니다. 단가 싸움 대신, 결제·리워드 원스톱 솔루션이라는 무기로 <em>법인 고객의 예산·KPI에 맞는 제안서</em>를 들고 아웃바운드 영업을 하겠습니다."</div>
      </div>
      <div class="kw-row">
        <span class="kw o">아웃바운드 영업</span><span class="kw o">B2B 제안서 작성</span><span class="kw o">신규 수주·클로징</span>
        <span class="kw w">계정 관리</span><span class="kw w">이탈 방지 소통</span><span class="kw w">재계약 유도</span>
        <span class="kw k">탑퍼포머</span><span class="kw k">파트리더 보조</span><span class="kw k">데이터 설득</span>
        <span class="kw k">ROAS 분석</span><span class="kw k">매출 시뮬레이션</span>
      </div>
    </div>
    <div class="istack">
      <div class="ir"><span class="ik">총 경력</span><span class="iv">약 3년 4개월</span></div>
      <div class="ir"><span class="ik">쿠팡 직급</span><span class="iv">사원 (탑퍼포머 → 파트리더 보조)</span></div>
      <div class="ir"><span class="ik">예지 직급</span><span class="iv">SL — Self Leader</span></div>
      <div class="ir"><span class="ik">영업 유형</span><span class="iv">B2B · B2G · 솔루션 영업</span></div>
      <div class="ir"><span class="ik">고객군</span><span class="iv">광고주 · 가맹점주<br>소상공인 · 관계기관</span></div>
      <div class="ir"><span class="ik">이메일</span><span class="iv hl">s_miiing@naver.com</span></div>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════════
     SKILLS
══════════════════════════════════════ -->
<section id="skills">
  <div class="sh rv"><div class="sh-eye">// 02 · B2B Sales Skills</div><div class="sh-title">영업 역량</div></div>
  <div class="sg-wrap">
    <div class="sg rv"><div class="sg-head" style="color:var(--h-deep)">Hunting · 신규 발굴</div><div class="sg-tags"><span class="stag">잠재 법인 고객 발굴</span><span class="stag">아웃바운드 콜·방문</span><span class="stag">타겟 산업군 분석</span><span class="stag">니즈·예산 파악</span><span class="stag">파이프라인 구축</span></div></div>
    <div class="sg rv d1"><div class="sg-head" style="color:var(--h-deep)">Proposal · 제안·설득</div><div class="sg-tags"><span class="stag">리워드 솔루션 제안서</span><span class="stag">ROI·ROAS 기반 설득</span><span class="stag">경쟁사 분석 활용</span><span class="stag">매출 시뮬레이션</span><span class="stag">예산·KPI 맞춤 제안</span></div></div>
    <div class="sg rv d2"><div class="sg-head" style="color:var(--h-deep)">Closing · 계약 체결</div><div class="sg-tags"><span class="stag">거절 대응 스크립트</span><span class="stag">경청·공감 소통</span><span class="stag">현장 전환 영업</span><span class="stag">계약 클로징</span></div></div>
    <div class="sg rv"><div class="sg-head" style="color:var(--h-deep)">Account Mgmt · 고객 유지</div><div class="sg-tags"><span class="stag">계정 전담 관리</span><span class="stag">성과 리포팅·보고</span><span class="stag">이탈 방지 케어</span><span class="stag">재계약·업셀 유도</span><span class="stag">감정 리스크 해소</span></div></div>
    <div class="sg rv d1"><div class="sg-head" style="color:var(--h-deep)">Team · 조직 기여</div><div class="sg-tags"><span class="stag">탑퍼포머 실적</span><span class="stag">파트리더 보조 수행</span><span class="stag">거절 대응 SOP 작성</span><span class="stag">업무 우선순위 조율</span><span class="stag">신입 교육 보조</span></div></div>
    <div class="sg rv d2"><div class="sg-head" style="color:var(--h-deep)">Data & Analytics</div><div class="sg-tags"><span class="stag">KPI·ROAS 트래킹</span><span class="stag">상권·주문 데이터 분석</span><span class="stag">유입·전환 분석</span><span class="stag">경쟁사 입찰 분석</span><span class="stag">엑셀 / 스프레드시트</span></div></div>
  </div>
</section>

<!-- ══════════════════════════════════════
     CAREER
══════════════════════════════════════ -->
<section id="career">
  <div class="sh rv"><div class="sh-eye">// 03 · Career & Sales Results</div><div class="sh-title">경력 & 영업 성과</div></div>
  <div class="timeline">

    <!-- 예지솔루션 -->
    <div class="cb rv">
      <div class="cdot"></div>
      <div class="co-name">㈜예지솔루션</div>
      <div class="co-meta">네이버사업부 · SL(Self Leader) · 신규 광고주 아웃바운드 영업</div>
      <div class="co-badges">
        <span class="cbadge cb-period">2022.07 – 2023.10 · 1년 3개월</span>
        <span class="cbadge cb-special">SL 직급</span>
        <span class="cbadge cb-note">아웃바운드 영업 · 제안서 작성 · 계정 관리</span>
      </div>
      <div class="pg">
        <div class="pc key">
          <div class="pt"><span class="pseq">PROJECT 01</span><span class="pper">23.05–23.10</span></div>
          <div class="pname">그릭데이</div>
          <div class="prole">시즌 수요 분석 · 쇼핑검색 최적화 제안</div>
          <div class="ptype">데이터 제안 영업</div>
          <div class="pdiv"></div>
          <ul class="plist">
            <li>성수기 다이어트 수요 분석 → 네이버 쇼핑검색 광고 최적화 제안 수용</li>
            <li>브랜드스토어 월 매출 <span class="num">+32% 상승</span> 및 ROAS 효율 개선</li>
            <li>성과 데이터 제시로 광고주 추가 예산 집행 결정 이끌어냄</li>
          </ul>
          <div class="presult"><div class="presult-ico">📈</div><div class="presult-txt">결과: 월 매출 <strong>+32%</strong> · ROAS 개선 → 추가 예산 수주</div></div>
        </div>
        <div class="pc key">
          <div class="pt"><span class="pseq">PROJECT 02</span><span class="pper">23.01–23.10</span></div>
          <div class="pname">컴투펫케어</div>
          <div class="prole">경쟁사 분석 기반 전략 제안 · 매체 확장 업셀</div>
          <div class="ptype">제안 영업 · 업셀링</div>
          <div class="pdiv"></div>
          <ul class="plist">
            <li>유저 동선 분석 기반 맞춤형 프로모션 제안 → 광고주 전략 변경 승인</li>
            <li>경쟁사 입찰가·노출 순위 데이터 제시 → 최적화 실행</li>
            <li>매체 확장 제안 채택 → 신규 채널 개척·업셀 성공</li>
          </ul>
          <div class="presult"><div class="presult-ico">🎯</div><div class="presult-txt">결과: 월 평균 유입량 <strong>+28% 증가</strong> → 추가 예산 확보</div></div>
        </div>
        <div class="pc key">
          <div class="pt"><span class="pseq">PROJECT 03</span><span class="pper">23.03–23.10</span></div>
          <div class="pname">EF코리아</div>
          <div class="prole">이탈 구간 분석 · CVR 개선 제안</div>
          <div class="ptype">성과 책임 영업</div>
          <div class="pdiv"></div>
          <ul class="plist">
            <li>이탈 구간 분석 후 캠페인 최적화 제안 → 광고주 수용</li>
            <li>타겟 세분화·소재 A/B 테스트 진행</li>
          </ul>
          <div class="presult"><div class="presult-ico">🔄</div><div class="presult-txt">결과: 전환율(CVR) <strong>+24% 개선</strong> → 재계약 성사</div></div>
        </div>
        <div class="pc">
          <div class="pt"><span class="pseq">PROJECT 04</span><span class="pper">22.07–23.10</span></div>
          <div class="pname">비타민하우스</div>
          <div class="prole">프로모션 연계 제안 · 장기 계정 유지</div>
          <div class="ptype">계정 유지 영업</div>
          <div class="pdiv"></div>
          <ul class="plist">
            <li>프로모션 일정 선제 분석 → 시즌 예산 집중 투입 제안 수용</li>
            <li>성과 모니터링·리포팅으로 광고주 신뢰 확보, 이탈 제로</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 책임지는사회네트워크 -->
    <div class="cb rv">
      <div class="cdot"></div>
      <div class="co-name">책임지는사회네트워크</div>
      <div class="co-meta">전략기획본부 · 사원 · B2G 현장 영업·행사 기획</div>
      <div class="co-badges">
        <span class="cbadge cb-period">2024.07 – 2024.10 · 4개월</span>
        <span class="cbadge cb-note">B2G 제안 · 현장 클로징 · 오프라인 영업</span>
      </div>
      <div class="pg">
        <div class="pc key">
          <div class="pt"><span class="pseq">PROJECT 01</span><span class="pper">24.07–24.08</span></div>
          <div class="pname">온누리상품권 홍보부스</div>
          <div class="prole">현장 고객 전환 · 대량 발행 유도</div>
          <div class="ptype">현장 클로징 영업</div>
          <div class="pdiv"></div>
          <ul class="plist">
            <li>부스 운영 프로세스·메시지 개선 → 방문객 <span class="num">+150% 증가</span></li>
            <li>현장 대면 설득으로 상품권 대량 발행률 <span class="num">+30% 상승</span></li>
            <li>고객 만족도 <span class="num">4.6/5점</span> 달성</li>
          </ul>
          <div class="presult"><div class="presult-ico">🏆</div><div class="presult-txt">현장 대면 설득으로 <strong>대량 발행 직접 견인</strong> — 헥토 쿠폰 현장 영업과 직결</div></div>
        </div>
        <div class="pc">
          <div class="pt"><span class="pseq">PROJECT 02</span><span class="pper">24.07</span></div>
          <div class="pname">전통시장 관계기관 워크숍</div>
          <div class="prole">관계자 설득 · 제안서 채택 · 후속 수주</div>
          <div class="ptype">B2G 제안 영업</div>
          <div class="pdiv"></div>
          <ul class="plist">
            <li>지자체·유관기관·외부 파트너 소통 채널 단일화로 행사 총괄</li>
            <li>관계자 <span class="num">80명</span> 대면 네트워킹 및 신뢰 관계 구축</li>
          </ul>
          <div class="presult"><div class="presult-ico">📋</div><div class="presult-txt">결과: 제안서 <strong>4건 채택</strong> → 후속 사업 수주로 직결</div></div>
        </div>
      </div>
    </div>

    <!-- 쿠팡 -->
    <div class="cb rv">
      <div class="cdot"></div>
      <div class="co-name">쿠팡(주)</div>
      <div class="co-meta">Eats Ads Sales 2 · 사원 · 입점 업주 광고 영업 & 리텐션 관리</div>
      <div class="co-badges">
        <span class="cbadge cb-period">2024.10 – 2025.11 · 1년 1개월</span>
        <span class="cbadge cb-special">탑퍼포머 → 파트리더 보조</span>
        <span class="cbadge cb-note">실무 성과 인정 · 사원으로서 파트 리딩 보조 수행</span>
      </div>
      <div class="co-notice">
        <strong>※ 파트리더 보조 역할 배경</strong><br>
        정식 직급은 사원이나, 현장 세일즈 탑퍼포머로서 파트 내 실무 리더 역할을 보조적으로 겸임했습니다. 거절 대응 스크립트 표준화, 업무 우선순위 조율 등 파트 운영 보조 실무를 수행했습니다.
      </div>
      <div class="pg">
        <div class="pc key">
          <div class="pt"><span class="pseq">PROJECT 01</span><span class="pper">24.10–25.11</span></div>
          <div class="pname">진정성 소통 기반 가맹점 밀착 케어</div>
          <div class="prole">경청·공감 → 신뢰 구축 → 플랫폼 록인(Lock-in)</div>
          <div class="ptype">Retention 영업</div>
          <div class="pdiv"></div>
          <ul class="plist">
            <li>비용 저항 높은 점주 대상 <strong>경청·공감 중심 소통</strong>으로 감정 리스크 선제 해소</li>
            <li>애로사항 해결을 통한 견고한 신뢰 관계 구축 → 이탈 위기 가맹점 설득</li>
            <li>광고 유지율 극대화 및 <strong>장기 파트너십 전환</strong> 성과 달성</li>
          </ul>
          <div class="presult"><div class="presult-ico">🤝</div><div class="presult-txt">헥토 법인 계정 관리에 <strong>그대로 적용 가능한 Retention 역량</strong></div></div>
        </div>
        <div class="pc key">
          <div class="pt"><span class="pseq">PROJECT 02</span><span class="pper">25.07–25.11</span></div>
          <div class="pname">상권 데이터 기반 매출 시뮬레이션 제안</div>
          <div class="prole">주문 흐름·상권 분석 → 맞춤형 효율 제안</div>
          <div class="ptype">데이터 솔루션 영업</div>
          <div class="pdiv"></div>
          <ul class="plist">
            <li>주문 시간대·지역 상권 데이터 분석 → 매장별 <strong>맞춤 매출 시뮬레이션 제공</strong></li>
            <li>효율 저하 매장 즉각 모니터링·운영 조정으로 고객 만족도 개선</li>
            <li>데이터 기반 추가 집행 제안으로 업셀링 기회 창출</li>
          </ul>
        </div>
        <div class="pc">
          <div class="pt"><span class="pseq">PROJECT 03</span><span class="pper">25.02–25.11</span></div>
          <div class="pname">탑퍼포머 기반 파트리더 역할 보조</div>
          <div class="prole">거절 대응 SOP · 업무 우선순위 조율 · 파트 운영 보조</div>
          <div class="ptype">★ 팀 기여</div>
          <div class="pdiv"></div>
          <ul class="plist">
            <li>현장 세일즈 성과 인정 → 파트 내 실무 리더 역할 보조 겸임</li>
            <li>팀원 거절 대응 스크립트 <strong>표준화</strong> 및 일일 업무 우선순위 조율</li>
            <li>운영 기준 가이드라인 정립으로 파트 전체 영업 효율 향상</li>
          </ul>
          <div class="presult"><div class="presult-ico">⭐</div><div class="presult-txt">사원으로서 <strong>탑퍼포머 실적</strong>으로 파트 운영 보조까지 수행</div></div>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- ══════════════════════════════════════
     HECTO CONNECT
══════════════════════════════════════ -->
<section id="hecto" style="padding:0">
  <div class="hc-grid rv" style="padding:6rem 4vw">
    <div class="hc-l">
      <h2>왜<br><em>헥토파이낸셜</em>인가</h2>
      <p>수많은 쿠폰 기업 중 헥토파이낸셜을 선택한 이유는 <strong>PG(전자금융결제)부터 내통장결제, 간편현금결제 인프라까지 완벽히 내재화된 유일한 기업</strong>이기 때문입니다.</p>
      <p>일반 쿠폰 유통사들이 단가 경쟁에 매몰될 때, 헥토파이낸셜은 <strong>결제 정산과 모바일 쿠폰 리워드를 원스톱으로 제공</strong>합니다. 이는 대형 법인 고객의 구매·마케팅 담당자를 설득할 때 <strong>예산 절감 + 행정 효율화</strong>라는 가장 강력한 무기입니다.</p>
      <div class="diff-table">
        <div class="diff-row diff-head"><div class="diff-cell">일반 쿠폰 유통사</div><div class="diff-cell">헥토파이낸셜 (내 무기)</div></div>
        <div class="diff-row"><div class="diff-cell">단가 경쟁·마진 경쟁</div><div class="diff-cell">결제+쿠폰 원스톱 가치 제안</div></div>
        <div class="diff-row"><div class="diff-cell">쿠폰 발행만 가능</div><div class="diff-cell">PG·내통장·간편현금 내재화</div></div>
        <div class="diff-row"><div class="diff-cell">가격으로만 설득</div><div class="diff-cell">예산 절감 + 행정 효율 설득</div></div>
      </div>
    </div>
    <div class="hc-r d1">
      <div class="hcc"><div class="hcc-top"><div class="hcc-ico">🎯</div><div><div class="hcc-title">아웃바운드 타겟 전략</div><div class="hcc-sub">기업 복지몰 · 마케팅 대행사 · 금융사</div></div></div><div class="hcc-body">대량 쿠폰 수요가 확실한 산업군 타겟 리스트 구축 → <strong>공격적인 아웃바운드 영업</strong> 시작. 예지솔루션의 Hunting → Proposal → Closing 사이클을 그대로 적용합니다.</div></div>
      <div class="hcc"><div class="hcc-top"><div class="hcc-ico">📋</div><div><div class="hcc-title">리워드 솔루션 제안서</div><div class="hcc-sub">단가 경쟁 NO → 가치 제안 YES</div></div></div><div class="hcc-body">고객사 예산·KPI에 맞춘 <strong>리워드 솔루션 제안서</strong>로 승부합니다. 결제 인프라 통합 가치를 수치로 증명해 계약을 따냅니다.</div></div>
      <div class="hcc"><div class="hcc-top"><div class="hcc-ico">🔄</div><div><div class="hcc-title">법인 고객 재계약률 극대화</div><div class="hcc-sub">쿠팡 Retention 역량 → 헥토 AM</div></div></div><div class="hcc-body">쿠팡에서 비용 저항 고객을 경청·데이터로 붙잡은 경험. <strong>헥토파이낸셜 대형 법인 고객 사후 관리</strong>와 재계약률 극대화에 바로 이어집니다.</div></div>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════════
     CONTACT
══════════════════════════════════════ -->
<section id="contact">
  <div class="sh rv"><div class="sh-eye">// 04 · Contact</div><div class="sh-title">헥토파이낸셜<br>B2B 쿠폰영업에<br>지원합니다</div></div>
  <div class="ct-wrap rv">
    <div class="ct-l">
      <h3>함께<br>수주를 만들어요</h3>
      <p>모바일쿠폰 B2B 영업, 법인 신규 수주, 계정 관리 포지션에 즉시 기여할 준비가 되어 있습니다.</p>
      <div class="ctlinks">
        <a href="mailto:s_miiing@naver.com" class="cta-link">
          <div class="cta-ico">✉️</div>
          <div class="cta-info"><div class="cta-lbl">Email</div><div class="cta-val">s_miiing@naver.com</div></div>
        </a>
      </div>
    </div>
    <div class="ct-r">
      <h4>고객사의 판을<br>짜드리겠습니다</h4>
      <p>예지솔루션 아웃바운드 영업 → 쿠팡 탑퍼포머 → 파트리더 보조. 헥토파이낸셜에서 그 다음 챕터를 쓰겠습니다.</p>
      <a href="mailto:s_miiing@naver.com" class="ct-btn">이메일 보내기 →</a>
    </div>
  </div>
</section>

<footer>
  <span>© 2025 B2B Sales Portfolio — 헥토파이낸셜 모바일쿠폰 영업 지원용</span>
  <span>s_miiing@naver.com</span>
</footer>

<script>
const cur=document.getElementById('cur');
document.addEventListener('mousemove',e=>{cur.style.left=e.clientX+'px';cur.style.top=e.clientY+'px'});
document.querySelectorAll('a,button').forEach(el=>{
  el.addEventListener('mouseenter',()=>cur.classList.add('big'));
  el.addEventListener('mouseleave',()=>cur.classList.remove('big'));
});
const obs=new IntersectionObserver(entries=>{
  entries.forEach(e=>{if(e.isIntersecting){e.target.classList.add('on');obs.unobserve(e.target)}});
},{threshold:.06,rootMargin:'0px 0px -28px 0px'});
document.querySelectorAll('.rv').forEach(el=>obs.observe(el));
</script>
</body>
</html>
