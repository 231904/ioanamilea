---
layout: default
title: Volunteering
permalink: /volunteering/
---

# Volunteering / Outreach

Community and outreach work. Click a banner to read more.

<style>
.vol-grid, .vol-modal {
  --vol-cream: #eadfca;
  --vol-ink: #1a120d;
  --vol-muted: #6e5b45;
  --vol-card: #241912;
  --vol-line: rgba(234, 223, 202, 0.28);
  --vol-radius: 18px;
}

/* ---------- Panels: masonry columns, so photos of any size fit ---------- */
.vol-grid {
  column-count: 3;
  column-gap: 22px;
  margin: 28px 0 8px;
}
.vol-grid .vol-card {
  display: block;
  margin: 0 0 22px;
  break-inside: avoid;
  -webkit-column-break-inside: avoid;
  background: var(--vol-card);
  border: 1px solid var(--vol-line);
  border-radius: var(--vol-radius);
  overflow: hidden;
  transition: border-color 0.3s ease, box-shadow 0.3s ease;
}
.vol-grid .vol-card:hover {
  border-color: var(--vol-cream);
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.35);
}
.vol-grid .vol-img {
  overflow: hidden;
  min-height: 120px;
  background: rgba(234, 223, 202, 0.08);
}
.vol-grid .vol-img img {
  display: block;
  width: 100%;
  height: auto;
  margin: 0 !important;
  border: 0 !important;
  border-radius: 0 !important;
  transition: transform 0.6s cubic-bezier(0.2, 0.8, 0.2, 1);
}
.vol-grid .vol-card:hover .vol-img img { transform: scale(1.04); }

/* ---------- Cream banner under the picture ---------- */
.vol-grid .vol-banner {
  -webkit-appearance: none;
  appearance: none;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 14px;
  width: 100%;
  margin: 0;
  padding: 14px 18px;
  border: 0;
  border-radius: 0;
  background: var(--vol-cream);
  color: var(--vol-ink);
  font: inherit;
  text-align: left;
  cursor: pointer;
  transition: background-color 0.25s ease;
}
.vol-grid .vol-banner:hover { background: #f3eadb; }
.vol-grid .vol-banner:focus-visible { outline: 2px solid var(--vol-ink); outline-offset: -5px; }
.vol-grid .vol-text { display: flex; flex-direction: column; gap: 2px; min-width: 0; }
.vol-grid .vol-title {
  font-family: var(--serif, Georgia, "Times New Roman", serif);
  font-size: 19px;
  font-weight: 600;
  line-height: 1.2;
  color: var(--vol-ink);
}
.vol-grid .vol-period {
  font-family: var(--sans, system-ui, -apple-system, "Segoe UI", sans-serif);
  font-size: 11.5px;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--vol-muted);
}
.vol-grid .vol-plus {
  flex: 0 0 auto;
  font-family: var(--sans, system-ui, sans-serif);
  font-size: 22px;
  line-height: 1;
  color: var(--vol-ink);
  transition: transform 0.3s ease;
}
.vol-grid .vol-banner:hover .vol-plus { transform: rotate(90deg); }

