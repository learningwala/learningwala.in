---
title: "Mihir Pathak"
---

<script>function hmfb(i){var s=i.getAttribute('src');if(s.indexOf('/images/')!==0){i.src='/images'+s;}else{i.onerror=null;}}</script>

<div class="hm">
<div class="hm-wrap">
<section class="hm-first">
<figure class="hm-tree">
<div class="hm-float">
<button type="button" class="hm-treebtn" aria-label="Tap to see another tree">
<img class="is-on" src="/index/tree-watercolor.webp" onerror="hmfb(this)" alt="A watercolour painting of a tree with a green and blue canopy and a golden trunk" width="1000" height="1000" fetchpriority="high" decoding="async">
<img src="/index/tree-yellow.png" onerror="hmfb(this)" alt="A hand-drawn tree with a green and orange canopy, a blue trunk and a yellow wash" width="1000" height="1000" loading="lazy" decoding="async">
<img src="/index/tree-pink.png" onerror="hmfb(this)" alt="A hand-drawn tree with a pink canopy and a black inked trunk on a teal wash" width="1000" height="1000" loading="lazy" decoding="async">
<img src="/index/tree-blue.jpg" onerror="hmfb(this)" alt="A small inked tree with a blue canopy and a green wash" width="1000" height="1000" loading="lazy" decoding="async">
<img src="/index/tree-ink.webp" onerror="hmfb(this)" alt="A pen drawing of a tree in black and blue ink" width="1000" height="1000" loading="lazy" decoding="async">
</button>
</div>
<figcaption class="hm-hint"><span>tap the tree</span><span class="hm-dots" aria-hidden="true"></span></figcaption>
<a class="hm-poemlink" href="https://www.themarginalian.org/2018/09/11/martin-buber-tree/" target="_blank" rel="noopener">Read Martin Buber on the tree ↗</a>
</figure>
<div class="hm-hero">
<h1 class="hm-name">Mihir Pathak</h1>
<svg class="hm-scrawl" viewBox="0 0 400 12" preserveAspectRatio="none" aria-hidden="true"><path pathLength="1" d="M2 7 C 70 3, 150 10, 230 5 S 350 8, 398 4"/></svg>
<p class="hm-lead">Hi, I’m a storyteller &amp; educator with specific interest in <mark class="hm-hl">‘Education for harmony’</mark>.</p>
<p class="hm-idea">This website is a living portfolio of my practice and philosophy.</p>
<ul class="hm-roles">
<li><a href="/educator">Educator</a></li>
<li><a href="/storyteller">Storyteller</a></li>
<li><a href="/philosophy">Philosophy</a></li>
</ul>
<p class="hm-find">Find me on: <a href="https://www.instagram.com/learningwala/" target="_blank" rel="noopener">Instagram</a><span aria-hidden="true"> | </span><a href="https://medium.com/learningwala" target="_blank" rel="noopener">Medium</a><span aria-hidden="true"> | </span><a href="https://www.linkedin.com/in/learningwalamihir/" target="_blank" rel="noopener">LinkedIn</a><br>Email: <a href="mailto:learningwalamihir@gmail.com">learningwalamihir@gmail.com</a></p>
</div>
</section>
</div>
</div>

<script>
(function(){
var root=document.querySelector('.hm');if(!root)return;
/* tap the tree: show the next hand-drawn tree */
var btn=root.querySelector('.hm-treebtn'),imgs=[].slice.call(btn.querySelectorAll('img')),
dotBox=root.querySelector('.hm-dots'),cur=0,dots=[];
imgs.forEach(function(m,k){var i=document.createElement('i');if(k===0)i.className='is-on';dotBox.appendChild(i);dots.push(i);});
var reduce=matchMedia('(prefers-reduced-motion:reduce)').matches;
var busy=false;
btn.addEventListener('click',function(){
if(busy)return;
busy=true;
cur=(cur+1)%imgs.length;
imgs.forEach(function(m,k){m.classList.toggle('is-on',k===cur);});
dots.forEach(function(d,k){d.classList.toggle('is-on',k===cur);});
setTimeout(function(){busy=false;},reduce?0:2500);
});

/* the tree drifts a few pixels away from the cursor (desktop only) */
var fl=root.querySelector('.hm-float'),first=root.querySelector('.hm-first');
if(!reduce&&matchMedia('(hover:hover) and (pointer:fine)').matches){
first.addEventListener('pointermove',function(e){
var r=first.getBoundingClientRect(),x=(e.clientX-r.left)/r.width-.5,y=(e.clientY-r.top)/r.height-.5;
fl.style.transform='translate('+(x*-18).toFixed(1)+'px,'+(y*-12).toFixed(1)+'px)';});
first.addEventListener('pointerleave',function(){fl.style.transform='';});}
})();
</script>

