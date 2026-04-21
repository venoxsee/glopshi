import React from "react";

export default function Store() {
  const products = [
    {
      id: 1,
      name: "Premium Leather Watch",
      price: "₹7,999",
      image: "https://via.placeholder.com/300",
    },
    {
      id: 2,
      name: "Minimalist Sneakers",
      price: "₹5,499",
      image: "https://via.placeholder.com/300",
    },
  ];

  return (
    <div className="bg-white text-gray-900 font-sans">
      {/* Navbar */}
      <header className="flex justify-between items-center p-6 shadow-sm">
        <h1 className="text-2xl font-bold tracking-wide">LUXE</h1>
        <nav className="space-x-6">
          <a href="#" className="hover:text-gray-500">Home</a>
          <a href="#" className="hover:text-gray-500">Shop</a>
          <a href="#" className="hover:text-gray-500">Contact</a>
        </nav>
      </header>

      {/* Hero Section */}
      <section className="text-center py-20 bg-gray-100">
        <h2 className="text-4xl font-semibold mb-4">
          Elevate Your Style
        </h2>
        <p className="text-gray-600 mb-6">
          Premium quality products for modern living
        </p>
        <button className="bg-black text-white px-6 py-3 rounded-full">
          Shop Now
        </button>
      </section>

      {/* Product Grid */}
      <section className="p-10 grid grid-cols-1 md:grid-cols-3 gap-8">
        {products.map((product) => (
          <div key={product.id} className="border rounded-xl p-4 hover:shadow-lg transition">
            <img src={product.image} alt={product.name} className="mb-4 rounded-lg"/>
            <h3 className="text-lg font-medium">{product.name}</h3>
            <p className="text-gray-500">{product.price}</p>
            <button className="mt-3 w-full bg-black text-white py-2 rounded-lg">
              Add to Cart
            </button>
          </div>
        ))}
      </section>

      {/* Footer */}
      <footer className="text-center p-6 border-t text-gray-500">
        © 2026 LUXE. All rights reserved.
      </footer>
    </div>
  );
}# glopshi
