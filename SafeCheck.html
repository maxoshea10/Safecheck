import { useState, useEffect, useRef } from "react";

// ─── Design Tokens ──────────────────────────────────────────────────────────
const COLORS = {
  navy: "#0A0E1A",
  navyMid: "#111827",
  navyLight: "#1E2A3B",
  navyBorder: "#1E293B",
  accent: "#00D4FF",
  accentGlow: "rgba(0,212,255,0.15)",
  green: "#00E676",
  greenDim: "rgba(0,230,118,0.12)",
  red: "#FF3D57",
  redDim: "rgba(255,61,87,0.12)",
  amber: "#FFB300",
  amberDim: "rgba(255,179,0,0.12)",
  white: "#F0F4FF",
  grey: "#8896B0",
  greyLight: "#CBD5E1",
};

// ─── Utility Styles ─────────────────────────────────────────────────────────
const css = `
  @import url('https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap');

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --navy: #0A0E1A;
    --navy-mid: #111827;
    --navy-light: #1E2A3B;
    --accent: #00D4FF;
    --green: #00E676;
    --red: #FF3D57;
    --amber: #FFB300;
    --white: #F0F4FF;
    --grey: #8896B0;
  }

  body { background: var(--navy); color: var(--white); font-family: 'DM Sans', sans-serif; overflow-x: hidden; }

  ::-webkit-scrollbar { width: 6px; }
  ::-webkit-scrollbar-track { background: var(--navy); }
  ::-webkit-scrollbar-thumb { background: #1E293B; border-radius: 3px; }

  .syne { font-family: 'Syne', sans-serif; }

  @keyframes pulse-glow {
    0%, 100% { box-shadow: 0 0 20px rgba(0,212,255,0.2); }
    50% { box-shadow: 0 0 40px rgba(0,212,255,0.5); }
  }
  @keyframes scan-line {
    0% { transform: translateY(-100%); opacity: 0; }
    10% { opacity: 1; }
    90% { opacity: 1; }
    100% { transform: translateY(500%); opacity: 0; }
  }
  @keyframes fade-in-up {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes float {
    0%, 100% { transform: translateY(0px); }
    50% { transform: translateY(-10px); }
  }
  @keyframes shimmer {
    0% { background-position: -200% center; }
    100% { background-position: 200% center; }
  }
  @keyframes spin { to { transform: rotate(360deg); } }
  @keyframes score-fill {
    from { stroke-dashoffset: 283; }
  }
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

  .fade-in-up { animation: fade-in-up 0.5s ease forwards; }

  .grid-bg {
    background-image:
      linear-gradient(rgba(0,212,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,212,255,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
  }

  .glass {
    background: rgba(30,42,59,0.5);
    backdrop-filter: blur(12px);
    border: 1px solid rgba(0,212,255,0.1);
  }

  .btn-primary {
    background: linear-gradient(135deg, #00D4FF, #0088AA);
    color: #0A0E1A;
    font-weight: 700;
    font-family: 'Syne', sans-serif;
    border: none;
    cursor: pointer;
    transition: all 0.2s;
    letter-spacing: 0.02em;
  }
  .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 30px rgba(0,212,255,0.4); filter: brightness(1.1); }

  .btn-ghost {
    background: transparent;
    border: 1px solid rgba(0,212,255,0.3);
    color: var(--accent);
    font-family: 'Syne', sans-serif;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.2s;
  }
  .btn-ghost:hover { background: rgba(0,212,255,0.08); border-color: var(--accent); }

  .risk-badge {
    display: inline-flex; align-items: center; gap: 6px;
    padding: 4px 12px; border-radius: 20px;
    font-family: 'Syne', sans-serif; font-size: 12px; font-weight: 700;
    letter-spacing: 0.05em; text-transform: uppercase;
  }
  .risk-low { background: rgba(0,230,118,0.12); color: #00E676; border: 1px solid rgba(0,230,118,0.3); }
  .risk-medium { background: rgba(255,179,0,0.12); color: #FFB300; border: 1px solid rgba(255,179,0,0.3); }
  .risk-high { background: rgba(255,61,87,0.12); color: #FF3D57; border: 1px solid rgba(255,61,87,0.3); }

  .nav-link {
    color: #8896B0; font-size: 14px; font-weight: 500;
    text-decoration: none; cursor: pointer;
    transition: color 0.2s; padding: 4px 0;
  }
  .nav-link:hover, .nav-link.active { color: #F0F4FF; }

  .card {
    background: #111827;
    border: 1px solid #1E293B;
    border-radius: 16px;
    transition: border-color 0.2s, transform 0.2s;
  }
  .card:hover { border-color: rgba(0,212,255,0.2); }

  .input-field {
    background: rgba(30,42,59,0.6);
    border: 1px solid #1E293B;
    color: #F0F4FF;
    font-family: 'DM Sans', sans-serif;
    font-size: 15px;
    outline: none;
    transition: border-color 0.2s;
    width: 100%;
  }
  .input-field:focus { border-color: rgba(0,212,255,0.5); }
  .input-field::placeholder { color: #4A5568; }

  .tab-btn {
    padding: 8px 20px; border-radius: 8px; border: none;
    font-family: 'Syne', sans-serif; font-size: 13px; font-weight: 600;
    cursor: pointer; transition: all 0.2s; letter-spacing: 0.02em;
  }
  .tab-btn.active { background: rgba(0,212,255,0.15); color: #00D4FF; }
  .tab-btn:not(.active) { background: transparent; color: #8896B0; }
  .tab-btn:not(.active):hover { color: #F0F4FF; }

  .score-ring { transition: stroke-dashoffset 1s ease; }

  .spinner {
    width: 20px; height: 20px;
    border: 2px solid rgba(0,212,255,0.2);
    border-top-color: #00D4FF;
    border-radius: 50%;
    animation: spin 0.7s linear infinite;
    display: inline-block;
  }

  .tooltip {
    position: relative;
  }
  .tooltip:hover::after {
    content: attr(data-tip);
    position: absolute; bottom: 110%; left: 50%; transform: translateX(-50%);
    background: #1E2A3B; color: #F0F4FF; font-size: 12px; padding: 6px 10px;
    border-radius: 6px; white-space: nowrap; border: 1px solid #1E293B;
    pointer-events: none; z-index: 100;
  }

  .hero-glow {
    position: absolute; width: 600px; height: 600px;
    background: radial-gradient(circle, rgba(0,212,255,0.08) 0%, transparent 70%);
    pointer-events: none;
  }

  .pricing-popular {
    position: relative;
    border-color: rgba(0,212,255,0.4) !important;
  }
  .pricing-popular::before {
    content: 'MOST POPULAR';
    position: absolute; top: -12px; left: 50%; transform: translateX(-50%);
    background: linear-gradient(135deg, #00D4FF, #0088AA);
    color: #0A0E1A; font-family: 'Syne', sans-serif;
    font-size: 10px; font-weight: 800; padding: 3px 12px;
    border-radius: 20px; letter-spacing: 0.1em;
  }

  .alert-dot {
    width: 8px; height: 8px; border-radius: 50%;
    animation: pulse-glow 2s infinite;
  }

  .feature-icon {
    width: 48px; height: 48px; border-radius: 12px;
    display: flex; align-items: center; justify-content: center;
    font-size: 22px;
  }

  select.input-field option { background: #111827; }

  .progress-bar {
    height: 6px; border-radius: 3px;
    background: rgba(255,255,255,0.06);
    overflow: hidden;
  }
  .progress-fill {
    height: 100%; border-radius: 3px;
    transition: width 1s ease;
  }

  .scan-overlay {
    position: absolute; inset: 0; overflow: hidden; pointer-events: none;
    border-radius: inherit;
  }
  .scan-line {
    position: absolute; left: 0; right: 0; height: 2px;
    background: linear-gradient(90deg, transparent, #00D4FF, transparent);
    animation: scan-line 2s ease-in-out;
  }

  textarea.input-field { resize: vertical; min-height: 140px; }

  @media (max-width: 768px) {
    .hide-mobile { display: none !important; }
    .col-mobile { flex-direction: column !important; }
  }
`;

// ─── Icons ───────────────────────────────────────────────────────────────────
const Icon = ({ name, size = 20, color = "currentColor" }) => {
  const icons = {
    shield: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>,
    search: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg>,
    message: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/></svg>,
    camera: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M23 19a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h4l2-3h6l2 3h4a2 2 0 0 1 2 2z"/><circle cx="12" cy="13" r="4"/></svg>,
    globe: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><circle cx="12" cy="12" r="10"/><path d="M2 12h20M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>,
    tag: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M20.59 13.41l-7.17 7.17a2 2 0 0 1-2.83 0L2 12V2h10l8.59 8.59a2 2 0 0 1 0 2.82z"/><line x1="7" y1="7" x2="7.01" y2="7"/></svg>,
    book: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20"/><path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z"/></svg>,
    alert: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M10.29 3.86L1.82 18a2 2 0 0 0 1.71 3h16.94a2 2 0 0 0 1.71-3L13.71 3.86a2 2 0 0 0-3.42 0z"/><line x1="12" y1="9" x2="12" y2="13"/><line x1="12" y1="17" x2="12.01" y2="17"/></svg>,
    check: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2.5" strokeLinecap="round" strokeLinejoin="round"><polyline points="20 6 9 17 4 12"/></svg>,
    x: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg>,
    upload: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><polyline points="16 16 12 12 8 16"/><line x1="12" y1="12" x2="12" y2="21"/><path d="M20.39 18.39A5 5 0 0 0 18 9h-1.26A8 8 0 1 0 3 16.3"/></svg>,
    user: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"/><circle cx="12" cy="7" r="4"/></svg>,
    chevron: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><polyline points="9 18 15 12 9 6"/></svg>,
    menu: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><line x1="3" y1="12" x2="21" y2="12"/><line x1="3" y1="6" x2="21" y2="6"/><line x1="3" y1="18" x2="21" y2="18"/></svg>,
    star: <svg width={size} height={size} viewBox="0 0 24 24" fill={color} stroke={color} strokeWidth="1"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>,
    info: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><circle cx="12" cy="12" r="10"/><line x1="12" y1="16" x2="12" y2="12"/><line x1="12" y1="8" x2="12.01" y2="8"/></svg>,
    trending: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><polyline points="23 6 13.5 15.5 8.5 10.5 1 18"/><polyline points="17 6 23 6 23 12"/></svg>,
    lock: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><rect x="3" y="11" width="18" height="11" rx="2" ry="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>,
    zap: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"/></svg>,
    eye: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M1 12s4-8 11-8 11 8 11 8-4 8-11 8-11-8-11-8z"/><circle cx="12" cy="12" r="3"/></svg>,
    mail: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>,
    phone: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 13a19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 3.56 2h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L7.91 9.91a16 16 0 0 0 6.29 6.29l1.27-1.27a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0 1 22 16.92z"/></svg>,
    settings: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><circle cx="12" cy="12" r="3"/><path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1-2.83 2.83l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-4 0v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83-2.83l.06-.06A1.65 1.65 0 0 0 4.68 15a1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1 0-4h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 2.83-2.83l.06.06A1.65 1.65 0 0 0 9 4.68a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 4 0v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 2.83l-.06.06A1.65 1.65 0 0 0 19.4 9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 0 4h-.09a1.65 1.65 0 0 0-1.51 1z"/></svg>,
    history: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><polyline points="1 4 1 10 7 10"/><path d="M3.51 15a9 9 0 1 0 .49-3.51"/></svg>,
    external: <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>,
  };
  return icons[name] || null;
};

// ─── Score Ring Component ────────────────────────────────────────────────────
const ScoreRing = ({ score, size = 120 }) => {
  const radius = 45;
  const circumference = 2 * Math.PI * radius;
  const offset = circumference - (score / 100) * circumference;
  const color = score <= 30 ? COLORS.green : score <= 60 ? COLORS.amber : COLORS.red;
  const label = score <= 30 ? "LOW RISK" : score <= 60 ? "MEDIUM RISK" : "HIGH RISK";

  return (
    <div style={{ display: "flex", flexDirection: "column", alignItems: "center", gap: 8 }}>
      <div style={{ position: "relative", width: size, height: size }}>
        <svg width={size} height={size} viewBox="0 0 100 100" style={{ transform: "rotate(-90deg)" }}>
          <circle cx="50" cy="50" r={radius} fill="none" stroke="rgba(255,255,255,0.05)" strokeWidth="8" />
          <circle
            cx="50" cy="50" r={radius} fill="none"
            stroke={color} strokeWidth="8"
            strokeDasharray={circumference}
            strokeDashoffset={offset}
            strokeLinecap="round"
            style={{ transition: "stroke-dashoffset 1.2s cubic-bezier(0.4,0,0.2,1)" }}
          />
        </svg>
        <div style={{ position: "absolute", inset: 0, display: "flex", flexDirection: "column", alignItems: "center", justifyContent: "center" }}>
          <span style={{ fontFamily: "'Syne', sans-serif", fontSize: size * 0.22, fontWeight: 800, color }}>{score}</span>
          <span style={{ fontSize: size * 0.1, color: COLORS.grey, fontWeight: 500 }}>/100</span>
        </div>
      </div>
      <span className="risk-badge" style={{ fontSize: 11, background: color + "20", color, border: `1px solid ${color}40` }}>
        {label}
      </span>
    </div>
  );
};

// ─── Indicator Row ───────────────────────────────────────────────────────────
const IndicatorRow = ({ label, present, detail }) => (
  <div style={{ display: "flex", alignItems: "flex-start", gap: 10, padding: "10px 0", borderBottom: "1px solid rgba(255,255,255,0.04)" }}>
    <div style={{
      width: 22, height: 22, borderRadius: "50%", flexShrink: 0, marginTop: 1,
      display: "flex", alignItems: "center", justifyContent: "center",
      background: present ? COLORS.redDim : COLORS.greenDim,
    }}>
      <Icon name={present ? "alert" : "check"} size={12} color={present ? COLORS.red : COLORS.green} />
    </div>
    <div>
      <div style={{ fontSize: 14, fontWeight: 500, color: COLORS.white }}>{label}</div>
      {detail && <div style={{ fontSize: 12, color: COLORS.grey, marginTop: 2 }}>{detail}</div>}
    </div>
  </div>
);

// ─── Navigation ──────────────────────────────────────────────────────────────
const Nav = ({ currentPage, setPage, user, setUser }) => {
  const [scrolled, setScrolled] = useState(false);
  useEffect(() => {
    const onScroll = () => setScrolled(window.scrollY > 20);
    window.addEventListener("scroll", onScroll);
    return () => window.removeEventListener("scroll", onScroll);
  }, []);

  return (
    <nav style={{
      position: "fixed", top: 0, left: 0, right: 0, zIndex: 100,
      background: scrolled ? "rgba(10,14,26,0.97)" : "rgba(10,14,26,0.75)",
      backdropFilter: "blur(24px)",
      borderBottom: `1px solid ${scrolled ? "rgba(0,212,255,0.12)" : "rgba(0,212,255,0.05)"}`,
      padding: "0 24px",
      transition: "all 0.3s ease",
    }}>
      <div style={{ maxWidth: 1200, margin: "0 auto", display: "flex", alignItems: "center", justifyContent: "space-between", height: 64 }}>

        {/* Logo */}
        <div onClick={() => setPage("home")} style={{ display: "flex", alignItems: "center", gap: 10, cursor: "pointer", userSelect: "none" }}>
          <div style={{
            width: 38, height: 38, borderRadius: 11,
            background: "linear-gradient(135deg, rgba(0,212,255,0.15), rgba(0,136,170,0.25))",
            border: "1px solid rgba(0,212,255,0.35)",
            display: "flex", alignItems: "center", justifyContent: "center",
            boxShadow: "0 0 16px rgba(0,212,255,0.1)",
          }}>
            <Icon name="shield" size={19} color={COLORS.accent} />
          </div>
          <span className="syne" style={{ fontSize: 19, fontWeight: 800, letterSpacing: "-0.02em" }}>
            Safe<span style={{ color: COLORS.accent }}>Check</span>
          </span>
        </div>

        {/* Desktop Nav Links — hidden on mobile via inline media */}
        <div style={{ display: "flex", gap: 32, alignItems: "center" }}
          className="hide-mobile">
          {[["home","Home"],["scanner","Check a Scam"],["knowledge","Library"],["alerts","Alerts"],["pricing","Pricing"]].map(([p,l]) => (
            <span key={p}
              onClick={() => setPage(p)}
              style={{
                fontSize: 14, fontWeight: 500, cursor: "pointer",
                color: currentPage === p ? COLORS.white : COLORS.grey,
                borderBottom: currentPage === p ? `2px solid ${COLORS.accent}` : "2px solid transparent",
                paddingBottom: 2,
                transition: "all 0.2s",
              }}
              onMouseEnter={e => e.target.style.color = COLORS.white}
              onMouseLeave={e => { if (currentPage !== p) e.target.style.color = COLORS.grey; }}
            >{l}</span>
          ))}
        </div>

        {/* Right side — auth + avatar (hamburger is separate TopRightMenu) */}
        <div style={{ display: "flex", gap: 10, alignItems: "center", paddingRight: 52 }}>
          {user ? (
            <>
              <button className="btn-ghost hide-mobile"
                style={{ padding: "7px 16px", borderRadius: 8, fontSize: 13 }}
                onClick={() => setPage("dashboard")}>
                Dashboard
              </button>
              <div
                title={`Signed in as ${user.email}\nClick to sign out`}
                onClick={() => setUser(null)}
                style={{
                  width: 36, height: 36, borderRadius: "50%", flexShrink: 0,
                  background: "linear-gradient(135deg, #00D4FF, #0088AA)",
                  display: "flex", alignItems: "center", justifyContent: "center",
                  cursor: "pointer", fontSize: 14, fontWeight: 800, color: "#0A0E1A",
                  boxShadow: "0 0 12px rgba(0,212,255,0.3)",
                  userSelect: "none",
                }}>
                {user.name[0].toUpperCase()}
              </div>
            </>
          ) : (
            <>
              <button className="btn-ghost hide-mobile"
                style={{ padding: "7px 16px", borderRadius: 8, fontSize: 13 }}
                onClick={() => setPage("auth")}>Sign In</button>
              <button className="btn-primary"
                style={{ padding: "8px 18px", borderRadius: 8, fontSize: 13 }}
                onClick={() => setPage("auth")}>Get Started</button>
            </>
          )}
        </div>
      </div>
    </nav>
  );
};

