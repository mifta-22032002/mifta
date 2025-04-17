import React, { useState } from "react";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { Phone, CheckCircle, Send, MessageSquare } from "lucide-react";
import { motion } from "framer-motion";

const services = [
  "Jasa Ketik Tugas",
  "Jasa Ketik Surat",
  "Jasa Cari Jurnal",
  "Jasa Review Jurnal",
  "Jasa Buat PPT",
  "Jasa Resume",
  "Jasa Lain-Lain"
];

const categories = [
  "Akademik",
  "Administrasi",
  "Desain Presentasi",
  "Riset dan Referensi"
];

const testimonials = [
  {
    quote: "Pelayanannya cepat dan hasilnya rapi banget. Sangat membantu tugas kuliah saya!",
    author: "– Mhs. A"
  },
  {
    quote: "Harga murah, kualitas mantap. PPT saya jadi menarik dan profesional.",
    author: "– Kryw. B"
  },
  {
    quote: "Langsung dibantu cari jurnal dan review-nya juga detail. Rekomen!",
    author: "– Pnl. C"
  }
];

export default function OpenJasaPage() {
  const [form, setForm] = useState({ name: "", service: "", message: "" });

  const handleChange = (e) => {
    setForm({ ...form, [e.target.name]: e.target.value });
  };

  const generateWhatsAppLink = () => {
    const base = "https://wa.me/6287756856942";
    const text = `Halo, saya ${form.name}. Saya ingin memesan: ${form.service}. Catatan tambahan: ${form.message}`;
    return `${base}?text=${encodeURIComponent(text)}`;
  };

  return (
    <div className="min-h-screen bg-cover bg-center bg-no-repeat p-6 font-sans" style={{ backgroundImage: "url('https://images.unsplash.com/photo-1532614338840-ab30cf10ed36?auto=format&fit=crop&w=1400&q=80')" }}>
      <div className="backdrop-blur-sm bg-white/80 max-w-5xl mx-auto text-center py-10 px-6 rounded-2xl shadow-xl">
        <motion.h1 initial={{ opacity: 0, y: -20 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.6 }} className="text-5xl font-extrabold text-gray-800 mb-2">
          OPEN JASA!
        </motion.h1>
        <h2 className="text-lg text-gray-600 tracking-wide mb-8">Mulai 10 Ribu, Urusan Beres</h2>

        <div className="rounded-xl overflow-hidden shadow-lg mb-10">
          <img src="https://images.unsplash.com/photo-1603791440384-56cd371ee9a7?auto=format&fit=crop&w=1400&q=80" alt="Slider" className="w-full h-64 object-cover" />
        </div>

        <h3 className="text-2xl font-semibold text-gray-700 mb-4">Kategori Layanan:</h3>
        <div className="flex flex-wrap justify-center gap-3 mb-6">
          {categories.map((cat, idx) => (
            <span key={idx} className="bg-blue-100 text-blue-700 px-4 py-2 rounded-full text-sm font-medium shadow">
              {cat}
            </span>
          ))}
        </div>

        <h3 className="text-2xl font-semibold text-gray-700 mb-4">Open Positions:</h3>
        <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4 mb-10">
          {services.map((service, idx) => (
            <Card key={idx} className="bg-white shadow p-4">
              <CardContent className="flex items-center gap-3">
                <CheckCircle className="text-green-500" />
                <span>{service}</span>
              </CardContent>
            </Card>
          ))}
        </div>

        <h3 className="text-2xl font-semibold text-gray-700 mb-4">Form Order Otomatis:</h3>
        <div className="max-w-xl mx-auto mb-10 text-left space-y-4">
          <input type="text" name="name" value={form.name} onChange={handleChange} placeholder="Nama Anda" required className="w-full border rounded p-3" />
          <input type="text" name="service" value={form.service} onChange={handleChange} placeholder="Jasa yang diinginkan" required className="w-full border rounded p-3" />
          <textarea name="message" value={form.message} onChange={handleChange} placeholder="Pesan tambahan (opsional)" className="w-full border rounded p-3" rows="4"></textarea>
          <Button asChild className="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-full w-full">
            <a href={generateWhatsAppLink()} target="_blank" rel="noopener noreferrer">
              <Send className="mr-2" /> Kirim Pesanan via WhatsApp
            </a>
          </Button>
        </div>

        <div className="bg-white p-8 rounded-xl shadow mb-10">
          <h3 className="text-xl font-bold mb-6">Testimoni Pelanggan:</h3>
          <div className="space-y-6">
            {testimonials.map((item, idx) => (
              <blockquote key={idx} className="text-gray-600 italic">
                "{item.quote}"
                <cite className="block text-right text-gray-800 font-semibold mt-2">{item.author}</cite>
              </blockquote>
            ))}
          </div>
        </div>

        <div className="bg-gray-50 p-6 rounded-xl shadow mb-10">
          <h3 className="text-xl font-bold mb-4 flex items-center justify-center gap-2"><MessageSquare /> Tinggalkan Komentar</h3>
          <textarea placeholder="Tulis komentarmu di sini..." className="w-full border rounded p-4 mb-4" rows="4"></textarea>
          <Button className="bg-blue-500 text-white hover:bg-blue-600 px-6 py-2 rounded-full">Kirim Komentar</Button>
        </div>

        <footer className="text-sm text-gray-400">&copy; 2025 Open Jasa. All rights reserved.</footer>
      </div>
    </div>
  );
}