/* ---------- Popup ---------- */
.vol-modal {
  position: fixed;
  inset: 0;
  z-index: 9999;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 24px;
  background: rgba(12, 7, 4, 0.74);
  -webkit-backdrop-filter: blur(5px);
  backdrop-filter: blur(5px);
  opacity: 0;
  visibility: hidden;
  transition: opacity 0.3s ease, visibility 0s linear 0.3s;
}
.vol-modal.open {
  opacity: 1;
  visibility: visible;
  transition: opacity 0.3s ease, visibility 0s linear 0s;
}
.vol-modal .vol-panel {
  position: relative;
  width: min(620px, 100%);
  max-height: 84vh;
  overflow-y: auto;
  padding: 32px 34px 30px;
  background: var(--vol-cream);
  border-radius: var(--vol-radius);
  box-shadow: 0 24px 70px rgba(0, 0, 0, 0.5);
  transform: translateY(22px) scale(0.96);
  opacity: 0;
  transition: transform 0.4s cubic-bezier(0.2, 0.8, 0.2, 1), opacity 0.3s ease;
}
.vol-modal.open .vol-panel { transform: none; opacity: 1; }
.vol-modal .vol-panel,
.vol-modal .vol-panel p,
.vol-modal .vol-panel li,
.vol-modal .vol-panel div { color: var(--vol-ink); }
.vol-modal .vol-panel a { color: #6b3f1d !important; }
.vol-modal .vol-modal-head {
  padding-bottom: 14px;
  margin-bottom: 16px;
  border-bottom: 1px solid rgba(26, 18, 13, 0.18);
}
.vol-modal .vol-modal-title {
  padding-right: 40px;
  font-family: var(--serif, Georgia, "Times New Roman", serif);
  font-size: clamp(24px, 4vw, 32px);
  font-weight: 600;
  line-height: 1.15;
}
.vol-modal .vol-panel .vol-modal-period {
  margin-top: 6px;
  font-family: var(--sans, system-ui, sans-serif);
  font-size: 12px;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--vol-muted);
}
.vol-modal .vol-modal-body { font-size: 15.5px; line-height: 1.7; }
.vol-modal .vol-modal-body p { margin: 0 0 12px; max-width: none; }
.vol-modal .vol-modal-body ul { margin: 0 0 12px; padding-left: 1.2em; }
.vol-modal .vol-close {
  position: absolute;
  top: 14px;
  right: 14px;
  width: 36px;
  height: 36px;
  padding: 0;
  border: 1px solid rgba(26, 18, 13, 0.3);
  border-radius: 50%;
  background: transparent;
  color: var(--vol-ink);
  font-size: 22px;
  line-height: 1;
  cursor: pointer;
  transition: background-color 0.2s ease, color 0.2s ease;
}
.vol-modal .vol-panel .vol-close:hover { background: var(--vol-ink); color: var(--vol-cream); }
.vol-modal .vol-close:focus-visible { outline: 2px solid var(--vol-ink); outline-offset: 2px; }

@media (max-width: 900px) { .vol-grid { column-count: 2; } }
@media (max-width: 560px) {
  .vol-grid { column-count: 1; }
  .vol-modal { padding: 14px; }
  .vol-modal .vol-panel { padding: 26px 22px 22px; }
}
@media (prefers-reduced-motion: reduce) {
  .vol-modal,
  .vol-modal .vol-panel,
  .vol-grid .vol-card,
  .vol-grid .vol-img img,
  .vol-grid .vol-plus { transition: none; }
  .vol-grid .vol-card:hover .vol-img img { transform: none; }
}
</style>

<div class="vol-grid">
<article class="vol-card">
<div class="vol-img"><img src="{{ '/assets/vol1.jpg' | relative_url }}" alt="Describe this photo" loading="lazy"></div>
<button type="button" class="vol-banner" aria-haspopup="dialog"><span class="vol-text"><span class="vol-title">Coding Mentor</span><span class="vol-period">2025 – present</span></span><span class="vol-plus" aria-hidden="true">+</span></button>
<div class="vol-desc" hidden>
<p>Placeholder description. Who you worked with, what you did, and what you learned from it.</p>
<p>Add as many paragraphs as you like, or a bullet list.</p>
</div>
</article>
<article class="vol-card">
<div class="vol-img"><img src="{{ '/assets/vol2.jpg' | relative_url }}" alt="Describe this photo" loading="lazy"></div>
<button type="button" class="vol-banner" aria-haspopup="dialog"><span class="vol-text"><span class="vol-title">Event Volunteer</span><span class="vol-period">2024</span></span><span class="vol-plus" aria-hidden="true">+</span></button>
<div class="vol-desc" hidden>
<p>Placeholder description of the event and your role.</p>
</div>
</article>
<article class="vol-card">
<div class="vol-img"><img src="{{ '/assets/vol3.jpg' | relative_url }}" alt="Describe this photo" loading="lazy"></div>
<button type="button" class="vol-banner" aria-haspopup="dialog"><span class="vol-text"><span class="vol-title">Outreach Lead</span><span class="vol-period">2023 – 2024</span></span><span class="vol-plus" aria-hidden="true">+</span></button>
<div class="vol-desc" hidden>
<p>Placeholder description of the initiatives you ran.</p>
<ul>
<li>A first thing you did</li>
<li>A second thing you did</li>
</ul>
</div>
</article>
<article class="vol-card">
<div class="vol-img"><img src="{{ '/assets/vol4.jpg' | relative_url }}" alt="Describe this photo" loading="lazy"></div>
<button type="button" class="vol-banner" aria-haspopup="dialog"><span class="vol-text"><span class="vol-title">Outreach Lead</span><span class="vol-period">2023 – 2024</span></span><span class="vol-plus" aria-hidden="true">+</span></button>
<div class="vol-desc" hidden>
<p>Placeholder description of the initiatives you ran.</p>
<ul>
<li>A first thing you did</li>
<li>A second thing you did</li>
</ul>
</div>
</article>
</div>

