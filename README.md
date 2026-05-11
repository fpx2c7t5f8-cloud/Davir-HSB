# Davir-HSB
Human social Bio study guide
import { useState } from "react";

const topics = [
  {
    id: 1,
    title: "Cells, Genetics & Reproduction",
    emoji: "🧬",
    color: "#22d3ee",
    bg: "#083344",
    fitb: [
      { text: "The ___ is the basic structural and functional unit of life.", answer: "cell" },
      { text: "The ___ controls all cell activities and contains DNA.", answer: "nucleus" },
      { text: "Cell division that produces two identical daughter cells is called ___.", answer: "mitosis" },
      { text: "Cell division that produces gametes with half the chromosome number is ___.", answer: "meiosis" },
      { text: "DNA stands for ___ acid.", answer: "deoxyribonucleic" },
      { text: "A ___ is a section of DNA that codes for a specific protein.", answer: "gene" },
      { text: "An organism with two identical alleles for a trait is called ___.", answer: "homozygous" },
      { text: "The physical appearance of an organism is its ___.", answer: "phenotype" },
      { text: "The genetic makeup of an organism is its ___.", answer: "genotype" },
      { text: "The ___ allele is always expressed when present.", answer: "dominant" },
      { text: "Asexual reproduction produces offspring that are genetically ___ to the parent.", answer: "identical" },
      { text: "___ are organelles that carry out photosynthesis.", answer: "chloroplasts" },
    ],
    flashcards: [
      { front: "What is mitosis?", back: "Cell division producing 2 genetically identical daughter cells — used for growth and repair." },
      { front: "What is meiosis?", back: "Cell division producing 4 gametes, each with half the parent's chromosome number (haploid)." },
      { front: "Dominant vs Recessive allele", back: "Dominant: always expressed when present.\nRecessive: only expressed when two copies are present (homozygous recessive)." },
      { front: "What is the difference between phenotype and genotype?", back: "Genotype = genetic makeup (e.g. Bb)\nPhenotype = physical appearance (e.g. brown eyes)" },
      { front: "Name 3 differences between plant and animal cells", back: "Plant cells have:\n• Cell wall (cellulose)\n• Chloroplasts\n• Large central vacuole\nAnimal cells lack all three." },
      { front: "What is sexual vs asexual reproduction?", back: "Sexual: involves two parents, gametes, fertilisation → genetic variation.\nAsexual: one parent, no gametes → genetically identical offspring." },
    ],
  },
  {
    id: 2,
    title: "Nutrition, Digestion & Enzymes",
    emoji: "🍽️",
    color: "#fb923c",
    bg: "#431407",
    fitb: [
      { text: "The process by which plants make food using sunlight is called ___.", answer: "photosynthesis" },
      { text: "The green pigment that absorbs light energy is ___.", answer: "chlorophyll" },
      { text: "Word equation for photosynthesis: CO₂ + water → ___ + oxygen.", answer: "glucose" },
      { text: "___ are biological catalysts that speed up chemical reactions.", answer: "enzymes" },
      { text: "The region of an enzyme where the substrate binds is the ___ site.", answer: "active" },
      { text: "When an enzyme is destroyed by high temperature, it is said to be ___.", answer: "denatured" },
      { text: "The enzyme ___ breaks down starch into maltose.", answer: "amylase" },
      { text: "The enzyme ___ breaks down proteins into amino acids.", answer: "protease" },
      { text: "Most absorption of nutrients occurs in the ___.", answer: "small intestine" },
      { text: "Finger-like projections that increase surface area in the small intestine are called ___.", answer: "villi" },
      { text: "Bile is produced by the ___ and emulsifies fats.", answer: "liver" },
      { text: "Water is mainly absorbed in the ___.", answer: "large intestine" },
    ],
    flashcards: [
      { front: "What is the role of enzymes?", back: "Biological catalysts that speed up chemical reactions without being used up. Made of protein." },
      { front: "What happens when an enzyme is denatured?", back: "High temperature or extreme pH changes the shape of the active site — the substrate can no longer bind and the enzyme stops working." },
      { front: "Amylase, Protease, Lipase — what does each break down?", back: "Amylase → starch → maltose\nProtease → proteins → amino acids\nLipase → lipids → fatty acids + glycerol" },
      { front: "What is the role of bile?", back: "Produced by the liver, stored in the gallbladder. Emulsifies fats (breaks them into smaller droplets) to increase surface area for lipase." },
      { front: "Where does most digestion and absorption occur?", back: "Small intestine — villi increase surface area for absorption into the bloodstream." },
      { front: "Autotroph vs Heterotroph", back: "Autotroph (producer): makes own food via photosynthesis.\nHeterotroph (consumer): cannot make own food, must consume other organisms." },
    ],
  },
  {
    id: 3,
    title: "Movement & Sensitivity",
    emoji: "⚡",
    color: "#a78bfa",
    bg: "#2e1065",
    fitb: [
      { text: "The ___ system coordinates responses to stimuli.", answer: "nervous" },
      { text: "The basic unit of the nervous system is the ___.", answer: "neurone" },
      { text: "Nerve impulses travel from sense organ to brain along ___ neurones.", answer: "sensory" },
      { text: "Nerve impulses travel from brain to effector along ___ neurones.", answer: "motor" },
      { text: "A ___ is an automatic response to a stimulus not involving the brain.", answer: "reflex action" },
      { text: "The gap between two neurones is called a ___.", answer: "synapse" },
      { text: "The ___ controls how much light enters the eye.", answer: "iris" },
      { text: "In bright light, the pupil becomes ___.", answer: "smaller (constricts)" },
      { text: "Bones are connected to each other by ___.", answer: "ligaments" },
      { text: "Muscles are connected to bones by ___.", answer: "tendons" },
      { text: "Muscles work in ___ pairs.", answer: "antagonistic" },
      { text: "Hormones are transported around the body in the ___.", answer: "blood" },
    ],
    flashcards: [
      { front: "What is a reflex arc? Name the pathway.", back: "An automatic response not involving conscious thought.\nPathway: Stimulus → Receptor → Sensory neurone → Relay neurone → Motor neurone → Effector → Response" },
      { front: "What is the difference between a ligament and a tendon?", back: "Ligament: connects bone to bone at a joint.\nTendon: connects muscle to bone." },
      { front: "What are antagonistic muscles? Give an example.", back: "Muscles that work in pairs — when one contracts the other relaxes.\nExample: Bicep (flexor) and Tricep (extensor) in the arm." },
      { front: "Ball-and-socket vs Hinge joint", back: "Ball-and-socket (e.g. shoulder, hip): movement in all directions.\nHinge (e.g. knee, elbow): movement in one plane only." },
      { front: "How does the eye adjust to bright vs dim light?", back: "Bright light: circular muscles contract → pupil constricts (smaller).\nDim light: radial muscles contract → pupil dilates (larger)." },
      { front: "What is the role of the endocrine system?", back: "Produces hormones (chemical messengers) secreted by glands into the blood to regulate body processes." },
    ],
  },
  {
    id: 4,
    title: "Respiration & Carbon Cycle",
    emoji: "💨",
    color: "#4ade80",
    bg: "#052e16",
    fitb: [
      { text: "Respiration is the process of releasing ___ from food.", answer: "energy" },
      { text: "Aerobic respiration: glucose + oxygen → ___ + water.", answer: "carbon dioxide" },
      { text: "___ respiration does not require oxygen.", answer: "anaerobic" },
      { text: "Anaerobic respiration in yeast produces ___ and carbon dioxide.", answer: "ethanol (alcohol)" },
      { text: "Anaerobic respiration in muscle cells produces ___.", answer: "lactic acid" },
      { text: "The accumulation of lactic acid causes muscle ___.", answer: "fatigue (cramp)" },
      { text: "The oxygen debt is repaid by ___ breathing after exercise.", answer: "increased (heavy)" },
      { text: "Carbon dioxide is returned to the atmosphere through ___ and combustion.", answer: "respiration" },
      { text: "Plants remove CO₂ from the atmosphere during ___.", answer: "photosynthesis" },
      { text: "The burning of fossil fuels is called ___.", answer: "combustion" },
      { text: "Decomposers break down dead matter releasing ___ back into the atmosphere.", answer: "carbon dioxide" },
      { text: "The carbon cycle maintains a balance of ___ in the atmosphere.", answer: "carbon dioxide" },
    ],
    flashcards: [
      { front: "Word equation for aerobic respiration", back: "Glucose + Oxygen → Carbon dioxide + Water (+ energy released)" },
      { front: "Word equation for anaerobic respiration (yeast)", back: "Glucose → Ethanol + Carbon dioxide (+ small amount of energy)" },
      { front: "Word equation for anaerobic respiration (muscles)", back: "Glucose → Lactic acid (+ small amount of energy)" },
      { front: "What is oxygen debt?", back: "The extra oxygen needed after exercise to oxidise the lactic acid that built up during anaerobic respiration." },
      { front: "How does carbon return to the atmosphere? (4 ways)", back: "1. Respiration (animals & plants)\n2. Combustion (burning fossil fuels)\n3. Decomposition (decomposers)\n4. Feeding (along food chains)" },
      { front: "What is the role of decomposers in the carbon cycle?", back: "Bacteria and fungi break down dead organisms and waste, releasing CO₂ back into the atmosphere through respiration." },
    ],
  },
  {
    id: 5,
    title: "Excretion, Homeostasis & Osmoregulation",
    emoji: "⚖️",
    color: "#f472b6",
    bg: "#4a044e",
    fitb: [
      { text: "Excretion is the removal of ___ metabolic waste products from the body.", answer: "toxic" },
      { text: "The main excretory organ for urea is the ___.", answer: "kidney" },
      { text: "Urea is produced in the ___ from the breakdown of excess amino acids.", answer: "liver" },
      { text: "CO₂ is excreted through the ___.", answer: "lungs" },
      { text: "Homeostasis is the maintenance of a ___ internal environment.", answer: "constant (stable)" },
      { text: "Body temperature in humans is maintained at approximately ___ °C.", answer: "37" },
      { text: "When body temperature rises, ___ occurs to cool the body down.", answer: "sweating" },
      { text: "The hormone ___ controls blood glucose levels by converting glucose to glycogen.", answer: "insulin" },
      { text: "Insulin is produced by the ___.", answer: "pancreas" },
      { text: "Osmoregulation is the control of ___ concentration in the blood.", answer: "water (solute)" },
      { text: "The hormone ___ controls water reabsorption in the kidney.", answer: "ADH" },
      { text: "The functional unit of the kidney is called the ___.", answer: "nephron" },
    ],
    flashcards: [
      { front: "What is excretion? Give 3 examples.", back: "Removal of toxic metabolic waste.\n• CO₂ → lungs\n• Urea → kidneys (in urine)\n• Excess water & salts → skin (sweat)" },
      { front: "What is homeostasis?", back: "The maintenance of a constant internal environment despite changes in external conditions (e.g. temperature, blood glucose, water balance)." },
      { front: "How does the body respond to high blood glucose?", back: "Pancreas detects high glucose → secretes insulin → liver converts glucose to glycogen → blood glucose falls back to normal." },
      { front: "What is the role of ADH in osmoregulation?", back: "ADH (antidiuretic hormone) is released when blood is too concentrated → kidneys reabsorb more water → less urine produced." },
      { front: "How does the body cool down when too hot?", back: "• Sweating (evaporation removes heat)\n• Vasodilation (blood vessels near skin widen → more heat lost)\n• Hairs lie flat" },
      { front: "What are the two processes in the nephron?", back: "1. Filtration: small molecules filtered from blood into nephron.\n2. Selective reabsorption: useful substances (glucose, water, salts) reabsorbed back into blood." },
    ],
  },
  {
    id: 6,
    title: "Environment & Disease",
    emoji: "🌍",
    color: "#fbbf24",
    bg: "#451a03",
    fitb: [
      { text: "A ___ is a community of organisms interacting with their environment.", answer: "ecosystem" },
      { text: "The role of an organism in its ecosystem is called its ___.", answer: "niche" },
      { text: "Organisms that break down dead matter are called ___.", answer: "decomposers" },
      { text: "The transfer of energy through a community is shown by a ___.", answer: "food chain (web)" },
      { text: "Only about ___% of energy is transferred from one trophic level to the next.", answer: "10" },
      { text: "A ___ disease is caused by a pathogen and can be passed from person to person.", answer: "communicable (infectious)" },
      { text: "HIV/AIDS attacks the body's ___ system.", answer: "immune" },
      { text: "Bacteria are killed by ___ while viruses are not.", answer: "antibiotics" },
      { text: "Vaccines work by stimulating the body to produce ___.", answer: "antibodies" },
      { text: "The clearing of forests is called ___.", answer: "deforestation" },
      { text: "The increase in Earth's average temperature due to greenhouse gases is called ___.", answer: "global warming" },
      { text: "The main greenhouse gas produced by burning fossil fuels is ___.", answer: "carbon dioxide" },
    ],
    flashcards: [
      { front: "What is the difference between a food chain and a food web?", back: "Food chain: shows one pathway of energy transfer.\nFood web: shows multiple interconnected food chains in an ecosystem." },
      { front: "Communicable vs Non-communicable disease", back: "Communicable: caused by pathogens, can spread person-to-person (e.g. flu, malaria, TB).\nNon-communicable: cannot spread (e.g. diabetes, cancer, heart disease)." },
      { front: "How do vaccines protect against disease?", back: "Vaccines introduce a weakened/dead pathogen → immune system produces antibodies → memory cells formed → faster response if real pathogen encountered." },
      { front: "Why can't antibiotics treat viral infections?", back: "Antibiotics target bacterial cell structures (e.g. cell wall). Viruses have no cell wall and reproduce inside host cells, so antibiotics have no effect." },
      { front: "What are 3 effects of deforestation?", back: "1. Increased CO₂ (fewer trees to absorb it)\n2. Loss of biodiversity (habitat destruction)\n3. Soil erosion (roots no longer hold soil)\n4. Disruption of water cycle" },
      { front: "What is the greenhouse effect?", back: "Greenhouse gases (CO₂, methane) trap heat from the sun in Earth's atmosphere → raises global temperatures → climate change." },
    ],
  },
];

