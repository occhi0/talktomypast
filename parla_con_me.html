const express = require("express");
const cors = require("cors");
const bodyParser = require("body-parser");
const dotenv = require("dotenv");
const OpenAI = require("openai");

dotenv.config();

const app = express();
const port = 3000;

app.use(cors());
app.use(bodyParser.json());

const openai = new OpenAI({
  apiKey: process.env.OPENAI_API_KEY,
});

app.post("/chat", async (req, res) => {
  const { messaggio, persona } = req.body;

  const tono = persona === "passato"
    ? "ironico, riflessivo, a volte pungente, ma sempre con empatia. Come se fosse una lettera scritta a mano da sé stessi da giovani."
    : "più saggio, pacato, con una visione ampia e compassionevole. Come se fosse una lettera dal proprio sé futuro.";

  const firma = persona === "passato"
    ? "Con affetto, Il tuo sé del passato"
    : "Con affetto, Il tuo sé futuro";

  const prompt = `
L'utente ha scritto: "${messaggio}".
Rispondi come ${persona === "passato" ? "il sé del passato" : "il sé del futuro"},
con tono ${tono}
e termina con la firma "${firma}".
`;

  try {
    const completion = await openai.chat.completions.create({
      model: "gpt-3.5-turbo", // Cambia in "gpt-4.1" o "gpt-4" se preferisci
      messages: [{ role: "user", content: prompt }],
    });

    const risposta = completion.choices[0].message.content;
    res.json({ risposta });
  } catch (error) {
    console.error("Errore:", error);
    res.status(500).json({
      errore: "Errore nella generazione della risposta AI.",
      dettaglio: error.message || "Errore sconosciuto",
    });
  }
});

app.listen(port, () => {
  console.log(`Server in ascolto su http://localhost:${port}`);
});