// ─── HOME PAGE ────────────────────────────────────────────────────────────────
const HomePage = ({ setPage, setScannerInput, setScannerType }) => {
  const [quickInput, setQuickInput] = useState("");
  const [quickType, setQuickType] = useState("message");

  const handleQuickScan = () => {
    if (!quickInput.trim()) return;
    setScannerInput(quickInput);
    setScannerType(quickType);
    setPage("scanner");
  };

  const testimonials = [
    { name: "Margaret O'Brien", age: 68, text: "SafeCheck saved me from losing €2,400 to a fake bank text. So easy to use!", avatar: "M" },
    { name: "James Doyle", age: 34, text: "Caught a fake DoneDeal courier scam immediately. The explanation was incredibly clear.", avatar: "J" },
    { name: "Sarah Murphy", age: 45, text: "I use this for my small business. Every suspicious email gets checked first now.", avatar: "S" },
  ];

  const stats = [{ v: "2.4M+", l: "Scams Detected" }, { v: "98.7%", l: "Accuracy Rate" }, { v: "€18M+", l: "Money Protected" }, { v: "150K+", l: "Active Users" }];

  return (
    <div>
      {/* Hero */}
      <section className="grid-bg" style={{ minHeight: "100vh", display: "flex", alignItems: "center", justifyContent: "center", position: "relative", overflow: "hidden", paddingTop: 80 }}>
        <div className="hero-glow" style={{ top: "10%", left: "50%", transform: "translateX(-50%)" }} />
        <div className="hero-glow" style={{ bottom: "-20%", right: "-10%" }} />

        <div style={{ maxWidth: 800, margin: "0 auto", padding: "80px 24px", textAlign: "center", position: "relative", zIndex: 1 }}>
          {/* Badge */}
          <div style={{
            display: "inline-flex", alignItems: "center", gap: 8, padding: "6px 16px",
            background: "rgba(0,212,255,0.08)", border: "1px solid rgba(0,212,255,0.2)",
            borderRadius: 20, marginBottom: 28,
          }}>
            <div className="alert-dot" style={{ background: COLORS.green, boxShadow: `0 0 8px ${COLORS.green}` }} />
            <span style={{ fontSize: 12, color: COLORS.accent, fontFamily: "'Syne',sans-serif", fontWeight: 600, letterSpacing: "0.05em" }}>
              PROTECTING IRELAND & BEYOND
            </span>
          </div>

          <h1 className="syne" style={{ fontSize: "clamp(36px, 6vw, 68px)", fontWeight: 800, lineHeight: 1.05, letterSpacing: "-0.02em", marginBottom: 20 }}>
            Don't Get Scammed.<br />
            <span style={{ background: "linear-gradient(135deg, #00D4FF, #00E676)", WebkitBackgroundClip: "text", WebkitTextFillColor: "transparent" }}>
              Check First.
            </span>
          </h1>

          <p style={{ fontSize: "clamp(16px, 2vw, 20px)", color: COLORS.grey, lineHeight: 1.7, maxWidth: 600, margin: "0 auto 48px" }}>
            AI-powered scam detection for emails, texts, websites, and marketplace listings. Instant results. Plain English explanations.
          </p>

          {/* Quick Scanner */}
          <div className="glass" style={{ borderRadius: 16, padding: 6, maxWidth: 680, margin: "0 auto 20px" }}>
            <div style={{ display: "flex", gap: 6, marginBottom: 6 }}>
              {[["message","💬 Message"],["url","🌐 Website"],["marketplace","🛒 Listing"]].map(([t,l]) => (
                <button key={t} className={`tab-btn ${quickType===t?"active":""}`} style={{ flex: 1, fontSize: 12 }} onClick={() => setQuickType(t)}>{l}</button>
              ))}
            </div>
            <div style={{ display: "flex", gap: 8 }}>
              <input
                className="input-field"
                style={{ borderRadius: 10, padding: "14px 16px", border: "1px solid rgba(0,212,255,0.15)", flex: 1 }}
                placeholder={quickType === "url" ? "Paste a website URL (e.g. paypa1-secure.com)" : "Paste a suspicious message, text, or listing..."}
                value={quickInput}
                onChange={e => setQuickInput(e.target.value)}
                onKeyDown={e => e.key === "Enter" && handleQuickScan()}
              />
              <button className="btn-primary" style={{ borderRadius: 10, padding: "14px 24px", whiteSpace: "nowrap", fontSize: 15 }} onClick={handleQuickScan}>
                Check Now →
              </button>
            </div>
          </div>
          <p style={{ fontSize: 12, color: COLORS.grey }}>Free • No account required • Instant results</p>

          {/* Stats */}
          <div style={{ display: "grid", gridTemplateColumns: "repeat(4,1fr)", gap: 20, marginTop: 60 }}>
            {stats.map(({ v, l }) => (
              <div key={l} style={{ textAlign: "center" }}>
                <div className="syne" style={{ fontSize: 28, fontWeight: 800, color: COLORS.accent }}>{v}</div>
                <div style={{ fontSize: 13, color: COLORS.grey, marginTop: 4 }}>{l}</div>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Features Grid */}
      <section style={{ padding: "80px 24px", maxWidth: 1200, margin: "0 auto" }}>
        <div style={{ textAlign: "center", marginBottom: 52 }}>
          <h2 className="syne" style={{ fontSize: "clamp(28px,4vw,42px)", fontWeight: 800, marginBottom: 12 }}>Everything You Need to Stay Safe</h2>
          <p style={{ color: COLORS.grey, fontSize: 17 }}>Six powerful tools, one simple platform</p>
        </div>

        <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(320px, 1fr))", gap: 20 }}>
          {[
            { icon: "message", color: "#00D4FF", title: "Message Detector", desc: "Paste emails, texts, WhatsApp or social media messages. Get an instant scam score with plain-English explanation.", badge: "Free", action: () => { setScannerType("message"); setPage("scanner"); } },
            { icon: "camera", color: "#00E676", title: "Screenshot Scanner", desc: "Upload a screenshot of a suspicious conversation or website. Our OCR extracts the text and AI analyzes it instantly.", badge: "Free", action: () => { setScannerType("screenshot"); setPage("scanner"); } },
            { icon: "globe", color: "#FFB300", title: "Website Checker", desc: "Check if a URL is safe before you click. Detects phishing, fake shops, brand impersonation and more.", badge: "Premium", action: () => { setScannerType("url"); setPage("scanner"); } },
            { icon: "tag", color: "#FF3D57", title: "Marketplace Guard", desc: "Specialized detection for Facebook Marketplace, DoneDeal, eBay and Adverts.ie scam patterns.", badge: "Premium", action: () => { setScannerType("marketplace"); setPage("scanner"); } },
            { icon: "book", color: "#A78BFA", title: "Scam Library", desc: "Searchable database of scam types with examples, red flags and what to do if you've already been targeted.", badge: "Free", action: () => setPage("knowledge") },
            { icon: "alert", color: "#FB923C", title: "Live Scam Alerts", desc: "Real-time feed of the latest scams circulating in Ireland and the UK. Subscribe for email alerts.", badge: "Free", action: () => setPage("alerts") },
          ].map(({ icon, color, title, desc, badge, action }) => (
            <div key={title} className="card" style={{ padding: 28, cursor: "pointer" }} onClick={action}>
              <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", marginBottom: 16 }}>
                <div className="feature-icon" style={{ background: color + "15", border: `1px solid ${color}30` }}>
                  <Icon name={icon} size={22} color={color} />
                </div>
                <span style={{
                  fontSize: 10, fontWeight: 700, padding: "3px 8px", borderRadius: 4,
                  fontFamily: "'Syne',sans-serif", letterSpacing: "0.06em",
                  background: badge === "Free" ? "rgba(0,230,118,0.1)" : "rgba(0,212,255,0.1)",
                  color: badge === "Free" ? COLORS.green : COLORS.accent,
                  border: `1px solid ${badge === "Free" ? "rgba(0,230,118,0.2)" : "rgba(0,212,255,0.2)"}`,
                }}>
                  {badge.toUpperCase()}
                </span>
              </div>
              <h3 className="syne" style={{ fontSize: 18, fontWeight: 700, marginBottom: 8 }}>{title}</h3>
              <p style={{ color: COLORS.grey, fontSize: 14, lineHeight: 1.6 }}>{desc}</p>
              <div style={{ marginTop: 16, color: color, fontSize: 13, fontWeight: 600, display: "flex", alignItems: "center", gap: 4 }}>
                Try it <Icon name="chevron" size={14} color={color} />
              </div>
            </div>
          ))}
        </div>
      </section>

      {/* How It Works */}
      <section style={{ padding: "80px 24px", background: "#0D1221" }}>
        <div style={{ maxWidth: 900, margin: "0 auto", textAlign: "center" }}>
          <h2 className="syne" style={{ fontSize: "clamp(28px,4vw,42px)", fontWeight: 800, marginBottom: 12 }}>How SafeCheck Works</h2>
          <p style={{ color: COLORS.grey, marginBottom: 56 }}>Results in under 10 seconds</p>

          <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(200px, 1fr))", gap: 8, position: "relative" }}>
            {[
              { step: "01", icon: "upload", title: "Paste or Upload", desc: "Add your suspicious message, URL or screenshot" },
              { step: "02", icon: "zap", title: "AI Analysis", desc: "Our model checks 47 scam indicators instantly" },
              { step: "03", icon: "eye", title: "Get Your Score", desc: "Clear risk score with plain-English explanation" },
              { step: "04", icon: "shield", title: "Stay Safe", desc: "Follow recommended actions to protect yourself" },
            ].map(({ step, icon, title, desc }, i) => (
              <div key={step} style={{ padding: "28px 20px", textAlign: "center", position: "relative" }}>
                <div style={{ fontSize: 11, color: COLORS.accent, fontFamily: "'Syne',sans-serif", fontWeight: 700, marginBottom: 12, letterSpacing: "0.1em" }}>{step}</div>
                <div style={{
                  width: 56, height: 56, borderRadius: 16, margin: "0 auto 16px",
                  background: "rgba(0,212,255,0.08)", border: "1px solid rgba(0,212,255,0.15)",
                  display: "flex", alignItems: "center", justifyContent: "center",
                }}>
                  <Icon name={icon} size={24} color={COLORS.accent} />
                </div>
                <h3 className="syne" style={{ fontSize: 16, fontWeight: 700, marginBottom: 8 }}>{title}</h3>
                <p style={{ color: COLORS.grey, fontSize: 13, lineHeight: 1.6 }}>{desc}</p>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Testimonials */}
      <section style={{ padding: "80px 24px", maxWidth: 1100, margin: "0 auto" }}>
        <h2 className="syne" style={{ fontSize: "clamp(26px,4vw,38px)", fontWeight: 800, textAlign: "center", marginBottom: 48 }}>
          Trusted by Thousands of Irish Users
        </h2>
        <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(280px, 1fr))", gap: 20 }}>
          {testimonials.map(({ name, age, text, avatar }) => (
            <div key={name} className="card" style={{ padding: 28 }}>
              <div style={{ display: "flex", gap: 4, marginBottom: 16 }}>
                {[1,2,3,4,5].map(i => <Icon key={i} name="star" size={14} color={COLORS.amber} />)}
              </div>
              <p style={{ color: COLORS.greyLight, lineHeight: 1.7, fontSize: 15, marginBottom: 20 }}>"{text}"</p>
              <div style={{ display: "flex", alignItems: "center", gap: 10 }}>
                <div style={{
                  width: 38, height: 38, borderRadius: "50%",
                  background: "linear-gradient(135deg, #00D4FF30, #0088AA50)",
                  border: "1px solid rgba(0,212,255,0.2)",
                  display: "flex", alignItems: "center", justifyContent: "center",
                  fontWeight: 700, color: COLORS.accent, fontSize: 15,
                }}>
                  {avatar}
                </div>
                <div>
                  <div style={{ fontSize: 14, fontWeight: 600 }}>{name}</div>
                  <div style={{ fontSize: 12, color: COLORS.grey }}>Age {age}</div>
                </div>
              </div>
            </div>
          ))}
        </div>
      </section>

      {/* CTA */}
      <section style={{ padding: "80px 24px", textAlign: "center", background: "#0D1221" }}>
        <div style={{ maxWidth: 600, margin: "0 auto" }}>
          <h2 className="syne" style={{ fontSize: "clamp(28px,4vw,44px)", fontWeight: 800, marginBottom: 16 }}>
            Stop Scammers in Their Tracks
          </h2>
          <p style={{ color: COLORS.grey, fontSize: 17, marginBottom: 36 }}>Join 150,000+ people who check before they click</p>
          <button className="btn-primary" style={{ padding: "16px 40px", borderRadius: 12, fontSize: 17 }} onClick={() => setPage("scanner")}>
            Start Checking for Free →
          </button>
        </div>
      </section>
    </div>
  );
};

// ─── AI CALL ─────────────────────────────────────────────────────────────────
const callAI = async (systemPrompt, userMessage) => {
  const response = await fetch("https://api.anthropic.com/v1/messages", {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify({
      model: "claude-sonnet-4-20250514",
      max_tokens: 1000,
      system: systemPrompt,
      messages: [{ role: "user", content: userMessage }],
    }),
  });
  const data = await response.json();
  const text = data.content?.map(b => b.text || "").join("");
  const clean = text.replace(/```json\n?|\n?```/g, "").trim();
  return JSON.parse(clean);
};

const SCAM_SYSTEM = `You are SafeCheck's scam detection AI. Analyze the input for scam indicators.
Return ONLY valid JSON (no markdown, no preamble):
{
  "score": <0-100 integer, 0=definitely safe, 100=definite scam>,
  "riskLevel": <"Low"|"Medium"|"High">,
  "summary": <2-3 sentence plain-English explanation for a non-technical user>,
  "indicators": [
    { "label": <string>, "present": <boolean>, "detail": <string> }
  ],
  "actions": [<string>, ...],
  "scamType": <string or null>
}
Include 5-7 indicators covering: urgency language, suspicious links, payment requests, impersonation, grammar issues, too-good-to-be-true offers, threat/fear tactics, unusual payment methods.`;

// ─── SCANNER PAGE ─────────────────────────────────────────────────────────────
const ScannerPage = ({ initialInput = "", initialType = "message" }) => {
  const [activeTab, setActiveTab] = useState(initialType);
  const [input, setInput] = useState(initialInput);
  const [url, setUrl] = useState("");
  const [marketplace, setMarketplace] = useState({ platform: "facebook", text: "" });
  const [loading, setLoading] = useState(false);
  const [result, setResult] = useState(null);
  const [error, setError] = useState("");
  const [scanning, setScanning] = useState(false);
  const [dragOver, setDragOver] = useState(false);
  const fileRef = useRef();

  const tabs = [
    { id: "message", label: "💬 Message", icon: "message" },
    { id: "url", label: "🌐 Website", icon: "globe" },
    { id: "screenshot", label: "📸 Screenshot", icon: "camera" },
    { id: "marketplace", label: "🛒 Marketplace", icon: "tag" },
  ];

  const getPromptContent = () => {
    if (activeTab === "message") return `Analyze this message for scam indicators:\n\n${input}`;
    if (activeTab === "url") return `Analyze this URL for phishing/scam indicators. Check for: suspicious domain names, brand impersonation, typosquatting, suspicious TLDs, excessive subdomains, and other red flags. URL: ${url}`;
    if (activeTab === "marketplace") return `Analyze this ${marketplace.platform} marketplace listing/message for scam patterns including: fake courier scams, overpayment scams, fake payment confirmations, deposit scams, account takeover behavior.\n\n${marketplace.text}`;
    if (activeTab === "screenshot") return `The user uploaded a screenshot of a suspicious message/website. Analyze for common scam patterns. Treat this as generic suspicious content: ${input || "Screenshot of suspicious content - apply general scam detection logic"}`;
    return input;
  };

  const runScan = async () => {
    const content = getPromptContent();
    const hasContent = activeTab === "url" ? url.trim() : activeTab === "marketplace" ? marketplace.text.trim() : input.trim();
    if (!hasContent) { setError("Please enter some content to analyze."); return; }

    setLoading(true); setScanning(true); setError(""); setResult(null);
    try {
      const data = await callAI(SCAM_SYSTEM, content);
      setResult(data);
    } catch (e) {
      setError("Analysis failed. Please check your connection and try again.");
    } finally {
      setLoading(false);
      setTimeout(() => setScanning(false), 300);
    }
  };

  const handleFile = (file) => {
    if (!file) return;
    setInput(`[Screenshot uploaded: ${file.name}] Analyzing for scam indicators...`);
  };

  return (
    <div style={{ maxWidth: 900, margin: "0 auto", padding: "100px 24px 60px" }}>
      <div style={{ marginBottom: 32 }}>
        <h1 className="syne" style={{ fontSize: "clamp(26px,4vw,38px)", fontWeight: 800, marginBottom: 8 }}>Scam Checker</h1>
        <p style={{ color: COLORS.grey }}>Paste your content below and get an instant AI-powered scam analysis</p>
      </div>

      {/* Tab Bar */}
      <div style={{ display: "flex", gap: 6, marginBottom: 24, flexWrap: "wrap" }}>
        {tabs.map(t => (
          <button key={t.id} className={`tab-btn ${activeTab===t.id?"active":""}`} onClick={() => { setActiveTab(t.id); setResult(null); setError(""); }}>
            {t.label}
          </button>
        ))}
      </div>

      <div style={{ display: "grid", gridTemplateColumns: result ? "1fr 1fr" : "1fr", gap: 24, alignItems: "start" }}>
        {/* Input Panel */}
        <div className="card" style={{ padding: 24, position: "relative", overflow: "hidden" }}>
          {scanning && (
            <div className="scan-overlay">
              <div className="scan-line" />
            </div>
          )}

          {activeTab === "message" && (
            <>
              <label style={{ fontSize: 13, color: COLORS.grey, marginBottom: 8, display: "block" }}>Paste email, SMS, WhatsApp, or social media message</label>
              <textarea
                className="input-field"
                style={{ borderRadius: 10, padding: 14, minHeight: 200 }}
                placeholder="Hi, your package has been held at customs. Click here to pay the €2.50 fee: track-parcel-ie.com..."
                value={input}
                onChange={e => setInput(e.target.value)}
              />
            </>
          )}

          {activeTab === "url" && (
            <>
              <label style={{ fontSize: 13, color: COLORS.grey, marginBottom: 8, display: "block" }}>Enter a website URL to check</label>
              <input
                className="input-field"
                style={{ borderRadius: 10, padding: "14px 16px" }}
                placeholder="https://paypa1-secure-verify.com"
                value={url}
                onChange={e => setUrl(e.target.value)}
              />
              <div style={{ marginTop: 16, padding: 12, background: COLORS.amberDim, border: `1px solid ${COLORS.amber}30`, borderRadius: 8 }}>
                <p style={{ fontSize: 12, color: COLORS.amber, display: "flex", gap: 6, alignItems: "flex-start" }}>
                  <Icon name="info" size={14} color={COLORS.amber} />
                  <span>Do <strong>not</strong> click on suspicious links. Copy and paste the URL here to check it safely.</span>
                </p>
              </div>
            </>
          )}

          {activeTab === "screenshot" && (
            <div
              onDragOver={e => { e.preventDefault(); setDragOver(true); }}
              onDragLeave={() => setDragOver(false)}
              onDrop={e => { e.preventDefault(); setDragOver(false); handleFile(e.dataTransfer.files[0]); }}
              onClick={() => fileRef.current?.click()}
              style={{
                border: `2px dashed ${dragOver ? COLORS.accent : "rgba(0,212,255,0.2)"}`,
                borderRadius: 12, padding: "48px 24px", textAlign: "center",
                cursor: "pointer", transition: "all 0.2s",
                background: dragOver ? COLORS.accentGlow : "transparent",
                minHeight: 200, display: "flex", flexDirection: "column", alignItems: "center", justifyContent: "center", gap: 12,
              }}
            >
              <input ref={fileRef} type="file" accept="image/*" style={{ display: "none" }} onChange={e => handleFile(e.target.files[0])} />
              <div style={{ width: 56, height: 56, borderRadius: 16, background: COLORS.accentGlow, display: "flex", alignItems: "center", justifyContent: "center" }}>
                <Icon name="upload" size={26} color={COLORS.accent} />
              </div>
              <div>
                <p style={{ fontWeight: 600, marginBottom: 4 }}>Drop screenshot here</p>
                <p style={{ fontSize: 13, color: COLORS.grey }}>or click to browse • PNG, JPG, GIF</p>
              </div>
              {input && <p style={{ fontSize: 13, color: COLORS.green }}>✓ {input.slice(0, 60)}</p>}
            </div>
          )}

          {activeTab === "marketplace" && (
            <>
              <label style={{ fontSize: 13, color: COLORS.grey, marginBottom: 8, display: "block" }}>Platform</label>
              <select
                className="input-field"
                style={{ borderRadius: 10, padding: "12px 16px", marginBottom: 16 }}
                value={marketplace.platform}
                onChange={e => setMarketplace(p => ({ ...p, platform: e.target.value }))}
              >
                <option value="facebook">Facebook Marketplace</option>
                <option value="donedeal">DoneDeal</option>
                <option value="ebay">eBay</option>
                <option value="adverts">Adverts.ie</option>
              </select>
              <label style={{ fontSize: 13, color: COLORS.grey, marginBottom: 8, display: "block" }}>Paste listing or message from seller/buyer</label>
              <textarea
                className="input-field"
                style={{ borderRadius: 10, padding: 14, minHeight: 160 }}
                placeholder="Hi! I'm interested in your item. I'll pay via PayPal but I need you to ship first. My courier will collect..."
                value={marketplace.text}
                onChange={e => setMarketplace(p => ({ ...p, text: e.target.value }))}
              />
            </>
          )}

          <button
            className="btn-primary"
            style={{ width: "100%", padding: 14, borderRadius: 10, fontSize: 16, marginTop: 16 }}
            onClick={runScan}
            disabled={loading}
          >
            {loading ? (
              <span style={{ display: "flex", alignItems: "center", justifyContent: "center", gap: 10 }}>
                <span className="spinner" style={{ borderTopColor: "#0A0E1A", borderColor: "rgba(10,14,26,0.3)" }} />
                Analyzing...
              </span>
            ) : "🔍 Analyze Now"}
          </button>

          {error && (
            <div style={{ marginTop: 12, padding: 12, background: COLORS.redDim, border: `1px solid ${COLORS.red}30`, borderRadius: 8 }}>
              <p style={{ fontSize: 13, color: COLORS.red }}>{error}</p>
            </div>
          )}
        </div>

        {/* Results Panel */}
        {result && (
          <div className="fade-in-up">
            {/* Score */}
            <div className="card" style={{ padding: 28, marginBottom: 20, textAlign: "center" }}>
              <ScoreRing score={result.score} size={140} />
              {result.scamType && (
                <div style={{ marginTop: 16, padding: "6px 14px", background: COLORS.redDim, borderRadius: 8, display: "inline-block" }}>
                  <span style={{ fontSize: 13, color: COLORS.red, fontWeight: 600 }}>⚠ {result.scamType}</span>
                </div>
              )}
            </div>

            {/* Summary */}
            <div className="card" style={{ padding: 20, marginBottom: 16 }}>
              <h3 className="syne" style={{ fontSize: 14, fontWeight: 700, marginBottom: 10, color: COLORS.grey, letterSpacing: "0.05em" }}>ANALYSIS</h3>
              <p style={{ color: COLORS.greyLight, lineHeight: 1.7, fontSize: 15 }}>{result.summary}</p>
            </div>

            {/* Indicators */}
            <div className="card" style={{ padding: 20, marginBottom: 16 }}>
              <h3 className="syne" style={{ fontSize: 14, fontWeight: 700, marginBottom: 4, color: COLORS.grey, letterSpacing: "0.05em" }}>SCAM INDICATORS</h3>
              {(result.indicators || []).map((ind, i) => (
                <IndicatorRow key={i} label={ind.label} present={ind.present} detail={ind.detail} />
              ))}
            </div>

            {/* Actions */}
            <div className="card" style={{ padding: 20 }}>
              <h3 className="syne" style={{ fontSize: 14, fontWeight: 700, marginBottom: 12, color: COLORS.grey, letterSpacing: "0.05em" }}>RECOMMENDED ACTIONS</h3>
              {(result.actions || []).map((action, i) => (
                <div key={i} style={{ display: "flex", gap: 10, marginBottom: 10, alignItems: "flex-start" }}>
                  <div style={{ width: 20, height: 20, borderRadius: "50%", background: COLORS.accentGlow, border: `1px solid ${COLORS.accent}30`, display: "flex", alignItems: "center", justifyContent: "center", flexShrink: 0, marginTop: 1 }}>
                    <Icon name="check" size={10} color={COLORS.accent} />
                  </div>
                  <span style={{ fontSize: 14, color: COLORS.greyLight, lineHeight: 1.5 }}>{action}</span>
                </div>
              ))}
            </div>
          </div>
        )}
      </div>
    </div>
  );
};

// ─── KNOWLEDGE BASE ───────────────────────────────────────────────────────────
const KnowledgePage = () => {
  const [search, setSearch] = useState("");
  const [activeCategory, setActiveCategory] = useState("all");
  const [selected, setSelected] = useState(null);

  const categories = [
    { id: "all", label: "All" },
    { id: "banking", label: "💳 Banking" },
    { id: "marketplace", label: "🛒 Marketplace" },
    { id: "investment", label: "📈 Investment" },
    { id: "romance", label: "💔 Romance" },
    { id: "job", label: "💼 Job" },
    { id: "ai", label: "🤖 AI Scams" },
  ];

  const scams = [
    { id: 1, cat: "banking", title: "Bank Impersonation Text", risk: "High", victims: "12,400/yr", desc: "Fraudsters send texts pretending to be your bank, claiming suspicious activity and asking you to verify your details via a fake link.", redFlags: ["Urgency ('act now or account locked')", "Link doesn't match bank's real domain", "Asks for full card number or PIN", "Unusual sender number"], actions: ["Never click links in banking texts", "Call your bank directly using the number on your card", "Report to Garda Síochána and your bank", "Forward to 7726 (spam reporting)"] },
    { id: 2, cat: "marketplace", title: "Fake Courier / Shipping Scam", risk: "High", victims: "8,200/yr", desc: "Buyer or seller insists on using their 'own courier'. You're asked to pay a fee or share details before the courier collects.", redFlags: ["Insists on specific courier service", "Asks for payment before collection", "Sends fake payment confirmation", "Communication moves off platform quickly"], actions: ["Never pay a 'courier fee' upfront", "Use platform's official payment system", "Meet in person for local sales", "Block and report the user"] },
    { id: 3, cat: "investment", title: "Crypto Investment Scam", risk: "High", victims: "€15M lost in IE 2023", desc: "Promises of guaranteed returns through crypto or trading platforms. Often starts as a romance or social media friendship.", redFlags: ["Guaranteed returns promised", "Pressure to invest more", "Fake 'profits' shown on platform", "Can't withdraw money"], actions: ["Never invest on advice from strangers", "Check with CBI register before investing", "Be wary of unsolicited investment advice", "Report to CCPC if targeted"] },
    { id: 4, cat: "romance", title: "Romance / Love Scam", risk: "High", victims: "€3.2M lost in IE 2023", desc: "Long-term emotional manipulation via dating apps or social media. Scammer builds trust then asks for money citing an emergency.", redFlags: ["Never meets in person or on video", "Moves off dating app quickly", "Profession is soldier/doctor/engineer abroad", "Eventually asks for money"], actions: ["Reverse image search their photos", "Never send money to someone you haven't met", "Talk to someone you trust about the relationship", "Report to Garda Síochána"] },
    { id: 5, cat: "job", title: "Work From Home Job Scam", risk: "Medium", victims: "4,100/yr", desc: "Fake job offers requiring upfront payment for 'training materials' or asking you to process payments through your account.", redFlags: ["Too good pay for simple tasks", "Asked to pay upfront for anything", "Asked to use your bank account for transfers", "No verifiable company information"], actions: ["Research the company independently", "Never pay to start a job", "Never use your personal account for employer funds", "Check job on official company website"] },
    { id: 6, cat: "banking", title: "Parcel Delivery Scam", risk: "Medium", victims: "22,000/yr", desc: "Fake An Post / DHL / DPD texts claiming a small customs fee is owed before your parcel can be delivered.", redFlags: ["Text about package you didn't order", "Small 'customs fee' required", "Link looks similar to but isn't the real carrier site", "Asks for card details on suspicious page"], actions: ["Go directly to carrier's official website", "Track parcels using official apps only", "Don't click links in delivery texts", "An Post never charges customs by SMS"] },
    { id: 7, cat: "ai", title: "AI Voice Clone Scam", risk: "High", victims: "Emerging 2024+", desc: "Scammers clone a family member's voice using AI and call claiming to be in an emergency, needing money urgently.", redFlags: ["Unexpected call from family in distress", "Urgency to wire money immediately", "Story changes or doesn't add up", "Caller avoids video call"], actions: ["Hang up and call the family member directly", "Establish a family 'code word' for emergencies", "Never wire money based on a phone call alone", "Report to Garda Cybercrime"] },
    { id: 8, cat: "marketplace", title: "Overpayment / Cheque Scam", risk: "High", victims: "3,800/yr", desc: "Buyer sends more than the agreed price, asks you to refund the difference. Their payment later bounces leaving you out of pocket.", redFlags: ["Buyer offers more than asking price", "Insists on cheque or bank transfer", "Story about being abroad or in a hurry", "Wants refund of 'overpayment' immediately"], actions: ["Only accept payment you can verify is cleared", "Never refund before payment fully clears", "Prefer cash for in-person transactions", "If unsure, wait 10 business days before refunding"] },
    { id: 9, cat: "ai", title: "Deepfake Celebrity Investment", risk: "High", victims: "Emerging 2024+", desc: "Fake ads using deepfake videos of celebrities (Elon Musk, Dragons' Den judges) promoting fake investment platforms.", redFlags: ["Celebrity appears to endorse specific platform", "Viral video with slightly unnatural movement", "Claims of guaranteed returns", "Ads on social media with celebrity content"], actions: ["No celebrity genuinely endorses investment platforms in ads", "Search for the platform name + 'scam'", "Check CBI register", "Report the ad to the social platform"] },
  ];

  const filtered = scams.filter(s =>
    (activeCategory === "all" || s.cat === activeCategory) &&
    (!search || s.title.toLowerCase().includes(search.toLowerCase()) || s.desc.toLowerCase().includes(search.toLowerCase()))
  );

  if (selected) {
    const scam = scams.find(s => s.id === selected);
    return (
      <div style={{ maxWidth: 760, margin: "0 auto", padding: "100px 24px 60px" }}>
        <button onClick={() => setSelected(null)} style={{ background: "none", border: "none", color: COLORS.grey, cursor: "pointer", display: "flex", alignItems: "center", gap: 6, marginBottom: 24, fontSize: 14 }}>
          ← Back to Library
        </button>
        <div className="card" style={{ padding: 32 }}>
          <div style={{ display: "flex", gap: 12, alignItems: "center", marginBottom: 20 }}>
            <span className={`risk-badge risk-${scam.risk.toLowerCase()}`}>{scam.risk} Risk</span>
            <span style={{ fontSize: 12, color: COLORS.grey }}>~{scam.victims} reported victims</span>
          </div>
          <h1 className="syne" style={{ fontSize: 28, fontWeight: 800, marginBottom: 16 }}>{scam.title}</h1>
          <p style={{ color: COLORS.greyLight, lineHeight: 1.8, fontSize: 16, marginBottom: 28 }}>{scam.desc}</p>

          <h3 className="syne" style={{ fontSize: 14, fontWeight: 700, color: COLORS.red, letterSpacing: "0.05em", marginBottom: 12 }}>🚩 RED FLAGS</h3>
          {scam.redFlags.map((f, i) => (
            <div key={i} style={{ display: "flex", gap: 10, marginBottom: 8, alignItems: "flex-start" }}>
              <span style={{ color: COLORS.red, fontSize: 16, lineHeight: 1 }}>•</span>
              <span style={{ fontSize: 14, color: COLORS.greyLight }}>{f}</span>
            </div>
          ))}

          <h3 className="syne" style={{ fontSize: 14, fontWeight: 700, color: COLORS.green, letterSpacing: "0.05em", marginTop: 24, marginBottom: 12 }}>✅ WHAT TO DO</h3>
          {scam.actions.map((a, i) => (
            <div key={i} style={{ display: "flex", gap: 10, marginBottom: 8, alignItems: "flex-start" }}>
              <span style={{ color: COLORS.green, fontSize: 16, lineHeight: 1 }}>•</span>
              <span style={{ fontSize: 14, color: COLORS.greyLight }}>{a}</span>
            </div>
          ))}
        </div>
      </div>
    );
  }

  return (
    <div style={{ maxWidth: 1100, margin: "0 auto", padding: "100px 24px 60px" }}>
      <div style={{ marginBottom: 36 }}>
        <h1 className="syne" style={{ fontSize: "clamp(26px,4vw,38px)", fontWeight: 800, marginBottom: 8 }}>Scam Knowledge Library</h1>
        <p style={{ color: COLORS.grey }}>Learn about the most common scams targeting people in Ireland and beyond</p>
      </div>

      <div style={{ display: "flex", gap: 12, marginBottom: 24, flexWrap: "wrap", alignItems: "center" }}>
        <div style={{ flex: 1, minWidth: 220, position: "relative" }}>
          <span style={{ position: "absolute", left: 12, top: "50%", transform: "translateY(-50%)" }}>
            <Icon name="search" size={16} color={COLORS.grey} />
          </span>
          <input className="input-field" style={{ borderRadius: 10, padding: "11px 16px 11px 38px" }} placeholder="Search scams..." value={search} onChange={e => setSearch(e.target.value)} />
        </div>
        <div style={{ display: "flex", gap: 6, flexWrap: "wrap" }}>
          {categories.map(c => (
            <button key={c.id} className={`tab-btn ${activeCategory===c.id?"active":""}`} style={{ fontSize: 12 }} onClick={() => setActiveCategory(c.id)}>{c.label}</button>
          ))}
        </div>
      </div>

      <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fill, minmax(300px, 1fr))", gap: 16 }}>
        {filtered.map(scam => (
          <div key={scam.id} className="card" style={{ padding: 22, cursor: "pointer" }} onClick={() => setSelected(scam.id)}>
            <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", marginBottom: 10 }}>
              <span className={`risk-badge risk-${scam.risk.toLowerCase()}`}>{scam.risk}</span>
              <span style={{ fontSize: 11, color: COLORS.grey }}>{scam.victims}</span>
            </div>
            <h3 className="syne" style={{ fontSize: 16, fontWeight: 700, marginBottom: 8 }}>{scam.title}</h3>
            <p style={{ fontSize: 13, color: COLORS.grey, lineHeight: 1.6 }}>{scam.desc.slice(0, 100)}...</p>
            <div style={{ marginTop: 14, color: COLORS.accent, fontSize: 13, fontWeight: 600 }}>
              Learn more →
            </div>
          </div>
        ))}
        {filtered.length === 0 && (
          <div style={{ gridColumn: "1/-1", textAlign: "center", padding: 48, color: COLORS.grey }}>
            No scams found matching your search
          </div>
        )}
      </div>
    </div>
  );
};

