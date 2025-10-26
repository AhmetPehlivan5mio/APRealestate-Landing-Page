import React, { useState } from "react";

const primary = "#144a89";
const primaryLight = "#1d5fb0";

export default function APRealestateSite() {
  const [sent, setSent] = useState(false);
  const handleSubmit = (e) => {
    e.preventDefault();
    setSent(true);
    setTimeout(() => setSent(false), 3500);
  };

  const nav = [
    { label: "Leistungen", href: "#leistungen" },
    { label: "Vorgehen", href: "#prozess" },
    { label: "Über uns", href: "#about" },
    { label: "Kontakt", href: "#kontakt" },
  ];

  return (
    <div className="min-h-screen bg-white text-slate-900 antialiased">
      {/* Header - weißer Hintergrund, blauer Trennstrich unten */}
      <header
        className="sticky top-0 z-30 backdrop-blur border-b shadow-sm"
        style={{ background: "white", borderColor: primary }}
      >
        <div className="max-w-[960px] mx-auto px-5 py-3 flex items-center justify-between">
          <a
            href="#top"
            className="tracking-tight font-medium text-[18px]"
            style={{ color: primary }}
          >
            APRealestate
          </a>
          <nav className="hidden md:flex items-center gap-6">
            {nav.map((n) => (
              <a
                key={n.href}
                href={n.href}
                className="text-[13px] uppercase tracking-[0.12em] font-medium transition-colors"
                style={{ color: primary }}
              >
                {n.label}
              </a>
            ))}
            <a
              href="#kontakt"
              className="text-[12px] uppercase tracking-[0.12em] text-white px-3 py-1.5 shadow-sm hover:shadow-md transition rounded-none"
              style={{ background: primary }}
            >
              Kontakt
            </a>
          </nav>
          <a
            href="#kontakt"
            className="md:hidden text-[12px] uppercase tracking-[0.12em] text-white px-3 py-1.5 shadow-sm rounded-none"
            style={{ background: primary }}
          >
            Kontakt
          </a>
        </div>
      </header>

      {/* Hero */}
      <section id="top">
        <div className="max-w-[960px] mx-auto px-5 py-24 md:py-32">
          <p className="text-[12px] uppercase tracking-[0.18em] text-slate-500">
            Exklusive Kontakte. Außergewöhnliche Immobilien.
          </p>
          <h1
            className="mt-4 text-[38px] md:text-[54px] font-light leading-[1.08] tracking-tight"
            style={{ color: primary }}
          >
            Premium-Akquise für anspruchsvolle Immobilienmakler.<br className="hidden md:block" />
            Verkäuferkontakte auf höchstem Niveau.
          </h1>
          <p className="mt-5 max-w-[52ch] text-slate-600 text-[17px]">
            Wir verbinden exklusive Immobilienbesitzer mit ausgewählten Maklern –
            diskret, effizient und erfolgsorientiert.
          </p>
          <div className="mt-10 flex flex-col sm:flex-row gap-3">
            <a
              href="#kontakt"
              className="inline-flex items-center gap-2 text-[13px] font-medium text-white px-5 py-2.5 shadow-sm hover:shadow-md transition rounded-none"
              style={{ background: primary }}
            >
              Exklusiv anfragen →
            </a>
            <a
              href="#leistungen"
              className="inline-flex items-center gap-2 text-[13px] font-medium border border-slate-300 px-5 py-2.5 hover:bg-slate-50 transition rounded-none"
              style={{ color: primary }}
            >
              Unsere Leistungen →
            </a>
          </div>
        </div>
      </section>

      {/* Kontakt mit Carousel */}
      <section id="kontakt">
        <div className="max-w-[720px] mx-auto px-5 py-18 md:py-24">
          <p className="text-[12px] uppercase tracking-[0.18em]" style={{ color: primary }}>Kontakt</p>
          <h4 className="mt-3 text-[26px] font-light tracking-tight" style={{ color: primary }}>Sprechen wir persönlich</h4>
          <form onSubmit={handleSubmit} className="mt-6">
            <div className="grid md:grid-cols-2 gap-5">
              <label className="text-sm">
                Name
                <input className="mt-1 w-full border border-slate-300 px-3 py-2 rounded-none" placeholder="Max Mustermann" required />
              </label>
              <label className="text-sm">
                E-Mail
                <input type="email" className="mt-1 w-full border border-slate-300 px-3 py-2 rounded-none" placeholder="max@firma.de" required />
              </label>
            </div>
            <div className="grid md:grid-cols-2 gap-5 mt-4">
              <label className="text-sm">
                Telefon
                <input className="mt-1 w-full border border-slate-300 px-3 py-2 rounded-none" placeholder="+49…" />
              </label>
              <label className="text-sm">
                Region / Gebiet
                <input className="mt-1 w-full border border-slate-300 px-3 py-2 rounded-none" placeholder="z. B. Köln, Düsseldorf" />
              </label>
            </div>
            <label className="text-sm block mt-4">
              Nachricht
              <textarea rows={4} className="mt-1 w-full border border-slate-300 px-3 py-2 rounded-none" placeholder="Ihr Anliegen…" />
            </label>
            <label className="flex items-start gap-2 text-sm text-slate-600 mt-4">
              <input type="checkbox" required className="mt-1" />
              <span>Ich akzeptiere die Datenschutzhinweise.</span>
            </label>
            <button type="submit" className="mt-6 inline-flex items-center gap-2 px-5 py-2.5 text-white text-[13px] shadow-sm hover:shadow-md transition rounded-none" style={{ background: primaryLight }}>Nachricht senden →</button>
            {sent && <div className="mt-2 text-sm text-green-600">Danke! Wir melden uns zeitnah.</div>}
          </form>
        </div>

        {/* Standorte – Carousel */}
        <div className="border-t" style={{ borderColor: primary }} />
        <div className="max-w-[960px] mx-auto px-5 pb-14 pt-10">
          <p className="text-[12px] uppercase tracking-[0.18em]" style={{ color: primary }}>Standorte</p>
          <h5 className="mt-2 text-[22px] font-light tracking-tight" style={{ color: primary }}>Berlin · Düsseldorf · Bielefeld</h5>
          <div className="mt-6 overflow-x-auto snap-x snap-mandatory">
            <div className="flex gap-4 min-w-full pr-4">
              {[{ city: "Berlin", email: "berlin@aprealestate.eu" }, { city: "Düsseldorf", email: "dus@aprealestate.eu" }, { city: "Bielefeld", email: "bielefeld@aprealestate.eu" }].map((loc) => (
                <div key={loc.city} className="snap-start shrink-0 w-[280px] md:w-[320px] border" style={{ borderColor: primary }}>
                  <div className="px-4 py-3 text-white" style={{ background: primary }}>
                    <div className="uppercase text-[12px] tracking-[0.18em]">{loc.city}</div>
                  </div>
                  <div className="px-4 py-4 bg-white">
                    <div className="text-sm text-slate-600">E-Mail</div>
                    <a href={`mailto:${loc.email}`} className="block text-[15px] underline" style={{ color: primary }}>{loc.email}</a>
                    <div className="mt-3 text-sm text-slate-600">Telefon</div>
                    <div className="text-[15px] text-slate-800">0176 62216512</div>
                  </div>
                </div>
              ))}
            </div>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer style={{ background: primary }}>
        <div className="max-w-[960px] mx-auto px-5 py-10 flex flex-col md:flex-row items-start md:items-center justify-between gap-4 text-sm text-white">
          <div>© {new Date().getFullYear()} APRealestate</div>
          <div className="flex gap-6">
            <a href="#" className="hover:underline text-white">Impressum</a>
            <a href="#" className="hover:underline text-white">Datenschutz</a>
            <a href="#" className="hover:underline text-white">AGB</a>
          </div>
        </div>
      </footer>
    </div>
  );
}