<script>
(function () {
  var cards = document.querySelectorAll('.vol-card');
  if (!cards.length) return;

  var modal = document.createElement('div');
  modal.className = 'vol-modal';
  modal.innerHTML =
    '<div class="vol-panel" role="dialog" aria-modal="true" aria-labelledby="vol-modal-title">' +
      '<button type="button" class="vol-close" aria-label="Close">×</button>' +
      '<div class="vol-modal-head">' +
        '<div class="vol-modal-title" id="vol-modal-title"></div>' +
        '<div class="vol-modal-period"></div>' +
      '</div>' +
      '<div class="vol-modal-body"></div>' +
    '</div>';
  document.body.appendChild(modal);

  var panel = modal.querySelector('.vol-panel');
  var closeBtn = modal.querySelector('.vol-close');
  var titleEl = modal.querySelector('.vol-modal-title');
  var periodEl = modal.querySelector('.vol-modal-period');
  var bodyEl = modal.querySelector('.vol-modal-body');
  var opener = null;

  function openModal(card, trigger) {
    var title = card.querySelector('.vol-title');
    var period = card.querySelector('.vol-period');
    var desc = card.querySelector('.vol-desc');
    titleEl.textContent = title ? title.textContent : '';
    periodEl.textContent = period ? period.textContent : '';
    bodyEl.innerHTML = desc ? desc.innerHTML : '';
    panel.scrollTop = 0;
    opener = trigger;
    var gap = window.innerWidth - document.documentElement.clientWidth;
    document.documentElement.style.overflow = 'hidden';
    if (gap > 0) document.body.style.paddingRight = gap + 'px';
    modal.classList.add('open');
    closeBtn.focus({ preventScroll: true });
  }

  function closeModal() {
    if (!modal.classList.contains('open')) return;
    modal.classList.remove('open');
    document.documentElement.style.overflow = '';
    document.body.style.paddingRight = '';
    if (opener) opener.focus({ preventScroll: true });
  }

  Array.prototype.forEach.call(cards, function (card) {
    var btn = card.querySelector('.vol-banner');
    if (btn) btn.addEventListener('click', function () { openModal(card, btn); });
  });

  closeBtn.addEventListener('click', closeModal);
  modal.addEventListener('click', function (e) { if (e.target === modal) closeModal(); });

  document.addEventListener('keydown', function (e) {
    if (!modal.classList.contains('open')) return;
    if (e.key === 'Escape') {
      closeModal();
    } else if (e.key === 'Tab') {
      var items = panel.querySelectorAll('a[href], button');
      var first = items[0];
      var last = items[items.length - 1];
      if (e.shiftKey && document.activeElement === first) { e.preventDefault(); last.focus(); }
      else if (!e.shiftKey && document.activeElement === last) { e.preventDefault(); first.focus(); }
    }
  });
})();
</script>
