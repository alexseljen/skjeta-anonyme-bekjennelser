import { useState } from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Textarea } from "@/components/ui/textarea";
import { motion } from "framer-motion";

export default function AnonymousConfessions() {
  const [confessions, setConfessions] = useState([
    "Jeg løy om at jeg var syk for å slippe en kjedelig date...",
    "Jeg stjeler alltid sjokolade fra jobben, og ingen har merket det enda!",
  ]);
  const [newConfession, setNewConfession] = useState("");

  const handleSubmit = () => {
    if (newConfession.trim() !== "") {
      setConfessions([newConfession, ...confessions]);
      setNewConfession("");
    }
  };

  return (
    <div className="max-w-xl mx-auto p-4 space-y-4">
      <h1 className="text-2xl font-bold text-center">💀 Anonyme Bekjennelser 💀</h1>
      <Textarea
        value={newConfession}
        onChange={(e) => setNewConfession(e.target.value)}
        placeholder="Skriv din skitne hemmelighet her..."
        className="w-full p-2 border rounded-lg"
      />
      <Button onClick={handleSubmit} className="w-full bg-red-500 text-white hover:bg-red-600">
        Send inn anonymt
      </Button>
      <div className="space-y-3">
        {confessions.map((confession, index) => (
          <motion.div key={index} initial={{ opacity: 0 }} animate={{ opacity: 1 }}>
            <Card className="p-4 bg-gray-100 border-l-4 border-red-500">
              <CardContent>{confession}</CardContent>
            </Card>
          </motion.div>
        ))}
      </div>
    </div>
  );
}

// Klargjort for bruk på Skjeta.no
