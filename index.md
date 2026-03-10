---
layout: default
title: Poway Woman's Club
hide: true
show_reading_time: false
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&family=Nunito+Sans:wght@300;400;600;700&display=swap');

  :root {
    --pwc-cream: #fbf8f6;
    --pwc-sage: #7a8e6b;
    --pwc-sage-dark: #5c6e50;
    --pwc-sage-light: #dde6d5;
    --pwc-rose: #c4788a;
    --pwc-rose-dark: #a25d6e;
    --pwc-rose-light: #f2dce2;
    --pwc-warm: #c9a070;
    --pwc-warm-light: #f5ede4;
    --pwc-charcoal: #342e30;
    --pwc-text: #504a4c;
    --pwc-muted: #928a8c;
    --pwc-border: #e8dfe2;
    --pwc-white: #ffffff;
  }

  /* ── Hero ── */
  .pwc-hero {
    position: relative;
    padding: 5rem 2rem 4rem;
    text-align: center;
    background: linear-gradient(135deg, var(--pwc-sage-light) 0%, var(--pwc-cream) 40%, var(--pwc-rose-light) 100%);
    border-bottom: 3px solid var(--pwc-warm);
    overflow: hidden;
  }

  .pwc-hero::before {
    content: '';
    position: absolute;
    top: -60px;
    right: -60px;
    width: 260px;
    height: 260px;
    border-radius: 50%;
    background: rgba(122, 142, 107, 0.1);
    pointer-events: none;
  }

  .pwc-hero::after {
    content: '';
    position: absolute;
    bottom: -40px;
    left: -40px;
    width: 180px;
    height: 180px;
    border-radius: 50%;
    background: rgba(196, 120, 138, 0.09);
    pointer-events: none;
  }

  .pwc-hero-badge {
    display: inline-block;
    padding: 0.3rem 1rem;
    background: var(--pwc-sage);
    color: var(--pwc-white);
    border-radius: 999px;
    font-family: 'Nunito Sans', sans-serif;
    font-size: 0.75rem;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 1.25rem;
    animation: fadeDown 0.6s ease both;
  }

  .pwc-hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: 3rem;
    font-weight: 700;
    color: var(--pwc-charcoal);
    line-height: 1.15;
    margin-bottom: 1rem;
    animation: fadeDown 0.6s 0.1s ease both;
  }

  .pwc-hero h1 em {
    color: var(--pwc-rose);
    font-style: italic;
  }

  .pwc-hero-sub {
    font-family: 'Nunito Sans', sans-serif;
    font-size: 1.1rem;
    font-weight: 300;
    color: var(--pwc-text);
    max-width: 560px;
    margin: 0 auto 2rem;
    line-height: 1.65;
    animation: fadeDown 0.6s 0.2s ease both;
  }

  .pwc-hero-actions {
    display: flex;
    justify-content: center;
    gap: 1rem;
    flex-wrap: wrap;
    animation: fadeDown 0.6s 0.3s ease both;
  }

  .pwc-btn {
    display: inline-block;
    padding: 0.75rem 1.8rem;
    border-radius: 8px;
    font-family: 'Nunito Sans', sans-serif;
    font-size: 0.9rem;
    font-weight: 700;
    text-decoration: none;
    transition: all 0.25s ease;
    cursor: pointer;
  }

  .pwc-btn-primary {
    background: linear-gradient(135deg, var(--pwc-sage) 0%, var(--pwc-rose) 100%);
    color: var(--pwc-white);
    border: 2px solid transparent;
  }

  .pwc-btn-primary:hover {
    background: linear-gradient(135deg, var(--pwc-sage-dark) 0%, var(--pwc-rose-dark) 100%);
    border-color: transparent;
    transform: translateY(-2px);
    box-shadow: 0 4px 12px rgba(160,120,120,0.3);
  }

  .pwc-btn-outline {
    background: transparent;
    color: var(--pwc-rose-dark);
    border: 2px solid var(--pwc-rose);
  }

  .pwc-btn-outline:hover {
    background: var(--pwc-rose);
    color: var(--pwc-white);
    transform: translateY(-2px);
  }

  /* ── Sections ── */
  .pwc-section {
    padding: 3.5rem 2rem;
    max-width: 960px;
    margin: 0 auto;
  }

  .pwc-section-label {
    font-family: 'Nunito Sans', sans-serif;
    font-size: 0.7rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.15em;
    color: var(--pwc-sage);
    margin-bottom: 0.5rem;
  }

  .pwc-section h2 {
    font-family: 'Playfair Display', serif;
    font-size: 2rem;
    font-weight: 600;
    color: var(--pwc-charcoal);
    margin-bottom: 1rem;
    line-height: 1.2;
  }

  .pwc-section p {
    font-family: 'Nunito Sans', sans-serif;
    font-size: 1rem;
    color: var(--pwc-text);
    line-height: 1.75;
    margin-bottom: 1rem;
  }

  .pwc-divider {
    width: 50px;
    height: 3px;
    background: var(--pwc-warm);
    border: none;
    margin: 0 0 2rem;
    border-radius: 2px;
  }

  /* ── Card Grid ── */
  .pwc-cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 1.5rem;
    margin-top: 1.5rem;
  }

  .pwc-card {
    background: var(--pwc-white);
    border: 1px solid var(--pwc-border);
    border-radius: 10px;
    padding: 1.5rem;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }

  .pwc-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 20px rgba(0,0,0,0.06);
  }

  .pwc-card-icon {
    font-size: 1.8rem;
    margin-bottom: 0.75rem;
  }

  .pwc-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.15rem;
    color: var(--pwc-charcoal);
    margin-bottom: 0.5rem;
  }

  .pwc-card p {
    font-family: 'Nunito Sans', sans-serif;
    font-size: 0.88rem;
    color: var(--pwc-muted);
    line-height: 1.6;
    margin: 0;
  }

  /* ── Quick Facts ── */
  .pwc-facts {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 1rem;
    margin-top: 1.5rem;
  }

  .pwc-fact {
    text-align: center;
    padding: 1.25rem 1rem;
    background: var(--pwc-sage-light);
    border-radius: 10px;
  }

  .pwc-fact-value {
    font-family: 'Playfair Display', serif;
    font-size: 1.6rem;
    font-weight: 700;
    color: var(--pwc-sage-dark);
    display: block;
  }

  .pwc-fact-label {
    font-family: 'Nunito Sans', sans-serif;
    font-size: 0.78rem;
    color: var(--pwc-text);
    margin-top: 0.25rem;
    display: block;
  }

  /* ── CTA Banner ── */
  .pwc-cta {
    background: linear-gradient(135deg, var(--pwc-sage) 0%, var(--pwc-rose) 100%);
    padding: 3rem 2rem;
    text-align: center;
    border-radius: 12px;
    margin: 2rem auto;
    max-width: 960px;
  }

  .pwc-cta h2 {
    font-family: 'Playfair Display', serif;
    font-size: 1.8rem;
    color: var(--pwc-white);
    margin-bottom: 0.75rem;
  }

  .pwc-cta p {
    font-family: 'Nunito Sans', sans-serif;
    font-size: 1rem;
    color: rgba(255,255,255,0.85);
    margin-bottom: 1.5rem;
  }

  .pwc-btn-white {
    background: var(--pwc-white);
    color: var(--pwc-sage-dark);
    border: 2px solid var(--pwc-white);
  }

  .pwc-btn-white:hover {
    background: transparent;
    color: var(--pwc-white);
    transform: translateY(-2px);
  }

  /* ── Animations ── */
  @keyframes fadeDown {
    from { opacity: 0; transform: translateY(-12px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* ── Dark mode overrides (Minima dark skin) ── */
  @media (prefers-color-scheme: dark) {
    .pwc-hero { background: linear-gradient(135deg, #252e22 0%, #1e1a1b 40%, #2e2228 100%); border-color: var(--pwc-warm); }
    .pwc-hero h1 { color: #eae8e6; }
    .pwc-hero-sub { color: #b8b2b4; }
    .pwc-section h2 { color: #eae8e6; }
    .pwc-section p { color: #b8b2b4; }
    .pwc-card { background: #26242a; border-color: #3a3438; }
    .pwc-card h3 { color: #eae6e8; }
    .pwc-card p { color: #9a9498; }
    .pwc-fact { background: linear-gradient(135deg, #2a3025 0%, #302428 100%); }
    .pwc-fact-value { color: var(--pwc-rose-light); }
    .pwc-fact-label { color: #b8b2b4; }
    .pwc-btn-outline { color: var(--pwc-rose-light); border-color: var(--pwc-rose-light); }
    .pwc-btn-outline:hover { background: var(--pwc-rose-light); color: var(--pwc-charcoal); }
  }
</style>

<!-- ════════ HERO ════════ -->
<div class="pwc-hero">
  <div class="pwc-hero-badge">Serving Poway Since 1960</div>
  <h1>Poway Woman's <em>Club</em></h1>
  <p class="pwc-hero-sub">
    A nonprofit community of women dedicated to scholarships, the arts, civic engagement, and making Poway a better place to live.
  </p>
  <div class="pwc-hero-actions">
    <a href="{{ site.baseurl }}/navigation/about" class="pwc-btn pwc-btn-primary">Learn About Us</a>
    <a href="{{ site.baseurl }}/navigation/events" class="pwc-btn pwc-btn-outline">Upcoming Events</a>
  </div>
</div>

<!-- ════════ QUICK FACTS ════════ -->
<div class="pwc-section">
  <div class="pwc-section-label">At a Glance</div>
  <h2>65 Years of Community Service</h2>
  <hr class="pwc-divider">
  <div class="pwc-facts">
    <div class="pwc-fact">
      <span class="pwc-fact-value">1960</span>
      <span class="pwc-fact-label">Founded</span>
    </div>
    <div class="pwc-fact">
      <span class="pwc-fact-value">501(c)(3)</span>
      <span class="pwc-fact-label">Nonprofit Status</span>
    </div>
    <div class="pwc-fact">
      <span class="pwc-fact-value">GFWC</span>
      <span class="pwc-fact-label">International Affiliation</span>
    </div>
    <div class="pwc-fact">
      <span class="pwc-fact-value">2nd Tue</span>
      <span class="pwc-fact-label">Monthly Meetings, Sept–June</span>
    </div>
  </div>
</div>

<!-- ════════ WHAT WE DO ════════ -->
<div class="pwc-section">
  <div class="pwc-section-label">What We Do</div>
  <h2>Building a Stronger Poway</h2>
  <hr class="pwc-divider">
  <p>
    The Poway Woman's Club supports local organizations, awards scholarships to students at four area high schools, sponsors art exhibits, and champions youth leadership — all through the volunteer spirit of its members.
  </p>
  <div class="pwc-cards">
    <div class="pwc-card">
      <div class="pwc-card-icon">🎓</div>
      <h3>Scholarships</h3>
      <p>HOBY Youth Leadership awards to Poway, Mt. Carmel, Rancho Bernardo, and Westview High students, plus continuing education scholarships.</p>
    </div>
    <div class="pwc-card">
      <div class="pwc-card-icon">🎨</div>
      <h3>Arts &amp; Culture</h3>
      <p>"Celebrate Women" Art Exhibit, Student Art Exhibit, and Theatre in the Park bring creative energy to the community year-round.</p>
    </div>
    <div class="pwc-card">
      <div class="pwc-card-icon">📚</div>
      <h3>Library &amp; Civic</h3>
      <p>Adopted the Poway Community Library, supporting staff, programs, and the Friends of the Poway Library initiative.</p>
    </div>
    <div class="pwc-card">
      <div class="pwc-card-icon">🤝</div>
      <h3>Community Partners</h3>
      <p>Active members of Old Poway Park Action Committee, PowPAC, Poway Historical Society, and the Weingart Senior Center.</p>
    </div>
  </div>
</div>

<!-- ════════ CTA ════════ -->
<div class="pwc-cta">
  <h2>Ready to Make a Difference?</h2>
  <p>Join a community of women who are building friendships, supporting local causes, and shaping the future of Poway.</p>
  <a href="{{ site.baseurl }}/navigation/contact" class="pwc-btn pwc-btn-white">Get In Touch</a>
</div>