import React from "react"; import { Button } from "@/components/ui/button"; import { Card, CardContent } from "@/components/ui/card"; import { motion } from "framer-motion";

const App = () => { return ( <div className="min-h-screen bg-gray-100 p-6"> <div className="max-w-4xl mx-auto"> <header className="text-center mb-8"> <h1 className="text-4xl font-bold text-gray-800 mb-4">Virtual Try-On</h1> <p className="text-lg text-gray-600">Coba produk baju, celana, dan lainnya secara virtual dengan animasi fashion show.</p> </header>

<motion.div className="grid gap-6 grid-cols-1 md:grid-cols-2">
      {['Baju', 'Celana', 'Sepatu', 'Aksesoris'].map((item) => (
        <Card key={item} className="bg-white rounded-2xl shadow-md overflow-hidden">
          <CardContent className="p-6">
            <h2 className="text-2xl font-semibold text-gray-800 mb-4">{item}</h2>
            <p className="text-gray-600 mb-6">Coba berbagai produk {item.toLowerCase()} dengan tampilan 3D dan animasi fashion show.</p>
            <Button variant="default" size="lg">Coba Sekarang</Button>
          </CardContent>
        </Card>
      ))}
    </motion.div>
  </div>
</div>

); };

export default App;

// Tambahkan package.json untuk konfigurasi Vercel export const config = { runtime: "edge", };

# This-Fisual_try_on