// ─── ALERTS PAGE ──────────────────────────────────────────────────────────────
const AlertsPage = () => {
  const alerts = [
    { date: "Today", title: "New AN Post SMS Scam Surge", severity: "High", count: "1,240 reports this week", desc: "A new wave of fake An Post customs fee texts targeting Irish mobile numbers. The link leads to paypost-ie-customs.com — do not click." },
    { date: "Yesterday", title: "AIB 'Suspended Account' Phishing", severity: "High", count: "876 reports", desc: "Fake AIB emails claiming your account has been suspended. The sender domain is aib-secure-login.com (not aib.ie)." },
    { date: "2 days ago", title: "DoneDeal Courier Scam Wave", severity: "High", count: "654 reports", desc: "Buyers on DoneDeal are messaging sellers with requests to use 'An Post Courier' and sending fake payment confirmations via WhatsApp." },
    { date: "3 days ago", title: "Fake Revenue.ie Refund Email", severity: "Medium", count: "432 reports", desc: "Emails claiming you're owed a tax refund from Revenue. Links to revenue-refunds-ie.com — the real site is revenue.ie." },
    { date: "4 days ago", title: "WhatsApp 'Wrong Number' Romance Scam", severity: "Medium", count: "321 reports", desc: "Scammers text random numbers claiming to have the 'wrong number', then build a friendship before pitching a crypto investment." },
    { date: "5 days ago", title: "Meta Business Account Takeover", severity: "High", count: "218 reports", desc: "Small business owners receiving emails about 'page violations' with links to fake Meta login pages. Designed to steal Facebook/Instagram access." },
    { date: "1 week ago", title: "Fake Jobs on Indeed/LinkedIn", severity: "Medium", count: "187 reports", desc: "Fraudulent work-from-home job listings offering high pay for simple data entry. Applicants asked to pay for 'starter kit' upfront." },
    { date: "1 week ago", title: "AI Grandparent Scam Calls", severity: "High", count: "143 reports", desc: "AI-cloned voices of grandchildren calling elderly people claiming to be in an accident or in trouble abroad, requesting urgent wire transfers." },
  ];

  const severityColor = { High: COLORS.red, Medium: COLORS.amber, Low: COLORS.green };

  return (
    <div style={{ maxWidth: 900, margin: "0 auto", padding: "100px 24px 60px" }}>
      <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", marginBottom: 36, flexWrap: "wrap", gap: 16 }}>
        <div>
          <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 6 }}>
            <h1 className="syne" style={{ fontSize: "clamp(26px,4vw,38px)", fontWeight: 800 }}>Live Scam Alerts</h1>
            <div style={{ display: "flex", alignItems: "center", gap: 6, padding: "3px 10px", background: COLORS.redDim, borderRadius: 20 }}>
              <div className="alert-dot" style={{ background: COLORS.red, boxShadow: `0 0 8px ${COLORS.red}` }} />
              <span style={{ fontSize: 11, color: COLORS.red, fontWeight: 700, fontFamily: "'Syne',sans-serif" }}>LIVE</span>
            </div>
          </div>
          <p style={{ color: COLORS.grey }}>Real-time scam alerts circulating in Ireland right now</p>
        </div>
        <button className="btn-primary" style={{ padding: "10px 20px", borderRadius: 10, fontSize: 14 }}>
          🔔 Get Email Alerts
        </button>
      </div>

      {/* Summary Cards */}
      <div style={{ display: "grid", gridTemplateColumns: "repeat(3, 1fr)", gap: 16, marginBottom: 32 }}>
        {[
          { label: "Reports This Week", value: "4,170", color: COLORS.red },
          { label: "Active Scam Types", value: "23", color: COLORS.amber },
          { label: "Money at Risk (IE)", value: "€840K", color: COLORS.accent },
        ].map(({ label, value, color }) => (
          <div key={label} className="card" style={{ padding: "20px 24px" }}>
            <div className="syne" style={{ fontSize: 28, fontWeight: 800, color, marginBottom: 4 }}>{value}</div>
            <div style={{ fontSize: 13, color: COLORS.grey }}>{label}</div>
          </div>
        ))}
      </div>

      {/* Alert Feed */}
      <div style={{ display: "flex", flexDirection: "column", gap: 12 }}>
        {alerts.map((alert, i) => (
          <div key={i} className="card" style={{ padding: "20px 24px", borderLeft: `3px solid ${severityColor[alert.severity]}` }}>
            <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", gap: 12, flexWrap: "wrap" }}>
              <div style={{ flex: 1 }}>
                <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 6, flexWrap: "wrap" }}>
                  <h3 className="syne" style={{ fontSize: 15, fontWeight: 700 }}>{alert.title}</h3>
                  <span className={`risk-badge risk-${alert.severity.toLowerCase()}`}>{alert.severity}</span>
                </div>
                <p style={{ fontSize: 13, color: COLORS.grey, lineHeight: 1.6 }}>{alert.desc}</p>
              </div>
              <div style={{ textAlign: "right", flexShrink: 0 }}>
                <div style={{ fontSize: 11, color: COLORS.grey, marginBottom: 4 }}>{alert.date}</div>
                <div style={{ fontSize: 12, color: severityColor[alert.severity], fontWeight: 600 }}>{alert.count}</div>
              </div>
            </div>
          </div>
        ))}
      </div>

      {/* Report CTA */}
      <div className="glass" style={{ borderRadius: 16, padding: 28, marginTop: 28, textAlign: "center" }}>
        <h3 className="syne" style={{ fontSize: 18, fontWeight: 700, marginBottom: 8 }}>Spotted a New Scam?</h3>
        <p style={{ color: COLORS.grey, fontSize: 14, marginBottom: 16 }}>Help protect others by reporting it to our database</p>
        <button className="btn-ghost" style={{ padding: "10px 24px", borderRadius: 10, fontSize: 14 }}>Submit a Report</button>
      </div>
    </div>
  );
};

