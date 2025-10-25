# APRealestate-Landing-Page

import { motion } from "framer-motion";
import { Button } from "@/components/ui/button";
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { Checkbox } from "@/components/ui/checkbox";
import { ArrowRight, Mail } from "lucide-react";

// AP Real Estate – Minimal White & Elegant Website
// Elegant, white background, minimal cards replaced with typographic layout, serif headings

export default function APRealEstateLanding() {
  return (
    <div className="min-h-screen bg-white text-black">
      {/* Top Navigation */}
      <header className="sticky top-0 z-50 border-b border-black/10 bg-white/90 backdrop-blur">
        <nav className="mx-auto flex max-w-6xl items-center justify-between px-4 py-4">
          <a href="#" className="font-serif text-xl tracking-tight">AP Real Estate</a>
          <ul className="hidden gap-10 md:flex font-light">
            <li><a href="#leistungen" className="text-sm hover:opacity-70">Leistungen</a></li>
            <li><a href="#kunden" className="text-sm hover:opacity-70">Kunden</a></li>
            <li><a href="#referenzen" className="text-sm hover:opacity-70">Referenzen</a></li>
            <li><a href="#kontakt" className="text-sm hover:opacity-70">Kontakt</a></li>
          </ul>
          <Button variant="outline" className="border-black text-black hover:bg-black hover:text-white">
            <Mail className="mr-2 h-4 w-4" />
            Anfragen
          </Button>
        </nav>
      </header>

      {/* Hero */}
      <section className="relative mx-auto max-w-5xl px-6 py-32 text-center">
        <motion.div initial={{ opacity: 0, y: 10 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.7 }}>
          <h1 className="font-serif text-5xl md:text-6xl leading-tight tracking-tight">
            Qualifizierte Verkäufer-Leads <br />
            <span className="text-black/50">für Immobilienprofis</span>
          </h1>
          <p className="mt-8 text-lg text-black/70 max-w-2xl mx-auto font-light">
            AP Real Estate generiert planbar Verkäuferkontakte für Vermittlungsräte, Investmentgesellschaften,
            Family Offices und Immobilienhäuser. Diskret. Effizient. Datengetrieben.
          </p>
          <div className="mt-12 flex flex-wrap justify-center gap-4">
            <a href="tel:017662216512">
              <Button className="bg-black text-white hover:bg-black/90">
                Jetzt Gespräch sichern
                <ArrowRight className="ml-2 h-4 w-4" />
              </Button>
            </a>
            <Button variant="outline" className="border-black text-black hover:bg-black hover:text-white">
              Leistungsübersicht
            </Button>
          </div>
        </motion.div>
      </section>

      {/* Leistungen */}
      <section id="leistungen" className="border-t border-black/10 bg-white">
        <div className="mx-auto max-w-4xl px-6 py-24 text-center">
          <h2 className="font-serif text-3xl mb-6">Unsere Leistungen</h2>
          <p className="text-black/70 leading-relaxed max-w-3xl mx-auto font-light">
            Wir übernehmen die komplette Lead-Generierung für Sie – von der Identifikation bis zur qualifizierten
            Übergabe. Unser datenbasierter Ansatz sorgt für planbare Verkäuferkontakte und messbare Ergebnisse.
          </p>
        </div>
      </section>

      {/* Kunden */}
      <section id="kunden" className="border-t border-black/10 bg-white">
        <div className="mx-auto max-w-4xl px-6 py-24 text-center">
          <h2 className="font-serif text-3xl mb-6">Unsere Kunden</h2>
          <p className="text-black/70 leading-relaxed max-w-3xl mx-auto font-light">
            Wir sourcen ab 20 Mio. Volumen und arbeiten für Vermittlungsräte, Maklerhäuser, Investmentgesellschaften, Family Offices und
            Immobilienhäuser, die ihren Verkäufer-Funnel strukturiert und diskret erweitern möchten.
          </p>
        </div>
      </section>

      {/* Referenzen */}
      <section id="referenzen" className="border-t border-black/10 bg-white">
        <div className="mx-auto max-w-4xl px-6 py-24 text-center">
          <h2 className="font-serif text-3xl mb-10">Ergebnisse, die zählen</h2>
          <div className="space-y-6 text-black/80 font-light">
            <p>+140 qualifizierte Kontakte pro Quartal</p>
            <p>{">35% Terminrate"}</p>
            <p>{"100% DSGVO-konform"}</p>
          </div>
        </div>
      </section>

      {/* Kontakt */}
      <section id="kontakt" className="border-t border-black/10 bg-white">
        <div className="mx-auto max-w-5xl px-6 py-24 grid md:grid-cols-2 gap-12 items-start">
          <div>
            <h2 className="font-serif text-3xl mb-4">Kontakt aufnehmen</h2>
            <p className="text-black/70 mb-6 font-light">
              Erzählen Sie uns kurz von Ihren Zielen – wir melden uns innerhalb von 24 Stunden.
            </p>
            <p className="text-black/70 text-sm leading-relaxed">
              AP Real Estate<br />Berlin · DACH & EU<br />
              <span className="flex items-center gap-2 mt-2"><Mail className="h-4 w-4" /> kontakt@aprealestate.eu</span>
            </p>
          </div>
          <div>
            <form className="space-y-4">
              <Input placeholder="Ihr Name" className="bg-transparent text-black placeholder:text-black/40 focus-visible:ring-black" />
              <Input type="email" placeholder="Ihre E-Mail" className="bg-transparent text-black placeholder:text-black/40 focus-visible:ring-black" />
              <Textarea placeholder="Ihre Nachricht" className="min-h-[140px] bg-transparent text-black placeholder:text-black/40 focus-visible:ring-black" />
              <div className="flex items-start gap-3 text-sm">
                <Checkbox id="gdpr" className="border-black data-[state=checked]:bg-black" />
                <label htmlFor="gdpr" className="leading-tight text-black/80 font-light">
                  Ich stimme der Verarbeitung meiner Daten gemäß Datenschutzhinweisen zu.
                </label>
              </div>
              <Button className="w-full bg-black text-white hover:bg-black/90">Nachricht senden</Button>
            </form>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="border-t border-black/10 bg-white">
        <div className="mx-auto flex max-w-5xl flex-col items-center justify-between gap-4 px-6 py-8 md:flex-row text-sm text-black/60">
          <p>© {new Date().getFullYear()} AP Real Estate. Alle Rechte vorbehalten.</p>
          <div className="flex items-center gap-6">
            <a href="#">Impressum</a>
            <a href="#">Datenschutz</a>
          </div>
        </div>
      </footer>
    </div>
  );
}