export default function App() {
  const [mode, setMode] = useState("home"); // home | fitb | flash
  const [selectedTopic, setSelectedTopic] = useState(null);
  const [answers, setAnswers] = useState({});
  const [checked, setChecked] = useState(false);
  const [cardIndex, setCardIndex] = useState(0);
  const [flipped, setFlipped] = useState(false);
  const [masteredCards, setMasteredCards] = useState(new Set());

  const topic = topics.find((t) => t.id === selectedTopic);

  const openTopic = (id, m) => {
    setSelectedTopic(id);
    setMode(m);
    setAnswers({});
    setChecked(false);
    setCardIndex(0);
    setFlipped(false);
    setMasteredCards(new Set());
  };

  const checkAnswers = () => setChecked(true);
  const reset = () => { setAnswers({}); setChecked(false); };

  const score = topic
    ? topic.fitb.filter((q, i) =>
        answers[i]?.trim().toLowerCase() === q.answer.toLowerCase()
      ).length
    : 0;

  const nextCard = () => {
    setFlipped(false);
    setTimeout(() => setCardIndex((c) => (c + 1) % topic.flashcards.length), 150);
  };
  const prevCard = () => {
    setFlipped(false);
    setTimeout(() => setCardIndex((c) => (c - 1 + topic.flashcards.length) % topic.flashcards.length), 150);
  };
  const markMastered = () => {
    setMasteredCards((s) => new Set([...s, cardIndex]));
    nextCard();
  };

  return (
    <div style={styles.root}>
      <style>{`
        @import url('https://fonts.googleapis.com/css2?family=Syne:wght@700;800&family=DM+Sans:wght@400;500&display=swap');
        * { box-sizing: border-box; margin: 0; padding: 0; }
        ::-webkit-scrollbar { width: 6px; }
        ::-webkit-scrollbar-track { background: #0a0a0a; }
        ::-webkit-scrollbar-thumb { background: #333; border-radius: 3px; }
        .topic-card { transition: transform 0.18s, box-shadow 0.18s; cursor: pointer; }
        .topic-card:hover { transform: translateY(-4px) scale(1.02); }
        .mode-btn { transition: all 0.15s; cursor: pointer; }
        .mode-btn:hover { opacity: 0.85; transform: scale(0.98); }
        .flip-card { perspective: 1000px; cursor: pointer; }
        .flip-inner { transition: transform 0.5s cubic-bezier(0.4,0,0.2,1); transform-style: preserve-3d; position: relative; }
        .flip-inner.flipped { transform: rotateY(180deg); }
        .flip-front, .flip-back { backface-visibility: hidden; -webkit-backface-visibility: hidden; }
        .flip-back { transform: rotateY(180deg); }
        input:focus { outline: none; }
        .nav-btn { transition: all 0.15s; cursor: pointer; }
        .nav-btn:hover { opacity: 0.8; }
        .check-btn:hover { filter: brightness(1.1); }
      `}</style>

      {/* HOME */}
      {mode === "home" && (
        <div style={styles.home}>
          <div style={styles.header}>
            <div style={styles.badge}>CSEC · Human & Social Biology</div>
            <h1 style={styles.title}>Study Hub</h1>
            <p style={styles.subtitle}>Choose a topic to practise</p>
          </div>
          <div style={styles.grid}>
            {topics.map((t) => (
              <div key={t.id} className="topic-card" style={{ ...styles.topicCard, borderColor: t.color + "55" }}>
                <div style={{ ...styles.topicEmoji }}>{t.emoji}</div>
                <div style={styles.topicNum} >Section {t.id}</div>
                <div style={{ ...styles.topicTitle, color: t.color }}>{t.title}</div>
                <div style={styles.topicActions}>
                  <button className="mode-btn" style={{ ...styles.actionBtn, background: t.color + "22", color: t.color, border: `1px solid ${t.color}55` }} onClick={() => openTopic(t.id, "fitb")}>
                    📝 Fill-in-Blank
                  </button>
                  <button className="mode-btn" style={{ ...styles.actionBtn, background: t.color + "22", color: t.color, border: `1px solid ${t.color}55` }} onClick={() => openTopic(t.id, "flash")}>
                    🃏 Flashcards
                  </button>
                </div>
              </div>
            ))}
          </div>
        </div>
      )}

      {/* FITB MODE */}
      {mode === "fitb" && topic && (
        <div style={styles.page}>
          <button onClick={() => setMode("home")} style={styles.back}>← Back</button>
          <div style={{ ...styles.pageHeader, borderColor: topic.color }}>
            <span style={styles.pageEmoji}>{topic.emoji}</span>
            <div>
              <div style={styles.pageSection}>Section {topic.id} · Fill in the Blank</div>
              <div style={{ ...styles.pageTitle, color: topic.color }}>{topic.title}</div>
            </div>
          </div>

          {checked && (
            <div style={{ ...styles.scoreBox, borderColor: topic.color, background: topic.color + "15" }}>
              <span style={{ color: topic.color, fontSize: "1.5rem", fontFamily: "Syne, sans-serif", fontWeight: 800 }}>
                {score}/{topic.fitb.length}
              </span>
              <span style={{ color: "#aaa", fontSize: "0.9rem" }}>
                {score === topic.fitb.length ? " 🎉 Perfect score!" : score >= topic.fitb.length * 0.7 ? " 👍 Good effort!" : " 📚 Keep studying!"}
              </span>
            </div>
          )}

          <div style={styles.fitbList}>
            {topic.fitb.map((q, i) => {
              const userAns = (answers[i] || "").trim().toLowerCase();
              const correct = userAns === q.answer.toLowerCase();
              const parts = q.text.split("___");
              let borderCol = "#2a2a2a";
              if (checked) borderCol = correct ? "#4ade80" : "#f87171";
              return (
                <div key={i} style={{ ...styles.fitbRow, borderColor: borderCol, background: checked ? (correct ? "#4ade8011" : "#f8717111") : "#111" }}>
                  <div style={styles.qNum}>{i + 1}</div>
                  <div style={styles.qContent}>
                    <div style={styles.qText}>
                      {parts[0]}
                      <input
                        value={answers[i] || ""}
                        onChange={(e) => setAnswers({ ...answers, [i]: e.target.value })}
                        disabled={checked}
                        placeholder="type answer…"
                        style={{ ...styles.input, borderColor: checked ? (correct ? "#4ade80" : "#f87171") : topic.color + "77", color: checked ? (correct ? "#4ade80" : "#f87171") : "#fff" }}
                      />
                      {parts[1]}
                    </div>
                    {checked && !correct && (
                      <div style={styles.correctAns}>✓ {q.answer}</div>
                    )}
                  </div>
                </div>
              );
            })}
          </div>

          <div style={styles.btnRow}>
            {!checked ? (
              <button className="check-btn" onClick={checkAnswers} style={{ ...styles.checkBtn, background: topic.color, color: "#000" }}>
                Check Answers
              </button>
            ) : (
              <button className="check-btn" onClick={reset} style={{ ...styles.checkBtn, background: "#222", color: "#fff", border: "1px solid #444" }}>
                Try Again
              </button>
            )}
            <button onClick={() => openTopic(topic.id, "flash")} style={{ ...styles.checkBtn, background: "transparent", color: topic.color, border: `1px solid ${topic.color}` }}>
              🃏 Flashcards
            </button>
          </div>
        </div>
      )}

      {/* FLASHCARD MODE */}
      {mode === "flash" && topic && (
        <div style={styles.page}>
          <button onClick={() => setMode("home")} style={styles.back}>← Back</button>
          <div style={{ ...styles.pageHeader, borderColor: topic.color }}>
            <span style={styles.pageEmoji}>{topic.emoji}</span>
            <div>
              <div style={styles.pageSection}>Section {topic.id} · Flashcards</div>
              <div style={{ ...styles.pageTitle, color: topic.color }}>{topic.title}</div>
            </div>
          </div>

          <div style={styles.flashMeta}>
            <span style={{ color: "#666" }}>Card {cardIndex + 1} of {topic.flashcards.length}</span>
            <span style={{ color: "#4ade80", fontSize: "0.85rem" }}>
              {masteredCards.size > 0 && `✓ ${masteredCards.size} mastered`}
            </span>
          </div>

          {/* Progress bar */}
          <div style={styles.progressBg}>
            <div style={{ ...styles.progressFill, width: `${((cardIndex + 1) / topic.flashcards.length) * 100}%`, background: topic.color }} />
          </div>

          <div className="flip-card" style={styles.flipCard} onClick={() => setFlipped(!flipped)}>
            <div className={`flip-inner${flipped ? " flipped" : ""}`} style={styles.flipInner}>
              {/* Front */}
              <div className="flip-front" style={{ ...styles.flipFace, background: topic.bg, border: `2px solid ${topic.color}44` }}>
                <div style={styles.flipLabel}>QUESTION</div>
                <div style={{ ...styles.flipText, color: topic.color }}>{topic.flashcards[cardIndex].front}</div>
                <div style={styles.flipHint}>tap to reveal answer</div>
              </div>
              {/* Back */}
              <div className="flip-back" style={{ ...styles.flipFace, ...styles.flipFaceBack, background: "#111", border: `2px solid ${topic.color}88` }}>
                <div style={styles.flipLabel}>ANSWER</div>
                <div style={{ ...styles.flipText, color: "#fff", fontSize: "1rem", whiteSpace: "pre-line", textAlign: "left", maxWidth: "90%" }}>
                  {topic.flashcards[cardIndex].back}
                </div>
              </div>
            </div>
          </div>

          <div style={styles.cardActions}>
            <button className="nav-btn" onClick={prevCard} style={styles.navBtn}>← Prev</button>
            <button onClick={markMastered} style={{ ...styles.masteredBtn, borderColor: topic.color, color: masteredCards.has(cardIndex) ? "#4ade80" : topic.color }}>
              {masteredCards.has(cardIndex) ? "✓ Mastered" : "Got it ✓"}
            </button>
            <button className="nav-btn" onClick={nextCard} style={styles.navBtn}>Next →</button>
          </div>

          <button onClick={() => openTopic(topic.id, "fitb")} style={{ ...styles.switchBtn, color: topic.color, borderColor: topic.color + "55" }}>
            📝 Switch to Fill-in-Blank
          </button>
        </div>
      )}
    </div>
  );
}