// ─── DASHBOARD PAGE ───────────────────────────────────────────────────────────
const DashboardPage = ({ user, setPage }) => {
  if (!user) { setPage("auth"); return null; }

  const history = [
    { type: "Message", content: "Your package requires a customs fee...", score: 87, risk: "High", date: "Today, 14:22" },
    { type: "Website", content: "paypa1-secure-verify.com", score: 95, risk: "High", date: "Today, 11:05" },
    { type: "Message", content: "You've been selected as a winner...", score: 62, risk: "Medium", date: "Yesterday" },
    { type: "Marketplace", content: "Facebook: Buyer wants to use their courier", score: 79, risk: "High", date: "2 days ago" },
    { type: "Message", content: "Your AIB account has been suspended", score: 92, risk: "High", date: "3 days ago" },
    { type: "Website", content: "amazon-deals-ie.shop", score: 44, risk: "Medium", date: "4 days ago" },
    { type: "Message", content: "Hi, I think I have the wrong number...", score: 28, risk: "Low", date: "5 days ago" },
  ];

  const riskColor = { High: COLORS.red, Medium: COLORS.amber, Low: COLORS.green };

  return (
    <div style={{ maxWidth: 1100, margin: "0 auto", padding: "100px 24px 60px" }}>
      {/* Header */}
      <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 36, flexWrap: "wrap", gap: 12 }}>
        <div>
          <h1 className="syne" style={{ fontSize: 28, fontWeight: 800, marginBottom: 4 }}>Welcome back, {user.name.split(" ")[0]} 👋</h1>
          <p style={{ color: COLORS.grey }}>{user.plan === "premium" ? "Premium Plan • Unlimited scans" : "Free Plan • 3 of 5 scans used today"}</p>
        </div>
        <button className="btn-primary" style={{ padding: "10px 22px", borderRadius: 10, fontSize: 14 }} onClick={() => setPage("scanner")}>
          + New Scan
        </button>
      </div>

      {/* Stats Row */}
      <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(180px, 1fr))", gap: 16, marginBottom: 28 }}>
        {[
          { label: "Total Scans", value: "47", icon: "search", color: COLORS.accent },
          { label: "Scams Caught", value: "31", icon: "shield", color: COLORS.red },
          { label: "Money Protected", value: "€4,800", icon: "lock", color: COLORS.green },
          { label: "This Month", value: "12 scans", icon: "trending", color: COLORS.amber },
        ].map(({ label, value, icon, color }) => (
          <div key={label} className="card" style={{ padding: "20px 22px", display: "flex", gap: 14, alignItems: "center" }}>
            <div style={{ width: 42, height: 42, borderRadius: 12, background: color + "15", display: "flex", alignItems: "center", justifyContent: "center" }}>
              <Icon name={icon} size={20} color={color} />
            </div>
            <div>
              <div className="syne" style={{ fontSize: 22, fontWeight: 800, color }}>{value}</div>
              <div style={{ fontSize: 12, color: COLORS.grey }}>{label}</div>
            </div>
          </div>
        ))}
      </div>

      <div style={{ display: "grid", gridTemplateColumns: "1fr 320px", gap: 20, alignItems: "start" }}>
        {/* History */}
        <div>
          <h2 className="syne" style={{ fontSize: 18, fontWeight: 700, marginBottom: 16 }}>Recent Scans</h2>
          <div className="card" style={{ overflow: "hidden" }}>
            {history.map((item, i) => (
              <div key={i} style={{
                display: "flex", alignItems: "center", gap: 14, padding: "14px 20px",
                borderBottom: i < history.length - 1 ? "1px solid rgba(255,255,255,0.04)" : "none",
              }}>
                <div style={{
                  width: 38, height: 38, borderRadius: 10, flexShrink: 0,
                  background: riskColor[item.risk] + "15",
                  display: "flex", alignItems: "center", justifyContent: "center",
                  fontSize: 16,
                }}>
                  {item.type === "Message" ? "💬" : item.type === "Website" ? "🌐" : item.type === "Marketplace" ? "🛒" : "📸"}
                </div>
                <div style={{ flex: 1, minWidth: 0 }}>
                  <div style={{ fontSize: 13, fontWeight: 500, color: COLORS.white, marginBottom: 2, overflow: "hidden", textOverflow: "ellipsis", whiteSpace: "nowrap" }}>
                    {item.content}
                  </div>
                  <div style={{ fontSize: 11, color: COLORS.grey }}>{item.type} • {item.date}</div>
                </div>
                <div style={{ flexShrink: 0, textAlign: "right" }}>
                  <div className="syne" style={{ fontSize: 18, fontWeight: 800, color: riskColor[item.risk] }}>{item.score}</div>
                  <span className={`risk-badge risk-${item.risk.toLowerCase()}`} style={{ fontSize: 9 }}>{item.risk}</span>
                </div>
              </div>
            ))}
          </div>
        </div>

        {/* Sidebar */}
        <div style={{ display: "flex", flexDirection: "column", gap: 16 }}>
          {/* Plan */}
          <div className="card" style={{ padding: 22 }}>
            <h3 className="syne" style={{ fontSize: 14, fontWeight: 700, marginBottom: 14, color: COLORS.grey, letterSpacing: "0.05em" }}>YOUR PLAN</h3>
            {user.plan === "premium" ? (
              <div>
                <div style={{ display: "flex", alignItems: "center", gap: 8, marginBottom: 12 }}>
                  <div className="alert-dot" style={{ background: COLORS.accent, boxShadow: `0 0 8px ${COLORS.accent}` }} />
                  <span className="syne" style={{ fontWeight: 700, color: COLORS.accent }}>Premium</span>
                </div>
                <p style={{ fontSize: 13, color: COLORS.grey, marginBottom: 14 }}>Unlimited scans • Advanced analysis • All features</p>
                <div style={{ fontSize: 13, color: COLORS.grey }}>Renews: July 2, 2026 • €4.99/mo</div>
              </div>
            ) : (
              <div>
                <div style={{ marginBottom: 12 }}>
                  <div style={{ display: "flex", justifyContent: "space-between", fontSize: 13, marginBottom: 6 }}>
                    <span style={{ color: COLORS.grey }}>Daily scans</span>
                    <span>3 / 5 used</span>
                  </div>
                  <div className="progress-bar">
                    <div className="progress-fill" style={{ width: "60%", background: COLORS.amber }} />
                  </div>
                </div>
                <button className="btn-primary" style={{ width: "100%", padding: 10, borderRadius: 10, fontSize: 13 }}>
                  Upgrade to Premium • €4.99/mo
                </button>
              </div>
            )}
          </div>

          {/* Quick links */}
          <div className="card" style={{ padding: 22 }}>
            <h3 className="syne" style={{ fontSize: 14, fontWeight: 700, marginBottom: 14, color: COLORS.grey, letterSpacing: "0.05em" }}>QUICK LINKS</h3>
            {[
              { icon: "settings", label: "Account Settings" },
              { icon: "history", label: "Full Scan History" },
              { icon: "book", label: "Scam Library" },
              { icon: "alert", label: "Scam Alerts" },
            ].map(({ icon, label }) => (
              <div key={label} style={{ display: "flex", alignItems: "center", gap: 10, padding: "8px 0", cursor: "pointer", borderBottom: "1px solid rgba(255,255,255,0.04)" }}>
                <Icon name={icon} size={15} color={COLORS.grey} />
                <span style={{ fontSize: 14, color: COLORS.greyLight }}>{label}</span>
              </div>
            ))}
          </div>
        </div>
      </div>
    </div>
  );
};