<style>
/* let every ancestor grow wide, instead of the theme's narrow column */
*:has(.hm){max-width:none!important;width:100%!important;overflow:visible!important}
.hm{--ink:var(--heading-color,#111);--ink2:var(--blockquote-color,#555);--line:var(--rule-color,#ddd);
  box-sizing:border-box;width:100%;margin:0;padding:0 clamp(20px,5vw,72px) 16px;font-family:var(--font-body,Georgia,serif);color:var(--ink2)}
.hm *,.hm *::before,.hm *::after{box-sizing:border-box}
.hm-wrap{width:100%;max-width:1040px;margin:0 auto}

/* desktop: the tree on the left, the words on the right, a lot of quiet space */
.hm-first{display:grid;grid-template-columns:minmax(0,1.1fr) minmax(0,1fr);align-items:center;column-gap:clamp(32px,7vw,110px);
  min-height:calc(100svh - 150px);padding:clamp(12px,3vh,40px) 0}

.hm-tree{margin:0;justify-self:center;width:min(100%,480px,62svh);animation:hm-fade 2s ease both}
.hm-float{transition:transform 1.8s cubic-bezier(.2,.7,.2,1)}
.hm-treebtn{position:relative;display:block;width:100%;aspect-ratio:1/1;padding:0;border:0;background:none;cursor:pointer;-webkit-tap-highlight-color:transparent}
.hm-treebtn:focus-visible{outline:1px dashed var(--ink);outline-offset:6px}
/* the tree stays still. One tree fades away, a pause, then the next fades in: like one breath out, one breath in.
   No overlap, so you never see two trees ghosted together. */
.hm-treebtn>img{position:absolute;inset:0;display:block;width:100%;height:100%;margin:0;object-fit:contain;opacity:0;transition:opacity 1.1s ease-in-out}
.hm-treebtn>img.is-on{opacity:1;transition-delay:1.3s}
.hm-hint{display:flex;align-items:center;justify-content:center;gap:10px;margin-top:8px;font-family:var(--font-secondary,sans-serif);font-size:.8125rem;line-height:1;color:var(--ink2)}
.hm-dots{display:inline-flex;gap:6px}
.hm-dots i{width:7px;height:7px;border:1.5px solid var(--ink2);border-radius:50%;transition:background .5s ease}
.hm-dots i.is-on{background:var(--ink2)}

/* the poem: the quiet centre of the page, right under the tree */
.hm .hm-poemlink{display:block;margin-top:16px;text-align:center;font-family:var(--font-body,Georgia,serif);font-style:italic;font-size:1.0625rem;line-height:1.4;color:var(--ink);
  text-decoration:underline wavy;text-decoration-thickness:1px;text-decoration-color:var(--line);text-underline-offset:7px;transition:text-decoration-color .3s ease}
.hm .hm-poemlink:hover,.hm .hm-poemlink:focus-visible{color:var(--ink);text-decoration-color:var(--ink)}

.hm-hero{animation:hm-fade 2s .4s ease both}
.hm .hm-name{margin:0;font-family:var(--font-head,Georgia,serif);font-weight:600;font-size:clamp(2.4rem,4.8vw,3.75rem);line-height:1.12;letter-spacing:0;color:var(--ink)}
.hm-scrawl{display:block;width:170px;height:10px;margin:10px 0 28px;overflow:visible;fill:none;stroke:var(--ink);stroke-width:1.6;stroke-linecap:round;opacity:.7}
.hm-scrawl path{stroke-dasharray:1;stroke-dashoffset:1;vector-effect:non-scaling-stroke;animation:hm-draw 2s 1s ease forwards}
.hm .hm-lead{max-width:24em;margin:0 0 1.1em;font-size:clamp(1.1rem,1.9vw,1.35rem);line-height:1.6;color:var(--ink)}
.hm .hm-idea{max-width:24em;margin:0 0 1.1em;font-style:italic;font-size:1.0625rem;line-height:1.65;color:var(--ink2)}
.hm .hm-note{max-width:26em;margin:0;font-family:var(--font-secondary,sans-serif);font-size:.875rem;line-height:1.7;color:var(--ink2)}
.hm .hm-hl{background:linear-gradient(104deg,transparent .5%,rgba(255,200,60,.5) 2%,rgba(255,200,60,.5) 97%,transparent 99%);color:inherit;padding:.02em .2em;margin:0 -.1em;border-radius:.3em .6em .4em .5em;-webkit-box-decoration-break:clone;box-decoration-break:clone}

/* three quiet links (desktop only; the floating nav has them on phones) */
.hm .hm-roles{display:flex;flex-wrap:wrap;gap:4px 28px;margin:34px 0 0;padding:0;list-style:none}
.hm .hm-roles li{margin:0}
.hm .hm-roles a{display:inline-block;padding:4px 0;font-family:var(--font-head,Georgia,serif);font-weight:600;font-size:1.15rem;line-height:1.3;color:var(--ink);text-decoration:none;
  background:linear-gradient(currentColor,currentColor) no-repeat 0 94%/0 1px;transition:background-size .5s ease}
.hm .hm-roles a:hover,.hm .hm-roles a:focus-visible{background-size:100% 1px;color:var(--ink)}
.hm .hm-roles a:focus-visible{outline:1px dashed var(--ink);outline-offset:4px}

/* find me on: social links and email, small and quiet, shown on every screen size */
.hm .hm-find{max-width:26em;margin:30px 0 0;font-family:var(--font-secondary,sans-serif);font-size:.9375rem;line-height:1.9;color:var(--ink2)}
.hm .hm-find a{color:var(--ink);text-decoration:underline;text-decoration-color:var(--line);text-decoration-thickness:1.5px;text-underline-offset:4px;overflow-wrap:anywhere;transition:text-decoration-color .3s ease}
.hm .hm-find a:hover,.hm .hm-find a:focus-visible{color:var(--ink);text-decoration-color:var(--ink)}
.hm .hm-find a:focus-visible{outline:1px dashed var(--ink);outline-offset:3px}
.hm .hm-find span{padding:0 .35em;opacity:.5}

@keyframes hm-fade{from{opacity:0}to{opacity:1}}
@keyframes hm-draw{to{stroke-dashoffset:0}}

/* tablets and phones: tree first, then the words, one column */
@media (max-width:899px){
.hm-first{grid-template-columns:minmax(0,1fr);row-gap:28px;min-height:0;padding:8px 0 0}
.hm-tree{width:min(78vw,340px)}
.hm-hero{max-width:520px;width:100%;margin:0 auto}
.hm .hm-name{font-size:clamp(2.3rem,10vw,3rem)}
.hm .hm-lead{font-size:1.1875rem}
.hm .hm-roles{display:none}
.hm .hm-find{margin-top:22px;padding-bottom:72px}
}

/* dark mode: show the tree on a paper tile so the drawing stays visible */
html[data-theme="dark"] .hm-treebtn{background:#fff;border-radius:10px;overflow:hidden}
html[data-theme="dark"] .hm .hm-hl{color:#111}
@media (prefers-color-scheme:dark){
html:not([data-theme="light"]) .hm-treebtn{background:#fff;border-radius:10px;overflow:hidden}
html:not([data-theme="light"]) .hm .hm-hl{color:#111}
}

@media (prefers-reduced-motion:reduce){
.hm-tree,.hm-hero{animation:none}
.hm-scrawl path{animation:none;stroke-dashoffset:0}
.hm-float,.hm-treebtn>img,.hm-dots i,.hm .hm-roles a,.hm .hm-poemlink,.hm .hm-find a{transition:none}
}
</style>