const styles = {
  root: {
    minHeight: "100vh",
    background: "#0a0a0a",
    color: "#fff",
    fontFamily: "'DM Sans', sans-serif",
    padding: "0 0 60px",
  },
  home: { maxWidth: 720, margin: "0 auto", padding: "40px 20px 20px" },
  header: { textAlign: "center", marginBottom: 36 },
  badge: { display: "inline-block", background: "#1a1a1a", border: "1px solid #333", borderRadius: 20, padding: "4px 14px", fontSize: "0.75rem", color: "#888", letterSpacing: "0.08em", marginBottom: 12 },
  title: { fontFamily: "Syne, sans-serif", fontSize: "2.4rem", fontWeight: 800, letterSpacing: "-0.02em", marginBottom: 6 },
  subtitle: { color: "#666", fontSize: "1rem" },
  grid: { display: "grid", gridTemplateColumns: "1fr 1fr", gap: 14 },
  topicCard: { background: "#111", border: "1px solid", borderRadius: 16, padding: "20px 18px", display: "flex", flexDirection: "column", gap: 8 },
  topicEmoji: { fontSize: "1.6rem" },
  topicNum: { fontSize: "0.72rem", color: "#555", letterSpacing: "0.1em", textTransform: "uppercase" },
  topicTitle: { fontFamily: "Syne, sans-serif", fontWeight: 700, fontSize: "0.95rem", lineHeight: 1.3 },
  topicActions: { display: "flex", flexDirection: "column", gap: 6, marginTop: 6 },
  actionBtn: { borderRadius: 8, padding: "7px 10px", fontSize: "0.8rem", fontFamily: "'DM Sans', sans-serif", fontWeight: 500, cursor: "pointer" },
  page: { maxWidth: 680, margin: "0 auto", padding: "28px 18px" },
  back: { background: "none", border: "none", color: "#666", cursor: "pointer", fontSize: "0.9rem", marginBottom: 20, padding: 0, fontFamily: "'DM Sans', sans-serif" },
  pageHeader: { display: "flex", alignItems: "center", gap: 14, borderLeft: "3px solid", paddingLeft: 14, marginBottom: 24 },
  pageEmoji: { fontSize: "2rem" },
  pageSection: { fontSize: "0.72rem", color: "#555", textTransform: "uppercase", letterSpacing: "0.1em", marginBottom: 2 },
  pageTitle: { fontFamily: "Syne, sans-serif", fontWeight: 800, fontSize: "1.25rem" },
  scoreBox: { display: "flex", alignItems: "center", gap: 10, border: "1px solid", borderRadius: 12, padding: "12px 18px", marginBottom: 20 },
  fitbList: { display: "flex", flexDirection: "column", gap: 10 },
  fitbRow: { display: "flex", gap: 12, border: "1px solid", borderRadius: 12, padding: "14px 14px", alignItems: "flex-start" },
  qNum: { minWidth: 26, height: 26, borderRadius: "50%", background: "#1e1e1e", display: "flex", alignItems: "center", justifyContent: "center", fontSize: "0.75rem", color: "#666", fontWeight: 700, flexShrink: 0, marginTop: 2 },
  qContent: { flex: 1 },
  qText: { fontSize: "0.92rem", lineHeight: 1.7, color: "#ddd", display: "flex", flexWrap: "wrap", alignItems: "center", gap: 4 },
  input: { border: "1px solid", borderRadius: 6, background: "#1a1a1a", color: "#fff", padding: "3px 10px", fontSize: "0.88rem", fontFamily: "'DM Sans', sans-serif", minWidth: 100, maxWidth: 180 },
  correctAns: { marginTop: 6, fontSize: "0.82rem", color: "#4ade80", fontWeight: 500 },
  btnRow: { display: "flex", gap: 10, marginTop: 24, flexWrap: "wrap" },
  checkBtn: { borderRadius: 10, padding: "11px 24px", fontSize: "0.92rem", fontWeight: 600, fontFamily: "'DM Sans', sans-serif", cursor: "pointer", border: "none", flex: 1 },
  // Flashcard
  flashMeta: { display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 8 },
  progressBg: { height: 4, background: "#1e1e1e", borderRadius: 4, marginBottom: 24, overflow: "hidden" },
  progressFill: { height: "100%", borderRadius: 4, transition: "width 0.3s" },
  flipCard: { width: "100%", height: 260 },
  flipInner: { width: "100%", height: "100%", position: "relative" },
  flipFace: { position: "absolute", width: "100%", height: "100%", borderRadius: 18, display: "flex", flexDirection: "column", alignItems: "center", justifyContent: "center", padding: "28px 24px", gap: 14 },
  flipFaceBack: {},
  flipLabel: { fontSize: "0.65rem", letterSpacing: "0.15em", color: "#555", textTransform: "uppercase", position: "absolute", top: 16, left: 20 },
  flipText: { fontFamily: "Syne, sans-serif", fontWeight: 700, fontSize: "1.15rem", textAlign: "center", lineHeight: 1.45 },
  flipHint: { fontSize: "0.75rem", color: "#444", position: "absolute", bottom: 16 },
  cardActions: { display: "flex", justifyContent: "space-between", alignItems: "center", marginTop: 20, gap: 10 },
  navBtn: { background: "#1a1a1a", border: "1px solid #333", color: "#aaa", borderRadius: 10, padding: "10px 20px", fontFamily: "'DM Sans', sans-serif", fontSize: "0.88rem", cursor: "pointer" },
  masteredBtn: { flex: 1, background: "transparent", border: "1px solid", borderRadius: 10, padding: "10px 16px", fontFamily: "'DM Sans', sans-serif", fontSize: "0.88rem", fontWeight: 600, cursor: "pointer" },
  switchBtn: { display: "block", width: "100%", marginTop: 14, background: "transparent", border: "1px solid", borderRadius: 10, padding: "10px", fontFamily: "'DM Sans', sans-serif", fontSize: "0.85rem", cursor: "pointer", textAlign: "center" },
};