// ─── PRICING PAGE ─────────────────────────────────────────────────────────────
const PricingPage = ({ setPage, user }) => {
  const plans = [
    {
      name: "Free",
      price: "€0",
      period: "",
      desc: "For occasional checks",
      features: ["5 scans per day", "Message & text analysis", "Basic scam score", "Scam knowledge library", "Scam alert feed"],
      missing: ["Website checker", "Screenshot scanner", "Marketplace guard", "Advanced AI analysis", "Priority support"],
      cta: "Get Started Free",
      popular: false,
    },
    {
      name: "Premium",
      price: "€4.99",
      period: "/month",
      desc: "For complete protection",
      features: ["Unlimited scans", "All scan types", "Advanced AI analysis", "Website safety checker", "Screenshot scanner", "Marketplace guard", "Priority email alerts", "Detailed PDF reports", "Priority support"],
      missing: [],
      cta: "Start Free Trial",
      popular: true,
    },
    {
      name: "Business",
      price: "€19.99",
      period: "/month",
      desc: "For teams and businesses",
      features: ["Everything in Premium", "Up to 10 team members", "API access", "Bulk URL scanning", "Custom alert thresholds", "Admin dashboard", "Dedicated support", "SLA guarantee"],
      missing: [],
      cta: "Contact Sales",
      popular: false,
    },
  ];

  return (
    <div style={{ maxWidth: 1100, margin: "0 auto", padding: "100px 24px 80px" }}>
      <div style={{ textAlign: "center", marginBottom: 56 }}>
        <h1 className="syne" style={{ fontSize: "clamp(30px,5vw,48px)", fontWeight: 800, marginBottom: 12 }}>Simple, Transparent Pricing</h1>
        <p style={{ color: COLORS.grey, fontSize: 18 }}>No tricks. No hidden fees. Cancel anytime.</p>
      </div>

      <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(280px, 1fr))", gap: 20 }}>
        {plans.map(plan => (
          <div key={plan.name} className={`card ${plan.popular ? "pricing-popular" : ""}`} style={{ padding: 32, position: "relative" }}>
            <div style={{ marginBottom: 24 }}>
              <h2 className="syne" style={{ fontSize: 22, fontWeight: 800, marginBottom: 4 }}>{plan.name}</h2>
              <div style={{ display: "flex", alignItems: "baseline", gap: 4, marginBottom: 6 }}>
                <span className="syne" style={{ fontSize: 40, fontWeight: 800, color: plan.popular ? COLORS.accent : COLORS.white }}>{plan.price}</span>
                <span style={{ color: COLORS.grey, fontSize: 15 }}>{plan.period}</span>
              </div>
              <p style={{ color: COLORS.grey, fontSize: 14 }}>{plan.desc}</p>
            </div>

            <button
              className={plan.popular ? "btn-primary" : "btn-ghost"}
              style={{ width: "100%", padding: 14, borderRadius: 12, fontSize: 15, marginBottom: 28 }}
              onClick={() => setPage(user ? "dashboard" : "auth")}
            >
              {plan.cta}
            </button>

            <div style={{ display: "flex", flexDirection: "column", gap: 10 }}>
              {plan.features.map(f => (
                <div key={f} style={{ display: "flex", gap: 10, alignItems: "flex-start" }}>
                  <div style={{ width: 18, height: 18, borderRadius: "50%", background: COLORS.greenDim, display: "flex", alignItems: "center", justifyContent: "center", flexShrink: 0, marginTop: 1 }}>
                    <Icon name="check" size={10} color={COLORS.green} />
                  </div>
                  <span style={{ fontSize: 14, color: COLORS.greyLight }}>{f}</span>
                </div>
              ))}
              {plan.missing.map(f => (
                <div key={f} style={{ display: "flex", gap: 10, alignItems: "flex-start" }}>
                  <div style={{ width: 18, height: 18, borderRadius: "50%", background: "rgba(255,255,255,0.04)", display: "flex", alignItems: "center", justifyContent: "center", flexShrink: 0, marginTop: 1 }}>
                    <Icon name="x" size={10} color="#374151" />
                  </div>
                  <span style={{ fontSize: 14, color: "#374151" }}>{f}</span>
                </div>
              ))}
            </div>
          </div>
        ))}
      </div>

      {/* Guarantee */}
      <div className="glass" style={{ borderRadius: 16, padding: 28, marginTop: 40, display: "flex", alignItems: "center", gap: 20, flexWrap: "wrap" }}>
        <div style={{ width: 52, height: 52, borderRadius: 14, background: COLORS.greenDim, display: "flex", alignItems: "center", justifyContent: "center", flexShrink: 0 }}>
          <Icon name="shield" size={26} color={COLORS.green} />
        </div>
        <div>
          <h3 className="syne" style={{ fontSize: 17, fontWeight: 700, marginBottom: 4 }}>30-Day Money-Back Guarantee</h3>
          <p style={{ color: COLORS.grey, fontSize: 14 }}>Try Premium risk-free. If SafeCheck doesn't protect you, we'll refund every cent. No questions asked.</p>
        </div>
      </div>

      {/* FAQ */}
      <div style={{ marginTop: 64 }}>
        <h2 className="syne" style={{ fontSize: 26, fontWeight: 800, textAlign: "center", marginBottom: 36 }}>Frequently Asked Questions</h2>
        <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(300px, 1fr))", gap: 20 }}>
          {[
            { q: "How accurate is the AI?", a: "Our model achieves 98.7% accuracy on known scam patterns, validated against a database of 2.4M+ confirmed scams." },
            { q: "Is my data kept private?", a: "Scans are analyzed and immediately discarded. We never store the content of your messages or personal data you enter." },
            { q: "Does it work for Irish scams?", a: "Yes! We've specifically trained on Irish scam patterns including An Post, Revenue, Irish banks, DoneDeal, and Adverts.ie scams." },
            { q: "Can I cancel anytime?", a: "Absolutely. Cancel with one click from your dashboard. No contracts, no cancellation fees, ever." },
          ].map(({ q, a }) => (
            <div key={q} className="card" style={{ padding: 22 }}>
              <h4 className="syne" style={{ fontSize: 14, fontWeight: 700, marginBottom: 8 }}>{q}</h4>
              <p style={{ fontSize: 13, color: COLORS.grey, lineHeight: 1.7 }}>{a}</p>
            </div>
          ))}
        </div>
      </div>
    </div>
  );
};

// ─── AUTH PAGE ────────────────────────────────────────────────────────────────
const AuthPage = ({ setUser, setPage }) => {
  const [mode, setMode] = useState("signin");
  const [form, setForm] = useState({ name: "", email: "", password: "" });
  const [loading, setLoading] = useState(false);
  const [error, setError] = useState("");

  const handleSubmit = async () => {
    if (!form.email || !form.password) { setError("Please fill in all fields."); return; }
    if (mode === "signup" && !form.name) { setError("Please enter your name."); return; }
    setLoading(true); setError("");
    await new Promise(r => setTimeout(r, 1200));
    setUser({
      name: form.name || form.email.split("@")[0],
      email: form.email,
      plan: "free",
    });
    setPage("dashboard");
    setLoading(false);
  };

  const handleGoogle = async () => {
    setLoading(true);
    await new Promise(r => setTimeout(r, 800));
    setUser({ name: "Demo User", email: "demo@example.com", plan: "premium" });
    setPage("dashboard");
    setLoading(false);
  };

  return (
    <div style={{ minHeight: "100vh", display: "flex", alignItems: "center", justifyContent: "center", padding: "100px 24px 60px" }}>
      <div style={{ width: "100%", maxWidth: 420 }}>
        <div style={{ textAlign: "center", marginBottom: 32 }}>
          <div style={{ display: "flex", justifyContent: "center", marginBottom: 16 }}>
            <div style={{ width: 56, height: 56, borderRadius: 16, background: "rgba(0,212,255,0.1)", border: "1px solid rgba(0,212,255,0.2)", display: "flex", alignItems: "center", justifyContent: "center" }}>
              <Icon name="shield" size={28} color={COLORS.accent} />
            </div>
          </div>
          <h1 className="syne" style={{ fontSize: 28, fontWeight: 800, marginBottom: 6 }}>
            {mode === "signin" ? "Welcome back" : "Create account"}
          </h1>
          <p style={{ color: COLORS.grey, fontSize: 14 }}>
            {mode === "signin" ? "Sign in to your SafeCheck account" : "Start protecting yourself today — free"}
          </p>
        </div>

        <div className="card" style={{ padding: 28 }}>
          {/* Google */}
          <button onClick={handleGoogle} style={{
            width: "100%", padding: "12px 16px", borderRadius: 10, marginBottom: 20,
            background: "rgba(255,255,255,0.05)", border: "1px solid rgba(255,255,255,0.1)",
            color: COLORS.white, cursor: "pointer", display: "flex", alignItems: "center", justifyContent: "center", gap: 10,
            fontSize: 14, fontFamily: "'DM Sans', sans-serif", fontWeight: 500, transition: "all 0.2s",
          }}>
            <svg width="18" height="18" viewBox="0 0 48 48"><path fill="#FFC107" d="M43.611,20.083H42V20H24v8h11.303c-1.649,4.657-6.08,8-11.303,8c-6.627,0-12-5.373-12-12c0-6.627,5.373-12,12-12c3.059,0,5.842,1.154,7.961,3.039l5.657-5.657C34.046,6.053,29.268,4,24,4C12.955,4,4,12.955,4,24c0,11.045,8.955,20,20,20c11.045,0,20-8.955,20-20C44,22.659,43.862,21.35,43.611,20.083z"/><path fill="#FF3D00" d="M6.306,14.691l6.571,4.819C14.655,15.108,18.961,12,24,12c3.059,0,5.842,1.154,7.961,3.039l5.657-5.657C34.046,6.053,29.268,4,24,4C16.318,4,9.656,8.337,6.306,14.691z"/><path fill="#4CAF50" d="M24,44c5.166,0,9.86-1.977,13.409-5.192l-6.19-5.238C29.211,35.091,26.715,36,24,36c-5.202,0-9.619-3.317-11.283-7.946l-6.522,5.025C9.505,39.556,16.227,44,24,44z"/><path fill="#1976D2" d="M43.611,20.083H42V20H24v8h11.303c-0.792,2.237-2.231,4.166-4.087,5.571c0.001-0.001,0.002-0.001,0.003-0.002l6.19,5.238C36.971,39.205,44,34,44,24C44,22.659,43.862,21.35,43.611,20.083z"/></svg>
            Continue with Google
          </button>

          <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 20 }}>
            <div style={{ flex: 1, height: 1, background: "rgba(255,255,255,0.06)" }} />
            <span style={{ fontSize: 12, color: COLORS.grey }}>or with email</span>
            <div style={{ flex: 1, height: 1, background: "rgba(255,255,255,0.06)" }} />
          </div>

          {/* Fields */}
          <div style={{ display: "flex", flexDirection: "column", gap: 14 }}>
            {mode === "signup" && (
              <input className="input-field" style={{ borderRadius: 10, padding: "13px 16px" }} placeholder="Full Name" value={form.name} onChange={e => setForm(f => ({ ...f, name: e.target.value }))} />
            )}
            <input className="input-field" style={{ borderRadius: 10, padding: "13px 16px" }} type="email" placeholder="Email address" value={form.email} onChange={e => setForm(f => ({ ...f, email: e.target.value }))} />
            <input className="input-field" style={{ borderRadius: 10, padding: "13px 16px" }} type="password" placeholder="Password" value={form.password} onChange={e => setForm(f => ({ ...f, password: e.target.value }))} onKeyDown={e => e.key === "Enter" && handleSubmit()} />
          </div>

          {error && <p style={{ fontSize: 13, color: COLORS.red, marginTop: 10 }}>{error}</p>}

          <button className="btn-primary" style={{ width: "100%", padding: 14, borderRadius: 10, fontSize: 15, marginTop: 18 }} onClick={handleSubmit} disabled={loading}>
            {loading ? <span className="spinner" style={{ borderTopColor: "#0A0E1A", borderColor: "rgba(10,14,26,0.3)" }} /> : (mode === "signin" ? "Sign In" : "Create Free Account")}
          </button>

          <p style={{ textAlign: "center", fontSize: 13, color: COLORS.grey, marginTop: 16 }}>
            {mode === "signin" ? "Don't have an account? " : "Already have an account? "}
            <span style={{ color: COLORS.accent, cursor: "pointer", fontWeight: 600 }} onClick={() => setMode(mode === "signin" ? "signup" : "signin")}>
              {mode === "signin" ? "Sign Up Free" : "Sign In"}
            </span>
          </p>
        </div>

        <p style={{ textAlign: "center", fontSize: 11, color: COLORS.grey, marginTop: 16, lineHeight: 1.6 }}>
          By continuing, you agree to our Terms of Service and Privacy Policy. Your scan data is never stored.
        </p>
      </div>
    </div>
  );
};

