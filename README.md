// File: app/page.tsx (Next.js 14)
import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

const accounts = [
  {
    id: 1,
    username: "RobloxKing123",
    price: "150K",
    avatar: "/images/avatar1.png",
    description: "Acc full item, có Pet quý, level cao."
  },
  {
    id: 2,
    username: "BuilderBoyVN",
    price: "100K",
    avatar: "/images/avatar2.png",
    description: "Acc thường, đã chơi Blox Fruits và Adopt Me."
  }
];

export default function Home() {
  return (
    <main className="min-h-screen bg-gray-900 text-white p-4">
      <h1 className="text-4xl font-bold text-center mb-8">Shop ACC Roblox</h1>
      <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        {accounts.map((acc) => (
          <Card key={acc.id} className="bg-gray-800">
            <CardContent className="p-4">
              <img
                src={acc.avatar}
                alt={acc.username}
                className="w-full h-40 object-cover rounded-xl mb-4"
              />
              <h2 className="text-xl font-semibold">{acc.username}</h2>
              <p className="text-sm text-gray-300 mb-2">{acc.description}</p>
              <p className="text-lg font-bold text-green-400">Giá: {acc.price}</p>
              <Button className="mt-4 w-full bg-blue-600 hover:bg-blue-500">
                Mua ngay
              </Button>
            </CardContent>
          </Card>
        ))}
      </div>
    </main>
  );
}