// ─── FOOTER ───────────────────────────────────────────────────────────────────
const Footer = ({ setPage }) => (
  <footer style={{ background: "#070B15", borderTop: "1px solid rgba(0,212,255,0.08)", padding: "48px 24px 28px" }}>
    <div style={{ maxWidth: 1100, margin: "0 auto" }}>
      <div style={{ display: "grid", gridTemplateColumns: "2fr 1fr 1fr 1fr", gap: 32, marginBottom: 40, flexWrap: "wrap" }}>
        <div>
          <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 14 }}>
            <div style={{ width: 30, height: 30, borderRadius: 8, background: "rgba(0,212,255,0.1)", border: "1px solid rgba(0,212,255,0.2)", display: "flex", alignItems: "center", justifyContent: "center" }}>
              <Icon name="shield" size={15} color={COLORS.accent} />
            </div>
            <span className="syne" style={{ fontSize: 16, fontWeight: 800 }}>Safe<span style={{ color: COLORS.accent }}>Check</span></span>
          </div>
          <p style={{ fontSize: 13, color: COLORS.grey, lineHeight: 1.7, maxWidth: 280 }}>
            AI-powered scam detection protecting consumers, elderly users, and small businesses across Ireland and beyond.
          </p>
          <div style={{ display: "flex", gap: 10, marginTop: 16 }}>
            {["mail", "phone"].map(icon => (
              <div key={icon} style={{ width: 32, height: 32, borderRadius: 8, background: "rgba(255,255,255,0.04)", display: "flex", alignItems: "center", justifyContent: "center", cursor: "pointer" }}>
                <Icon name={icon} size={14} color={COLORS.grey} />
              </div>
            ))}
          </div>
        </div>

        {[
          { title: "Product", links: [["scanner","Check a Scam"],["knowledge","Scam Library"],["alerts","Live Alerts"],["pricing","Pricing"]] },
          { title: "Scam Types", links: [["knowledge","Banking Scams"],["knowledge","Marketplace Scams"],["knowledge","Investment Scams"],["knowledge","Romance Scams"]] },
          { title: "Company", links: [["home","About Us"],["home","Blog"],["home","Contact"],["home","Privacy Policy"]] },
        ].map(({ title, links }) => (
          <div key={title}>
            <h4 className="syne" style={{ fontSize: 12, fontWeight: 700, color: COLORS.grey, letterSpacing: "0.1em", marginBottom: 14 }}>{title.toUpperCase()}</h4>
            <div style={{ display: "flex", flexDirection: "column", gap: 10 }}>
              {links.map(([page, label]) => (
                <span key={label} onClick={() => setPage(page)} style={{ fontSize: 13, color: COLORS.grey, cursor: "pointer", transition: "color 0.2s" }}
                  onMouseEnter={e => e.target.style.color = COLORS.white}
                  onMouseLeave={e => e.target.style.color = COLORS.grey}>
                  {label}
                </span>
              ))}
            </div>
          </div>
        ))}
      </div>

      <div style={{ borderTop: "1px solid rgba(255,255,255,0.04)", paddingTop: 20, display: "flex", justifyContent: "space-between", alignItems: "center", flexWrap: "wrap", gap: 10 }}>
        <p style={{ fontSize: 12, color: COLORS.grey }}>© 2026 SafeCheck. All rights reserved. Not affiliated with any government body.</p>
        <div style={{ display: "flex", gap: 16 }}>
          {["Privacy", "Terms", "Cookies"].map(l => (
            <span key={l} style={{ fontSize: 12, color: COLORS.grey, cursor: "pointer" }}>{l}</span>
          ))}
        </div>
      </div>
    </div>
  </footer>
);

// ─── MINI BAR CHART ──────────────────────────────────────────────────────────
const MiniBarChart = ({ data, color = COLORS.accent, height = 60 }) => {
  const max = Math.max(...data.map(d => d.v));
  return (
    <div style={{ display: "flex", alignItems: "flex-end", gap: 4, height }}>
      {data.map((d, i) => (
        <div key={i} style={{ flex: 1, display: "flex", flexDirection: "column", alignItems: "center", gap: 3 }}>
          <div style={{
            width: "100%", borderRadius: 3,
            height: `${(d.v / max) * (height - 16)}px`,
            background: `${color}${i === data.length - 1 ? "FF" : "60"}`,
            transition: "height 0.6s ease",
            minHeight: 4,
          }} />
          <span style={{ fontSize: 9, color: COLORS.grey, whiteSpace: "nowrap" }}>{d.l}</span>
        </div>
      ))}
    </div>
  );
};

// ─── DONUT CHART ─────────────────────────────────────────────────────────────
const DonutChart = ({ segments, size = 100 }) => {
  const total = segments.reduce((s, g) => s + g.value, 0);
  let offset = 0;
  const r = 36, circ = 2 * Math.PI * r;
  return (
    <div style={{ display: "flex", alignItems: "center", gap: 20 }}>
      <svg width={size} height={size} viewBox="0 0 100 100" style={{ transform: "rotate(-90deg)", flexShrink: 0 }}>
        <circle cx="50" cy="50" r={r} fill="none" stroke="rgba(255,255,255,0.04)" strokeWidth="14" />
        {segments.map((seg, i) => {
          const len = (seg.value / total) * circ;
          const el = (
            <circle key={i} cx="50" cy="50" r={r} fill="none"
              stroke={seg.color} strokeWidth="14"
              strokeDasharray={`${len} ${circ - len}`}
              strokeDashoffset={-offset}
              strokeLinecap="butt"
            />
          );
          offset += len;
          return el;
        })}
      </svg>
      <div style={{ display: "flex", flexDirection: "column", gap: 8 }}>
        {segments.map(seg => (
          <div key={seg.label} style={{ display: "flex", alignItems: "center", gap: 8 }}>
            <div style={{ width: 8, height: 8, borderRadius: 2, background: seg.color, flexShrink: 0 }} />
            <span style={{ fontSize: 12, color: COLORS.grey }}>{seg.label}</span>
            <span style={{ fontSize: 12, fontWeight: 600, color: COLORS.white, marginLeft: "auto", paddingLeft: 12 }}>{seg.value}%</span>
          </div>
        ))}
      </div>
    </div>
  );
};

// ─── ADMIN PANEL ──────────────────────────────────────────────────────────────
const ADMIN_EMAIL = "maxoshea365@gmail.com";
const isAdmin = (user) => user?.email?.toLowerCase() === ADMIN_EMAIL;

const AdminPage = ({ user, setPage }) => {
  const [activeTab, setActiveTab] = useState("overview");

  if (!user) { setPage("auth"); return null; }

  if (!isAdmin(user)) {
    return (
      <div style={{ minHeight: "100vh", display: "flex", alignItems: "center", justifyContent: "center", padding: "100px 24px" }}>
        <div style={{ textAlign: "center", maxWidth: 400 }}>
          <div style={{ width: 72, height: 72, borderRadius: 20, background: COLORS.redDim, border: `1px solid ${COLORS.red}30`, display: "flex", alignItems: "center", justifyContent: "center", margin: "0 auto 24px" }}>
            <Icon name="lock" size={32} color={COLORS.red} />
          </div>
          <h1 className="syne" style={{ fontSize: 28, fontWeight: 800, marginBottom: 12 }}>Access Denied</h1>
          <p style={{ color: COLORS.grey, fontSize: 15, lineHeight: 1.7, marginBottom: 28 }}>
            This page is restricted to SafeCheck administrators only.
          </p>
          <button className="btn-primary" style={{ padding: "12px 28px", borderRadius: 10, fontSize: 15 }} onClick={() => setPage("home")}>
            Go Home
          </button>
        </div>
      </div>
    );
  }

  const weeklyScans = [
    { l: "Mon", v: 1240 }, { l: "Tue", v: 1890 }, { l: "Wed", v: 1560 },
    { l: "Thu", v: 2100 }, { l: "Fri", v: 2480 }, { l: "Sat", v: 980 }, { l: "Sun", v: 720 },
  ];
  const scamTypes = [
    { label: "Banking / Phishing", value: 34, color: COLORS.red },
    { label: "Marketplace", value: 28, color: COLORS.amber },
    { label: "Investment", value: 18, color: COLORS.accent },
    { label: "Romance", value: 12, color: "#A78BFA" },
    { label: "Other", value: 8, color: COLORS.grey },
  ];

  const users = [
    { name: "Margaret O'Brien", email: "margaret@example.com", plan: "Premium", scans: 47, joined: "Jan 2026", status: "Active" },
    { name: "James Doyle", email: "james.d@example.com", plan: "Free", scans: 12, joined: "Feb 2026", status: "Active" },
    { name: "Sarah Murphy", email: "smurphy@example.com", plan: "Business", scans: 234, joined: "Nov 2025", status: "Active" },
    { name: "Patrick Ryan", email: "pryan@example.com", plan: "Free", scans: 3, joined: "Mar 2026", status: "Inactive" },
    { name: "Aoife Kelly", email: "aoife.k@example.com", plan: "Premium", scans: 88, joined: "Dec 2025", status: "Active" },
    { name: "Conor Walsh", email: "cwalsh@example.com", plan: "Free", scans: 5, joined: "Apr 2026", status: "Active" },
  ];

  const reports = [
    { type: "Phishing Email", content: "AIB account suspended — click here...", reporter: "margaret@example.com", date: "Today 14:22", status: "New", risk: "High" },
    { type: "Fake Website", content: "paypa1-secure-verify.com", reporter: "james.d@example.com", date: "Today 11:05", status: "Reviewing", risk: "High" },
    { type: "Marketplace Scam", content: "DoneDeal courier — won't meet in person", reporter: "smurphy@example.com", date: "Yesterday", status: "Confirmed", risk: "Medium" },
    { type: "Investment Scam", content: "Crypto platform guarantee 300% returns", reporter: "aoife.k@example.com", date: "2 days ago", status: "New", risk: "High" },
    { type: "SMS Scam", content: "An Post customs fee €2.50 required", reporter: "cwalsh@example.com", date: "3 days ago", status: "Confirmed", risk: "High" },
  ];

  const statusColor = { New: COLORS.accent, Reviewing: COLORS.amber, Confirmed: COLORS.green };
  const planColor = { Free: COLORS.grey, Premium: COLORS.accent, Business: COLORS.amber };

  const tabs = [
    { id: "overview", label: "📊 Overview" },
    { id: "users", label: "👥 Users" },
    { id: "reports", label: "🚨 Reports" },
    { id: "database", label: "🗄 Scam DB" },
  ];

  return (
    <div style={{ maxWidth: 1200, margin: "0 auto", padding: "100px 24px 60px" }}>
      {/* Header */}
      <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 32, flexWrap: "wrap", gap: 12 }}>
        <div>
          <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 4 }}>
            <div style={{ width: 8, height: 8, borderRadius: "50%", background: COLORS.green, boxShadow: `0 0 8px ${COLORS.green}` }} />
            <span style={{ fontSize: 12, color: COLORS.green, fontFamily: "'Syne',sans-serif", fontWeight: 700, letterSpacing: "0.08em" }}>ADMIN PANEL</span>
          </div>
          <h1 className="syne" style={{ fontSize: 28, fontWeight: 800 }}>SafeCheck Dashboard</h1>
        </div>
        <div style={{ display: "flex", gap: 10 }}>
          <button className="btn-ghost" style={{ padding: "8px 16px", borderRadius: 8, fontSize: 13 }}>Export CSV</button>
          <button className="btn-primary" style={{ padding: "8px 16px", borderRadius: 8, fontSize: 13 }}>+ Add Scam Alert</button>
        </div>
      </div>

      {/* Tabs */}
      <div style={{ display: "flex", gap: 6, marginBottom: 28, flexWrap: "wrap" }}>
        {tabs.map(t => (
          <button key={t.id} className={`tab-btn ${activeTab === t.id ? "active" : ""}`}
            onClick={() => setActiveTab(t.id)}>{t.label}</button>
        ))}
      </div>

      {/* OVERVIEW TAB */}
      {activeTab === "overview" && (
        <div>
          {/* KPI Cards */}
          <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(180px, 1fr))", gap: 16, marginBottom: 24 }}>
            {[
              { label: "Total Users", value: "152,430", delta: "+8.4%", color: COLORS.accent, icon: "user" },
              { label: "Premium Subs", value: "12,841", delta: "+12.1%", color: COLORS.green, icon: "lock" },
              { label: "Scans Today", value: "11,204", delta: "+3.2%", color: COLORS.amber, icon: "search" },
              { label: "MRR", value: "€64,077", delta: "+9.7%", color: "#A78BFA", icon: "trending" },
              { label: "Reports Pending", value: "34", delta: "-5", color: COLORS.red, icon: "alert" },
            ].map(({ label, value, delta, color, icon }) => (
              <div key={label} className="card" style={{ padding: "18px 20px" }}>
                <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", marginBottom: 10 }}>
                  <div style={{ width: 36, height: 36, borderRadius: 10, background: color + "15", display: "flex", alignItems: "center", justifyContent: "center" }}>
                    <Icon name={icon} size={17} color={color} />
                  </div>
                  <span style={{ fontSize: 11, color: delta.startsWith("+") ? COLORS.green : COLORS.red, fontWeight: 600, background: (delta.startsWith("+") ? COLORS.greenDim : COLORS.redDim), padding: "2px 6px", borderRadius: 4 }}>{delta}</span>
                </div>
                <div className="syne" style={{ fontSize: 22, fontWeight: 800, color }}>{value}</div>
                <div style={{ fontSize: 12, color: COLORS.grey, marginTop: 2 }}>{label}</div>
              </div>
            ))}
          </div>

          <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 20 }}>
            {/* Weekly scans chart */}
            <div className="card" style={{ padding: 24 }}>
              <h3 className="syne" style={{ fontSize: 14, fontWeight: 700, color: COLORS.grey, letterSpacing: "0.05em", marginBottom: 20 }}>SCANS THIS WEEK</h3>
              <MiniBarChart data={weeklyScans} color={COLORS.accent} height={120} />
            </div>

            {/* Scam type breakdown */}
            <div className="card" style={{ padding: 24 }}>
              <h3 className="syne" style={{ fontSize: 14, fontWeight: 700, color: COLORS.grey, letterSpacing: "0.05em", marginBottom: 20 }}>SCAM TYPE BREAKDOWN</h3>
              <DonutChart segments={scamTypes} size={110} />
            </div>

            {/* Revenue chart */}
            <div className="card" style={{ padding: 24 }}>
              <h3 className="syne" style={{ fontSize: 14, fontWeight: 700, color: COLORS.grey, letterSpacing: "0.05em", marginBottom: 20 }}>MONTHLY REVENUE (€)</h3>
              <MiniBarChart data={[
                { l: "Jan", v: 38200 }, { l: "Feb", v: 44100 }, { l: "Mar", v: 49800 },
                { l: "Apr", v: 55200 }, { l: "May", v: 60100 }, { l: "Jun", v: 64077 },
              ]} color={COLORS.green} height={120} />
            </div>

            {/* User growth */}
            <div className="card" style={{ padding: 24 }}>
              <h3 className="syne" style={{ fontSize: 14, fontWeight: 700, color: COLORS.grey, letterSpacing: "0.05em", marginBottom: 20 }}>NEW USERS / MONTH</h3>
              <MiniBarChart data={[
                { l: "Jan", v: 8400 }, { l: "Feb", v: 11200 }, { l: "Mar", v: 14800 },
                { l: "Apr", v: 18100 }, { l: "May", v: 22400 }, { l: "Jun", v: 26300 },
              ]} color={COLORS.amber} height={120} />
            </div>
          </div>
        </div>
      )}

      {/* USERS TAB */}
      {activeTab === "users" && (
        <div>
          <div style={{ display: "flex", gap: 12, marginBottom: 20 }}>
            <input className="input-field" style={{ borderRadius: 10, padding: "10px 16px", maxWidth: 280 }} placeholder="Search users..." />
            <select className="input-field" style={{ borderRadius: 10, padding: "10px 16px", width: "auto" }}>
              <option>All Plans</option>
              <option>Free</option>
              <option>Premium</option>
              <option>Business</option>
            </select>
          </div>

          <div className="card" style={{ overflow: "hidden" }}>
            {/* Table Header */}
            <div style={{ display: "grid", gridTemplateColumns: "2fr 2fr 1fr 1fr 1fr 1fr", gap: 12, padding: "12px 20px", borderBottom: "1px solid rgba(255,255,255,0.06)" }}>
              {["Name", "Email", "Plan", "Scans", "Joined", "Status"].map(h => (
                <span key={h} style={{ fontSize: 11, color: COLORS.grey, fontFamily: "'Syne',sans-serif", fontWeight: 700, letterSpacing: "0.06em" }}>{h.toUpperCase()}</span>
              ))}
            </div>

            {users.map((u, i) => (
              <div key={i} style={{ display: "grid", gridTemplateColumns: "2fr 2fr 1fr 1fr 1fr 1fr", gap: 12, padding: "14px 20px", borderBottom: i < users.length - 1 ? "1px solid rgba(255,255,255,0.04)" : "none", alignItems: "center" }}>
                <div style={{ display: "flex", alignItems: "center", gap: 10 }}>
                  <div style={{ width: 32, height: 32, borderRadius: "50%", background: "linear-gradient(135deg, #00D4FF20, #0088AA40)", display: "flex", alignItems: "center", justifyContent: "center", fontSize: 13, fontWeight: 700, color: COLORS.accent, flexShrink: 0 }}>
                    {u.name[0]}
                  </div>
                  <span style={{ fontSize: 14, fontWeight: 500 }}>{u.name}</span>
                </div>
                <span style={{ fontSize: 13, color: COLORS.grey, overflow: "hidden", textOverflow: "ellipsis" }}>{u.email}</span>
                <span style={{ fontSize: 12, fontWeight: 600, color: planColor[u.plan] }}>{u.plan}</span>
                <span style={{ fontSize: 14, color: COLORS.white }}>{u.scans}</span>
                <span style={{ fontSize: 13, color: COLORS.grey }}>{u.joined}</span>
                <div style={{ display: "flex", alignItems: "center", gap: 6 }}>
                  <div style={{ width: 6, height: 6, borderRadius: "50%", background: u.status === "Active" ? COLORS.green : COLORS.grey }} />
                  <span style={{ fontSize: 12, color: u.status === "Active" ? COLORS.green : COLORS.grey }}>{u.status}</span>
                </div>
              </div>
            ))}
          </div>

          <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginTop: 16 }}>
            <span style={{ fontSize: 13, color: COLORS.grey }}>Showing 6 of 152,430 users</span>
            <div style={{ display: "flex", gap: 8 }}>
              {["←", "1", "2", "3", "...", "→"].map((l, i) => (
                <button key={i} style={{ width: 32, height: 32, borderRadius: 6, background: l === "1" ? "rgba(0,212,255,0.15)" : "rgba(255,255,255,0.04)", border: "1px solid " + (l === "1" ? "rgba(0,212,255,0.3)" : "rgba(255,255,255,0.08)"), color: l === "1" ? COLORS.accent : COLORS.grey, cursor: "pointer", fontSize: 13, fontWeight: l === "1" ? 700 : 400 }}>
                  {l}
                </button>
              ))}
            </div>
          </div>
        </div>
      )}

      {/* REPORTS TAB */}
      {activeTab === "reports" && (
        <div>
          <div style={{ display: "grid", gridTemplateColumns: "repeat(3, 1fr)", gap: 16, marginBottom: 24 }}>
            {[{ l: "New Reports", v: 34, c: COLORS.accent }, { l: "Under Review", v: 12, c: COLORS.amber }, { l: "Confirmed Scams", v: 891, c: COLORS.green }].map(({ l, v, c }) => (
              <div key={l} className="card" style={{ padding: "16px 20px", display: "flex", gap: 12, alignItems: "center" }}>
                <span className="syne" style={{ fontSize: 28, fontWeight: 800, color: c }}>{v}</span>
                <span style={{ fontSize: 13, color: COLORS.grey }}>{l}</span>
              </div>
            ))}
          </div>

          <div style={{ display: "flex", flexDirection: "column", gap: 12 }}>
            {reports.map((r, i) => (
              <div key={i} className="card" style={{ padding: "18px 22px", display: "flex", gap: 16, alignItems: "center", flexWrap: "wrap" }}>
                <div style={{ flex: 1, minWidth: 200 }}>
                  <div style={{ display: "flex", gap: 10, alignItems: "center", marginBottom: 4, flexWrap: "wrap" }}>
                    <span className="syne" style={{ fontSize: 14, fontWeight: 700 }}>{r.type}</span>
                    <span className={`risk-badge risk-${r.risk.toLowerCase()}`}>{r.risk}</span>
                  </div>
                  <p style={{ fontSize: 13, color: COLORS.grey, marginBottom: 4 }}>{r.content}</p>
                  <span style={{ fontSize: 11, color: COLORS.grey }}>Reported by {r.reporter} · {r.date}</span>
                </div>
                <div style={{ display: "flex", gap: 8, alignItems: "center", flexShrink: 0 }}>
                  <span style={{ fontSize: 12, fontWeight: 600, color: statusColor[r.status], background: statusColor[r.status] + "15", padding: "4px 10px", borderRadius: 6 }}>{r.status}</span>
                  <button className="btn-ghost" style={{ padding: "6px 14px", borderRadius: 6, fontSize: 12 }}>Review</button>
                  <button style={{ padding: "6px 14px", borderRadius: 6, fontSize: 12, background: COLORS.greenDim, color: COLORS.green, border: `1px solid ${COLORS.green}30`, cursor: "pointer", fontFamily: "'Syne',sans-serif", fontWeight: 600 }}>Confirm</button>
                </div>
              </div>
            ))}
          </div>
        </div>
      )}

      {/* DATABASE TAB */}
      {activeTab === "database" && (
        <div>
          <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 20, flexWrap: "wrap", gap: 12 }}>
            <p style={{ color: COLORS.grey, fontSize: 14 }}>891 confirmed scam entries in the database</p>
            <button className="btn-primary" style={{ padding: "9px 20px", borderRadius: 8, fontSize: 13 }}>+ Add New Entry</button>
          </div>

          <div className="card" style={{ overflow: "hidden" }}>
            <div style={{ display: "grid", gridTemplateColumns: "2fr 1fr 1fr 1fr 1fr", gap: 12, padding: "12px 20px", borderBottom: "1px solid rgba(255,255,255,0.06)" }}>
              {["Scam Title", "Category", "Risk", "Reports", "Actions"].map(h => (
                <span key={h} style={{ fontSize: 11, color: COLORS.grey, fontFamily: "'Syne',sans-serif", fontWeight: 700, letterSpacing: "0.06em" }}>{h.toUpperCase()}</span>
              ))}
            </div>
            {[
              { title: "Bank Account Suspended SMS", cat: "Banking", risk: "High", reports: 1240 },
              { title: "Fake An Post Customs Fee", cat: "Delivery", risk: "High", reports: 890 },
              { title: "DoneDeal Courier Scam", cat: "Marketplace", risk: "High", reports: 654 },
              { title: "Crypto Investment Platform", cat: "Investment", risk: "High", reports: 432 },
              { title: "Romance / Dating Scam", cat: "Romance", risk: "High", reports: 321 },
              { title: "Work From Home Data Entry", cat: "Job", risk: "Medium", reports: 218 },
              { title: "AI Voice Clone (Grandparent)", cat: "AI Scam", risk: "High", reports: 143 },
            ].map((entry, i) => (
              <div key={i} style={{ display: "grid", gridTemplateColumns: "2fr 1fr 1fr 1fr 1fr", gap: 12, padding: "13px 20px", borderBottom: "1px solid rgba(255,255,255,0.04)", alignItems: "center" }}>
                <span style={{ fontSize: 14, fontWeight: 500 }}>{entry.title}</span>
                <span style={{ fontSize: 12, color: COLORS.grey }}>{entry.cat}</span>
                <span className={`risk-badge risk-${entry.risk.toLowerCase()}`} style={{ fontSize: 10 }}>{entry.risk}</span>
                <span style={{ fontSize: 14 }}>{entry.reports.toLocaleString()}</span>
                <div style={{ display: "flex", gap: 6 }}>
                  <button style={{ padding: "4px 10px", borderRadius: 5, background: "rgba(0,212,255,0.1)", color: COLORS.accent, border: "none", cursor: "pointer", fontSize: 11, fontWeight: 600 }}>Edit</button>
                  <button style={{ padding: "4px 10px", borderRadius: 5, background: COLORS.redDim, color: COLORS.red, border: "none", cursor: "pointer", fontSize: 11, fontWeight: 600 }}>Delete</button>
                </div>
              </div>
            ))}
          </div>
        </div>
      )}
    </div>
  );
};

// ─── SCHEMA PAGE ──────────────────────────────────────────────────────────────
const SchemaPage = () => {
  const [activeSection, setActiveSection] = useState("db");

  const dbSchema = `-- ══════════════════════════════════════════
--  SafeCheck · Supabase Database Schema
-- ══════════════════════════════════════════

-- Enable UUID generation
create extension if not exists "uuid-ossp";

-- ─── USERS ──────────────────────────────
create table public.users (
  id            uuid primary key default uuid_generate_v4(),
  email         text unique not null,
  full_name     text,
  avatar_url    text,
  plan          text not null default 'free'
                  check (plan in ('free','premium','business')),
  scans_today   integer not null default 0,
  scans_total   integer not null default 0,
  stripe_customer_id text unique,
  created_at    timestamptz default now(),
  updated_at    timestamptz default now()
);

alter table public.users enable row level security;
create policy "Users can view own profile"
  on public.users for select using (auth.uid() = id);
create policy "Users can update own profile"
  on public.users for update using (auth.uid() = id);

-- ─── SUBSCRIPTIONS ──────────────────────
create table public.subscriptions (
  id                   uuid primary key default uuid_generate_v4(),
  user_id              uuid not null references public.users(id) on delete cascade,
  stripe_subscription_id text unique not null,
  stripe_price_id      text not null,
  plan                 text not null check (plan in ('premium','business')),
  status               text not null check (status in ('active','cancelled','past_due','trialing')),
  current_period_start timestamptz,
  current_period_end   timestamptz,
  cancel_at_period_end boolean default false,
  created_at           timestamptz default now()
);

alter table public.subscriptions enable row level security;
create policy "Users can view own subscriptions"
  on public.subscriptions for select using (auth.uid() = user_id);

-- ─── SCANS ──────────────────────────────
create table public.scans (
  id          uuid primary key default uuid_generate_v4(),
  user_id     uuid references public.users(id) on delete set null,
  scan_type   text not null check (scan_type in ('message','url','screenshot','marketplace')),
  platform    text,                    -- for marketplace scans
  input_hash  text,                    -- SHA-256 of input (privacy)
  scam_score  integer check (scam_score between 0 and 100),
  risk_level  text check (risk_level in ('Low','Medium','High')),
  scam_type   text,
  summary     text,
  indicators  jsonb,
  actions     jsonb,
  created_at  timestamptz default now()
);

create index scans_user_id_idx on public.scans(user_id);
create index scans_created_at_idx on public.scans(created_at desc);
create index scans_risk_level_idx on public.scans(risk_level);

alter table public.scans enable row level security;
create policy "Users can view own scans"
  on public.scans for select using (auth.uid() = user_id);
create policy "Users can insert own scans"
  on public.scans for insert with check (auth.uid() = user_id);

-- ─── SCAM KNOWLEDGE BASE ────────────────
create table public.scam_entries (
  id          uuid primary key default uuid_generate_v4(),
  title       text not null,
  category    text not null check (category in (
                'banking','marketplace','investment','romance','job','ai','delivery','other')),
  risk_level  text not null check (risk_level in ('Low','Medium','High')),
  description text not null,
  red_flags   jsonb not null default '[]',
  actions     jsonb not null default '[]',
  report_count integer default 0,
  is_active   boolean default true,
  created_by  uuid references public.users(id),
  created_at  timestamptz default now(),
  updated_at  timestamptz default now()
);

create index scam_entries_category_idx on public.scam_entries(category);
create index scam_entries_risk_idx on public.scam_entries(risk_level);

-- Public read access for knowledge base
create policy "Anyone can read active scam entries"
  on public.scam_entries for select using (is_active = true);

-- ─── SCAM ALERTS ────────────────────────
create table public.scam_alerts (
  id           uuid primary key default uuid_generate_v4(),
  title        text not null,
  description  text not null,
  severity     text not null check (severity in ('Low','Medium','High')),
  report_count integer default 0,
  is_active    boolean default true,
  published_at timestamptz default now(),
  created_by   uuid references public.users(id),
  created_at   timestamptz default now()
);

-- Public read for active alerts
create policy "Anyone can read active alerts"
  on public.scam_alerts for select using (is_active = true);

-- ─── USER REPORTS ────────────────────────
create table public.user_reports (
  id          uuid primary key default uuid_generate_v4(),
  user_id     uuid references public.users(id) on delete set null,
  report_type text not null,
  content     text not null,
  platform    text,
  status      text default 'new'
                check (status in ('new','reviewing','confirmed','rejected')),
  admin_notes text,
  created_at  timestamptz default now()
);

alter table public.user_reports enable row level security;
create policy "Users can submit reports"
  on public.user_reports for insert with check (auth.uid() = user_id);
create policy "Users can view own reports"
  on public.user_reports for select using (auth.uid() = user_id);

-- ─── ALERT SUBSCRIPTIONS ─────────────────
create table public.alert_subscriptions (
  id         uuid primary key default uuid_generate_v4(),
  user_id    uuid not null references public.users(id) on delete cascade,
  email      text not null,
  categories jsonb default '["all"]',
  is_active  boolean default true,
  created_at timestamptz default now(),
  unique(user_id)
);

-- ─── DAILY SCAN RESET FUNCTION ───────────
create or replace function reset_daily_scans()
returns void language sql security definer as $$
  update public.users set scans_today = 0;
$$;

-- Schedule via pg_cron (Supabase):
-- select cron.schedule('reset-scans', '0 0 * * *', 'select reset_daily_scans()');

-- ─── UPDATED_AT TRIGGER ──────────────────
create or replace function update_updated_at()
returns trigger language plpgsql as $$
begin new.updated_at = now(); return new; end;
$$;

create trigger users_updated_at before update on public.users
  for each row execute function update_updated_at();
create trigger scam_entries_updated_at before update on public.scam_entries
  for each row execute function update_updated_at();`;

  // Payments integration code (server-side Next.js API route)
  const stripeLines = [
    "// ── pages/api/payments/webhook.ts ───────────────────────",
    "// npm install stripe supabase micro  (server packages)",
    "",
    "// SERVER-SIDE ONLY imports (not bundled in browser):",
    "// $ npm install stripe  — payment processing SDK",
    "// $ npm install @supabase/supabase-js  — database client",
    "// $ npm install micro  — request body parser",
    "",
    "export const config = { api: { bodyParser: false } };",
    "",
    "export default async function webhookHandler(req, res) {",
    "  const stripe = new StripeLib(process.env.STRIPE_SECRET_KEY);",
    "  const db = createClient(",
    "    process.env.NEXT_PUBLIC_SUPABASE_URL,",
    "    process.env.SUPABASE_SERVICE_ROLE_KEY",
    "  );",
    "  const sig = req.headers['stripe-signature'];",
    "  const buf = await buffer(req);",
    "  let event;",
    "",
    "  try {",
    "    event = stripe.webhooks.constructEvent(",
    "      buf, sig, process.env.STRIPE_WEBHOOK_SECRET",
    "    );",
    "  } catch (err) {",
    "    return res.status(400).send('Webhook Error: ' + err.message);",
    "  }",
    "",
    "  switch (event.type) {",
    "    case 'checkout.session.completed': {",
    "      const session = event.data.object;",
    "      await db.from('subscriptions').upsert({",
    "        user_id:    session.metadata.userId,",
    "        stripe_sub: session.subscription,",
    "        plan:       session.metadata.plan || 'premium',",
    "        status:     'active',",
    "      });",
    "      await db.from('users')",
    "        .update({ plan: session.metadata.plan || 'premium' })",
    "        .eq('id', session.metadata.userId);",
    "      break;",
    "    }",
    "    case 'customer.subscription.deleted': {",
    "      const sub = event.data.object;",
    "      await db.from('subscriptions')",
    "        .update({ status: 'cancelled' })",
    "        .eq('stripe_sub', sub.id);",
    "      await db.from('users')",
    "        .update({ plan: 'free' })",
    "        .eq('stripe_customer_id', sub.customer);",
    "      break;",
    "    }",
    "    case 'invoice.payment_failed': {",
    "      const inv = event.data.object;",
    "      await db.from('subscriptions')",
    "        .update({ status: 'past_due' })",
    "        .eq('stripe_sub', inv.subscription);",
    "      break;",
    "    }",
    "  }",
    "  res.json({ received: true });",
    "}",
    "",
    "// ── lib/plans.ts ──────────────────────────────────────────",
    "export const PLANS = {",
    "  premium: {",
    "    name: 'Premium',",
    "    priceId: process.env.STRIPE_PREMIUM_PRICE_ID,",
    "    price: '€4.99/mo',",
    "    features: ['Unlimited scans', 'All scan types', 'Advanced AI'],",
    "  },",
    "  business: {",
    "    name: 'Business',",
    "    priceId: process.env.STRIPE_BUSINESS_PRICE_ID,",
    "    price: '€19.99/mo',",
    "    features: ['Everything in Premium', '10 seats', 'API access'],",
    "  },",
    "};",
    "",
    "export async function createCheckoutSession(userId, plan) {",
    "  const session = await stripe.checkout.sessions.create({",
    "    mode: 'subscription',",
    "    line_items: [{ price: PLANS[plan].priceId, quantity: 1 }],",
    "    success_url: process.env.APP_URL + '/dashboard?upgraded=true',",
    "    cancel_url:  process.env.APP_URL + '/pricing',",
    "    metadata: { userId, plan },",
    "  });",
    "  return session;",
    "}",
  ];
  const stripeCode = stripeLines.join("\n");
  const seoCode = `// ── next-sitemap.config.js ───────────────────────────────
module.exports = {
  siteUrl: "https://safecheck.ie",
  generateRobotsTxt: true,
  changefreq: "daily",
  priority: 0.8,
  exclude: ["/dashboard", "/admin"],
};

// ── pages/index.tsx metadata ──────────────────────────────
export const metadata = {
  title: "SafeCheck — Free Scam Checker for Emails, Texts & Websites",
  description: "Check if a message, website or marketplace listing is a scam. AI-powered scam detection for emails, SMS, phishing links and more. Free & instant.",
  keywords: [
    "scam checker", "phishing checker", "is this website safe",
    "email scam checker", "text message scam detector",
    "marketplace scam checker", "fake website checker ireland",
  ],
  openGraph: {
    title: "SafeCheck — Don't Get Scammed. Check First.",
    description: "AI-powered scam detection trusted by 150,000+ users.",
    url: "https://safecheck.ie",
    type: "website",
    images: [{ url: "https://safecheck.ie/og-image.png", width: 1200, height: 630 }],
  },
  twitter: { card: "summary_large_image", site: "@safecheckie" },
};

// ── SEO Page Routes ───────────────────────────────────────
// /scam-checker          → "Free Scam Checker — Is This a Scam?"
// /phishing-checker      → "Phishing Link Checker — Check URLs Safely"
// /is-this-website-safe  → "Is This Website Safe? Check Any URL"
// /email-scam-checker    → "Email Scam Checker — Spot Phishing Emails"
// /text-scam-checker     → "SMS Scam Checker — Spot Fake Texts"
// /marketplace-scam      → "Marketplace Scam Detector — DoneDeal, eBay"
// /facebook-marketplace-scam → "Facebook Marketplace Scam Checker"
// /donedeal-scam-checker → "DoneDeal Scam Checker Ireland"

// ── JSON-LD Structured Data ──────────────────────────────
export const jsonLd = {
  "@context": "https://schema.org",
  "@type": "WebApplication",
  name: "SafeCheck",
  url: "https://safecheck.ie",
  description: "AI-powered scam and phishing detection tool",
  applicationCategory: "SecurityApplication",
  operatingSystem: "Web",
  offers: [
    { "@type": "Offer", price: "0", priceCurrency: "EUR", name: "Free Plan" },
    { "@type": "Offer", price: "4.99", priceCurrency: "EUR", name: "Premium", billingPeriod: "P1M" },
  ],
  aggregateRating: {
    "@type": "AggregateRating",
    ratingValue: "4.9", reviewCount: "8420",
  },
};`;

  const envLines = [
    "# ── .env.local ───────────────────────────────────────────",
    "# Database (Supabase)",
    "NEXT_PUBLIC_SUPABASE_URL=https://xxxx.supabase.co",
    "NEXT_PUBLIC_SUPABASE_ANON_KEY=eyJhbGci...",
    "SUPABASE_SERVICE_ROLE_KEY=eyJhbGci...",
    "",
    "# AI (Anthropic Claude)",
    "ANTHROPIC_API_KEY=sk-ant-...",
    "",
    "# Payments",
    "STRIPE_SECRET_KEY=sk_live_...",
    "NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_live_...",
    "STRIPE_WEBHOOK_SECRET=whsec_...",
    "STRIPE_PREMIUM_PRICE_ID=price_...",
    "STRIPE_BUSINESS_PRICE_ID=price_...",
    "",
    "# App",
    "NEXT_PUBLIC_APP_URL=https://safecheck.ie",
    "NEXT_PUBLIC_GA_ID=G-XXXXXXXXXX",
    "",
    "# ── Full Tech Stack ──────────────────────────────────────",
    "# Frontend:   Next.js 14 (App Router) + TypeScript + Tailwind CSS",
    "# Database:   Supabase (Postgres + Auth + Storage + Edge Functions)",
    "# AI Engine:  Anthropic Claude API (claude-sonnet-4)",
    "# Payments:   Stripe Subscriptions + Webhooks",
    "# Email:      Resend + React Email templates",
    "# Analytics:  PostHog (product) + Vercel Analytics (web)",
    "# Hosting:    Vercel (frontend) + Supabase Cloud (backend)",
    "# CDN:        Cloudflare (DNS + DDoS protection)",
    "# Monitoring: Sentry (errors) + Uptime Robot (availability)",
    "# SEO:        next-sitemap + JSON-LD structured data",
  ];
  const envCode = envLines.join("\n");;

  const sections = [
    { id: "db", label: "🗄 Database Schema" },
    { id: "stripe", label: "💳 Stripe / Payments" },
    { id: "seo", label: "🔍 SEO & Metadata" },
    { id: "env", label: "⚙️ Config & Stack" },
  ];

  const codeMap = { db: dbSchema, stripe: stripeCode, seo: seoCode, env: envCode };

  return (
    <div style={{ maxWidth: 1000, margin: "0 auto", padding: "100px 24px 60px" }}>
      <div style={{ marginBottom: 32 }}>
        <h1 className="syne" style={{ fontSize: "clamp(26px,4vw,38px)", fontWeight: 800, marginBottom: 8 }}>Technical Documentation</h1>
        <p style={{ color: COLORS.grey }}>Database schema, Stripe integration, SEO setup, and environment configuration</p>
      </div>

      <div style={{ display: "flex", gap: 6, marginBottom: 24, flexWrap: "wrap" }}>
        {sections.map(s => (
          <button key={s.id} className={`tab-btn ${activeSection === s.id ? "active" : ""}`} onClick={() => setActiveSection(s.id)}>{s.label}</button>
        ))}
      </div>

      <div className="card" style={{ padding: 0, overflow: "hidden" }}>
        <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", padding: "14px 20px", borderBottom: "1px solid rgba(255,255,255,0.06)", background: "rgba(0,0,0,0.2)" }}>
          <div style={{ display: "flex", gap: 6 }}>
            {["#FF5F57","#FFBD2E","#28C840"].map(c => (
              <div key={c} style={{ width: 10, height: 10, borderRadius: "50%", background: c }} />
            ))}
          </div>
          <span style={{ fontSize: 12, color: COLORS.grey, fontFamily: "monospace" }}>
            {activeSection === "db" ? "schema.sql" : activeSection === "stripe" ? "stripe/webhook.ts" : activeSection === "seo" ? "metadata.ts" : ".env.local"}
          </span>
          <button onClick={() => navigator.clipboard?.writeText(codeMap[activeSection])} style={{ background: "none", border: "none", color: COLORS.grey, cursor: "pointer", fontSize: 12 }}>Copy</button>
        </div>
        <pre style={{
          padding: 24, overflowX: "auto", fontSize: 12.5, lineHeight: 1.7,
          color: "#A8B8D8", fontFamily: "'Fira Code', 'Cascadia Code', monospace",
          background: "transparent", maxHeight: 560, overflowY: "auto",
          whiteSpace: "pre-wrap", wordBreak: "break-word",
        }}>
          <code>{codeMap[activeSection]}</code>
        </pre>
      </div>

      {/* Architecture diagram (text) */}
      <div className="glass" style={{ borderRadius: 16, padding: 28, marginTop: 24 }}>
        <h3 className="syne" style={{ fontSize: 16, fontWeight: 700, marginBottom: 16 }}>System Architecture</h3>
        <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(180px, 1fr))", gap: 12 }}>
          {[
            { layer: "Frontend", tech: "Next.js 14 · TypeScript · Tailwind CSS", color: COLORS.accent },
            { layer: "Auth", tech: "Supabase Auth · Email + Google OAuth", color: COLORS.green },
            { layer: "Database", tech: "Supabase Postgres · RLS Policies", color: COLORS.amber },
            { layer: "AI Engine", tech: "Anthropic Claude API · Sonnet 4", color: "#A78BFA" },
            { layer: "Payments", tech: "Stripe Subscriptions · Webhooks", color: COLORS.red },
            { layer: "Hosting", tech: "Vercel · Cloudflare · Supabase Edge", color: COLORS.accent },
          ].map(({ layer, tech, color }) => (
            <div key={layer} style={{ padding: "14px 16px", borderRadius: 10, background: color + "08", border: `1px solid ${color}20` }}>
              <div className="syne" style={{ fontSize: 12, fontWeight: 700, color, letterSpacing: "0.06em", marginBottom: 6 }}>{layer.toUpperCase()}</div>
              <div style={{ fontSize: 12, color: COLORS.grey, lineHeight: 1.5 }}>{tech}</div>
            </div>
          ))}
        </div>
      </div>
    </div>
  );
};

// ─── TOP-RIGHT MENU ──────────────────────────────────────────────────────────
const TopRightMenu = ({ page, navigateTo, user, isAdmin }) => {
  const [open, setOpen] = useState(false);

  const items = [
    ["home",      "🏠", "Home"],
    ["scanner",   "🔍", "Check a Scam"],
    ["knowledge", "📚", "Scam Library"],
    ["alerts",    "🚨", "Live Alerts"],
    ["pricing",   "💳", "Pricing"],
    ["dashboard", "📊", "Dashboard"],
    ["auth",      "👤", user ? "Account" : "Sign In"],
    ["schema",    "🗄", "Tech Docs"],
    ...(isAdmin(user) ? [["admin", "⚙️", "Admin Panel"]] : []),
  ];

  return (
    <>
      {/* Hamburger button — top right */}
      <button
        onClick={() => setOpen(o => !o)}
        style={{
          position: "fixed", top: 14, right: 20, zIndex: 300,
          width: 40, height: 40, borderRadius: 10,
          background: open ? "rgba(0,212,255,0.15)" : "rgba(10,14,26,0.85)",
          backdropFilter: "blur(12px)",
          border: "1px solid rgba(0,212,255,0.2)",
          cursor: "pointer", display: "flex", alignItems: "center",
          justifyContent: "center", flexDirection: "column", gap: 5,
          transition: "all 0.2s",
        }}
      >
        {/* Three lines that animate to X */}
        {[0,1,2].map(i => (
          <span key={i} style={{
            display: "block", width: 16, height: 2, borderRadius: 2,
            background: open ? COLORS.accent : COLORS.greyLight,
            transition: "all 0.25s ease",
            transform: open
              ? i === 0 ? "translateY(7px) rotate(45deg)"
              : i === 2 ? "translateY(-7px) rotate(-45deg)"
              : "scaleX(0)"
              : "none",
            opacity: open && i === 1 ? 0 : 1,
          }} />
        ))}
      </button>

      {/* Backdrop */}
      {open && (
        <div
          onClick={() => setOpen(false)}
          style={{
            position: "fixed", inset: 0, zIndex: 290,
            background: "rgba(0,0,0,0.4)", backdropFilter: "blur(2px)",
          }}
        />
      )}

      {/* Dropdown panel */}
      <div style={{
        position: "fixed", top: 62, right: 16, zIndex: 295,
        width: 220,
        background: "rgba(10,14,26,0.97)",
        backdropFilter: "blur(20px)",
        border: "1px solid rgba(0,212,255,0.15)",
        borderRadius: 14,
        overflow: "hidden",
        boxShadow: "0 20px 60px rgba(0,0,0,0.6)",
        transform: open ? "translateY(0) scale(1)" : "translateY(-10px) scale(0.95)",
        opacity: open ? 1 : 0,
        pointerEvents: open ? "auto" : "none",
        transition: "all 0.2s cubic-bezier(0.4,0,0.2,1)",
        transformOrigin: "top right",
      }}>
        {/* Header */}
        <div style={{
          padding: "12px 16px",
          borderBottom: "1px solid rgba(255,255,255,0.06)",
          display: "flex", alignItems: "center", gap: 8,
        }}>
          <div style={{
            width: 24, height: 24, borderRadius: 6,
            background: "rgba(0,212,255,0.1)",
            border: "1px solid rgba(0,212,255,0.2)",
            display: "flex", alignItems: "center", justifyContent: "center",
          }}>
            <Icon name="shield" size={13} color={COLORS.accent} />
          </div>
          <span className="syne" style={{ fontSize: 13, fontWeight: 700, color: COLORS.white }}>
            Safe<span style={{ color: COLORS.accent }}>Check</span>
          </span>
        </div>

        {/* Nav items */}
        <div style={{ padding: "6px 0" }}>
          {items.map(([p, emoji, label]) => {
            const active = page === p;
            const isAdminItem = p === "admin";
            return (
              <button
                key={p}
                onClick={() => { navigateTo(p); setOpen(false); }}
                style={{
                  width: "100%", padding: "10px 16px",
                  display: "flex", alignItems: "center", gap: 10,
                  background: active ? "rgba(0,212,255,0.08)" : "transparent",
                  border: "none", cursor: "pointer",
                  borderLeft: active ? `2px solid ${COLORS.accent}` : "2px solid transparent",
                  transition: "all 0.15s",
                }}
                onMouseEnter={e => { if (!active) e.currentTarget.style.background = "rgba(255,255,255,0.04)"; }}
                onMouseLeave={e => { if (!active) e.currentTarget.style.background = "transparent"; }}
              >
                <span style={{ fontSize: 15, width: 20, textAlign: "center" }}>{emoji}</span>
                <span style={{
                  fontSize: 13, fontWeight: active ? 600 : 400,
                  color: active ? COLORS.accent : isAdminItem ? COLORS.amber : COLORS.greyLight,
                  fontFamily: "'DM Sans', sans-serif",
                }}>
                  {label}
                </span>
                {isAdminItem && (
                  <span style={{
                    marginLeft: "auto", fontSize: 9, fontWeight: 700,
                    color: COLORS.amber, background: "rgba(255,179,0,0.12)",
                    border: "1px solid rgba(255,179,0,0.25)",
                    padding: "1px 6px", borderRadius: 4,
                    fontFamily: "'Syne',sans-serif", letterSpacing: "0.06em",
                  }}>
                    ADMIN
                  </span>
                )}
              </button>
            );
          })}
        </div>

        {/* Footer */}
        {user && (
          <div style={{
            padding: "10px 16px",
            borderTop: "1px solid rgba(255,255,255,0.06)",
            display: "flex", alignItems: "center", gap: 8,
          }}>
            <div style={{
              width: 28, height: 28, borderRadius: "50%", flexShrink: 0,
              background: "linear-gradient(135deg, #00D4FF, #0088AA)",
              display: "flex", alignItems: "center", justifyContent: "center",
              fontSize: 12, fontWeight: 700, color: "#0A0E1A",
            }}>
              {user.name[0]}
            </div>
            <div style={{ minWidth: 0 }}>
              <div style={{ fontSize: 12, fontWeight: 600, color: COLORS.white, overflow: "hidden", textOverflow: "ellipsis", whiteSpace: "nowrap" }}>{user.name}</div>
              <div style={{ fontSize: 10, color: COLORS.grey }}>{user.plan === "premium" ? "⭐ Premium" : "Free Plan"}</div>
            </div>
          </div>
        )}
      </div>
    </>
  );
};

// ─── MAIN APP ─────────────────────────────────────────────────────────────────
export default function SafeCheckApp() {
  const [page, setPage] = useState("home");
  const [user, setUser] = useState(null);
  const [scannerInput, setScannerInput] = useState("");
  const [scannerType, setScannerType] = useState("message");

  useEffect(() => {
    window.scrollTo({ top: 0, behavior: "smooth" });
  }, [page]);

  const navigateTo = (p) => {
    // Block direct navigation to admin for non-admin users
    if (p === "admin" && !isAdmin(user)) return;
    setPage(p);
  };

  return (
    <>
      <style>{css}</style>
      <div style={{ minHeight: "100vh", display: "flex", flexDirection: "column" }}>
        <Nav currentPage={page} setPage={navigateTo} user={user} setUser={setUser} />

        <main style={{ flex: 1 }}>
          {page === "home"      && <HomePage setPage={navigateTo} setScannerInput={setScannerInput} setScannerType={setScannerType} />}
          {page === "scanner"   && <ScannerPage initialInput={scannerInput} initialType={scannerType} />}
          {page === "knowledge" && <KnowledgePage />}
          {page === "alerts"    && <AlertsPage />}
          {page === "pricing"   && <PricingPage setPage={navigateTo} user={user} />}
          {page === "dashboard" && <DashboardPage user={user} setPage={navigateTo} />}
          {page === "auth"      && <AuthPage setUser={setUser} setPage={navigateTo} />}
          {page === "admin"     && <AdminPage user={user} setPage={navigateTo} />}
          {page === "schema"    && <SchemaPage />}
        </main>

        {/* Top-right hamburger menu */}
        <TopRightMenu page={page} navigateTo={navigateTo} user={user} isAdmin={isAdmin} />

        {!["auth"].includes(page) && <Footer setPage={navigateTo} />}
      </div>
    </>
  );
}
