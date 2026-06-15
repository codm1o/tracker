import { useState, useEffect, useRef } from "react";

const DAYS = ["Segunda", "Terça", "Quarta", "Quinta", "Sexta", "Sábado", "Domingo"];

const MEALS = {
  "Café da Manhã": {
    target: { kcal: 800, prot: 60, carb: 85, fat: 28 },
    options: [
      {
        label: "A — Pão + Ovos",
        items: ["2 pães franceses", "2 fatias de mortadela", "1 fatia de queijo", "2 col. requeijão", "3 ovos mexidos", "1 iogurte Danone"],
        macros: { kcal: 800, prot: 40, carb: 52, fat: 38 }
      },
      {
        label: "B — Tapioca Reforçada",
        items: ["1 tapioca grande (80g)", "2 ovos + 60g frango + queijo", "2 col. requeijão", "1 iogurte integral", "1 banana"],
        macros: { kcal: 780, prot: 45, carb: 65, fat: 25 }
      },
      {
        label: "C — Batata-doce + Ovos",
        items: ["150g batata-doce + margarina", "4 ovos mexidos", "1 iogurte integral", "1 banana", "1 Yakult"],
        macros: { kcal: 715, prot: 35, carb: 50, fat: 27 }
      }
    ]
  },
  "Almoço": {
    target: { kcal: 700, prot: 90, carb: 5, fat: 35 },
    options: [
      {
        label: "Frango Grelhado",
        items: ["220g frango grelhado/assado", "200g legumes refogados no azeite", "1 ovo cozido"],
        macros: { kcal: 700, prot: 72, carb: 8, fat: 30 }
      },
      {
        label: "Carne Moída",
        items: ["200g carne moída (patinho)", "Legumes variados no azeite", "Cebola, tomate, pimentão, abobrinha"],
        macros: { kcal: 700, prot: 62, carb: 8, fat: 38 }
      },
      {
        label: "Carne de Panela",
        items: ["200g carne de panela", "Couve refogada + cenoura + abobrinha", "Azeite no preparo"],
        macros: { kcal: 680, prot: 58, carb: 8, fat: 36 }
      }
    ]
  },
  "Café da Noite": {
    target: { kcal: 550, prot: 70, carb: 5, fat: 27 },
    options: [
      {
        label: "A — Omelete Proteica",
        items: ["4 ovos com queijo e tomate", "1 iogurte integral", "2 col. requeijão", "1 Yakult"],
        macros: { kcal: 570, prot: 37, carb: 5, fat: 34 }
      },
      {
        label: "B — Ovos + Frios",
        items: ["3 ovos mexidos na margarina", "2 fatias de mortadela", "1 fatia de queijo", "1 iogurte desnatado", "1 Yakult"],
        macros: { kcal: 510, prot: 37, carb: 4, fat: 28 }
      },
      {
        label: "C — Noite Leve",
        items: ["3 ovos cozidos", "1 iogurte integral", "2 col. requeijão", "1 Yakult", "1 fatia de queijo"],
        macros: { kcal: 530, prot: 29, carb: 4, fat: 28 }
      }
    ]
  }
};

const WORKOUTS = {
  "Segunda": {
    focus: "Bíceps + Costas + Abdômen",
    exercises: [
      { name: "Rosca direta bilateral", sets: 4, reps: "10–12" },
      { name: "Rosca martelo alternada", sets: 3, reps: "12 cada" },
      { name: "Rosca concentrada", sets: 3, reps: "10–12 cada" },
      { name: "Rosca inversa (pronada)", sets: 3, reps: "15" },
      { name: "Remada curvada com halteres", sets: 4, reps: "10–12" },
      { name: "Remada unilateral", sets: 3, reps: "12 cada" },
      { name: "Cruncho abdominal", sets: 3, reps: "25" },
      { name: "Abdominal bicicleta", sets: 3, reps: "20" },
      { name: "Prancha frontal", sets: 3, reps: "40 seg" },
    ],
    bike: "12 min — 2 aquec / 8 intervalado (30s forte + 30s mod) / 2 cool"
  },
  "Terça": {
    focus: "Tríceps + Peito + Abdômen",
    exercises: [
      { name: "Extensão tríceps overhead (2 mãos)", sets: 4, reps: "10–12" },
      { name: "Tríceps testa deitado no chão", sets: 3, reps: "12" },
      { name: "Kickback de tríceps", sets: 3, reps: "12–15 cada" },
      { name: "Extensão unilateral overhead", sets: 3, reps: "12 cada" },
      { name: "Supino com halteres no chão", sets: 4, reps: "12" },
      { name: "Crucifixo no chão", sets: 3, reps: "12" },
      { name: "Flexão close grip", sets: 3, reps: "até falha" },
      { name: "Elevação de pernas deitado", sets: 3, reps: "15" },
      { name: "Prancha lateral", sets: 2, reps: "35 seg cada" },
      { name: "Cruncho oblíquo", sets: 3, reps: "20" },
    ],
    bike: "12 min — ritmo forte constante (80%)"
  },
  "Quarta": {
    focus: "Pernas + Ombros + Abdômen",
    exercises: [
      { name: "Agachamento goblet com halter", sets: 4, reps: "15" },
      { name: "Afundo alternado com halteres", sets: 3, reps: "12 cada" },
      { name: "Stiff com halteres", sets: 3, reps: "12" },
      { name: "Elevação de panturrilha em pé", sets: 3, reps: "25" },
      { name: "Desenvolvimento Arnold", sets: 4, reps: "10–12" },
      { name: "Elevação lateral", sets: 3, reps: "12–15" },
      { name: "Elevação frontal alternada", sets: 3, reps: "12 cada" },
      { name: "Cruncho", sets: 3, reps: "25" },
      { name: "Prancha", sets: 3, reps: "45 seg" },
      { name: "Abdominal bicicleta", sets: 2, reps: "20" },
    ],
    bike: "10 min — intervalado curto (20s sprint / 40s recup, 6 ciclos)"
  },
  "Quinta": {
    focus: "Bíceps + Antebraço + Abdômen",
    exercises: [
      { name: "Rosca direta bilateral", sets: 3, reps: "12" },
      { name: "Rosca alternada em pé", sets: 3, reps: "10 cada" },
      { name: "Rosca concentrada (coxa)", sets: 3, reps: "12 cada" },
      { name: "Rosca inversa (pronada)", sets: 4, reps: "15" },
      { name: "Flexão de punho (halteres nos joelhos)", sets: 3, reps: "20" },
      { name: "Extensão de punho", sets: 3, reps: "20" },
      { name: "Farmer's walk (30 passos)", sets: 3, reps: "30 passos" },
      { name: "Cruncho", sets: 3, reps: "25" },
      { name: "Elevação de pernas", sets: 3, reps: "15" },
      { name: "Prancha", sets: 3, reps: "45 seg" },
      { name: "Abdominal bicicleta", sets: 3, reps: "20" },
    ],
    bike: "12 min — moderado-forte contínuo"
  },
  "Sexta": {
    focus: "Circuito Metabólico Completo",
    exercises: [
      { name: "Supino halter no chão", sets: 4, reps: "12" },
      { name: "Remada curvada", sets: 4, reps: "12" },
      { name: "Extensão tríceps overhead", sets: 4, reps: "12" },
      { name: "Rosca direta", sets: 4, reps: "12" },
      { name: "Desenvolvimento ombro", sets: 4, reps: "10" },
      { name: "Agachamento goblet", sets: 4, reps: "15" },
      { name: "Prancha", sets: 4, reps: "30 seg" },
    ],
    bike: "15 min — 30s sprint máximo / 30s recuperação, 10 ciclos"
  },
  "Sábado": {
    focus: "Descanso Ativo",
    exercises: [],
    bike: "Caminhada 20–30 min (opcional)"
  },
  "Domingo": {
    focus: "Descanso Ativo",
    exercises: [],
    bike: "Caminhada 20–30 min (opcional)"
  }
};

const TEAS = [
  { name: "Gengibre + limão", time: "04h35", role: "Termogênese pré-treino" },
  { name: "Hortelã", time: "~09h", role: "Digestão pós-café" },
  { name: "Hibisco", time: "14h–15h", role: "Diurético" },
  { name: "Camomila", time: "21h30", role: "Relaxamento e sono" },
];

function getTodayKey() {
  return new Date().toISOString().split("T")[0];
}

function getDayName() {
  const days = ["Domingo","Segunda","Terça","Quarta","Quinta","Sexta","Sábado"];
  return days[new Date().getDay()];
}

function loadState() {
  try {
    const raw = localStorage.getItem("tracker_v2");
    return raw ? JSON.parse(raw) : {};
  } catch { return {}; }
}

function saveState(state) {
  try {
    localStorage.setItem("tracker_v2", JSON.stringify(state));
  } catch {}
}

function MacroBadge({ label, value, color }) {
  return (
    <div style={{ textAlign: "center", background: color + "22", borderRadius: 10, padding: "6px 10px", minWidth: 60 }}>
      <div style={{ fontSize: 18, fontWeight: 700, color }}>{value}</div>
      <div style={{ fontSize: 11, color: "#888" }}>{label}</div>
    </div>
  );
}

function ProgressRing({ value, max, color, size = 56, label, unit = "" }) {
  const r = (size - 8) / 2;
  const circ = 2 * Math.PI * r;
  const pct = Math.min(value / max, 1);
  const dash = pct * circ;
  return (
    <div style={{ display: "flex", flexDirection: "column", alignItems: "center", gap: 2 }}>
      <svg width={size} height={size}>
        <circle cx={size/2} cy={size/2} r={r} fill="none" stroke="#2a2a2a" strokeWidth={7} />
        <circle cx={size/2} cy={size/2} r={r} fill="none" stroke={color} strokeWidth={7}
          strokeDasharray={`${dash} ${circ}`} strokeLinecap="round"
          transform={`rotate(-90 ${size/2} ${size/2})`} />
        <text x={size/2} y={size/2+5} textAnchor="middle" fill={color} fontSize={13} fontWeight="700">{value}</text>
      </svg>
      <div style={{ fontSize: 11, color: "#888" }}>{label}</div>
    </div>
  );
}

export default function App() {
  const todayKey = getTodayKey();
  const dayName = getDayName();

  const [allData, setAllData] = useState(() => loadState());
  const [tab, setTab] = useState("hoje");
  const [expandedMeal, setExpandedMeal] = useState(null);
  const [expandedEx, setExpandedEx] = useState({});
  const [photoModal, setPhotoModal] = useState(null);
  const [weightInput, setWeightInput] = useState("");
  const [waterInput, setWaterInput] = useState("");
  const [showWeek, setShowWeek] = useState(false);
  const fileRef = useRef();

  const today = allData[todayKey] || {};

  function updateToday(patch) {
    const next = { ...allData, [todayKey]: { ...today, ...patch } };
    setAllData(next);
    saveState(next);
  }

  // Meals
  function toggleMealDone(meal) {
    const meals = today.meals || {};
    updateToday({ meals: { ...meals, [meal]: { ...meals[meal], done: !meals[meal]?.done } } });
  }
  function setMealOption(meal, idx) {
    const meals = today.meals || {};
    updateToday({ meals: { ...meals, [meal]: { ...meals[meal], option: idx } } });
  }
  function addMealNote(meal, note) {
    const meals = today.meals || {};
    updateToday({ meals: { ...meals, [meal]: { ...meals[meal], note } } });
  }

  // Exercises
  function toggleExDone(ex) {
    const exs = today.exercises || {};
    updateToday({ exercises: { ...exs, [ex]: !exs[ex] } });
  }

  // Teas
  function toggleTea(idx) {
    const teas = today.teas || {};
    updateToday({ teas: { ...teas, [idx]: !teas[idx] } });
  }

  // Water
  const waterGlasses = today.water || 0;
  function addWater() { updateToday({ water: Math.min(waterGlasses + 1, 16) }); }
  function removeWater() { updateToday({ water: Math.max(waterGlasses - 1, 0) }); }

  // Weight
  function saveWeight() {
    if (!weightInput) return;
    updateToday({ weight: parseFloat(weightInput) });
    setWeightInput("");
  }

  // Photo
  function handlePhoto(e) {
    const file = e.target.files[0];
    if (!file) return;
    const reader = new FileReader();
    reader.onload = (ev) => {
      const photos = today.photos || [];
      const label = photoModal;
      updateToday({ photos: [...photos, { src: ev.target.result, label, ts: Date.now() }] });
      setPhotoModal(null);
    };
    reader.readAsDataURL(file);
  }

  // Computed macros
  const mealNames = Object.keys(MEALS);
  let totalKcal = 0, totalProt = 0, totalCarb = 0, totalFat = 0;
  mealNames.forEach(m => {
    const mData = today.meals?.[m];
    if (mData?.done) {
      const opt = MEALS[m].options[mData.option ?? 0];
      totalKcal += opt.macros.kcal;
      totalProt += opt.macros.prot;
      totalCarb += opt.macros.carb;
      totalFat += opt.macros.fat;
    }
  });

  const workout = WORKOUTS[dayName] || WORKOUTS["Sábado"];
  const exsDone = today.exercises || {};
  const exCount = workout.exercises.length;
  const exDoneCount = workout.exercises.filter(e => exsDone[e.name]).length;

  // Weekly summary
  const last7 = [];
  for (let i = 6; i >= 0; i--) {
    const d = new Date();
    d.setDate(d.getDate() - i);
    const k = d.toISOString().split("T")[0];
    const dayD = ["Dom","Seg","Ter","Qua","Qui","Sex","Sáb"][d.getDay()];
    last7.push({ key: k, label: dayD, data: allData[k] || {} });
  }

  const accent = "#00e5a0";
  const bg = "#0f0f0f";
  const card = "#1a1a1a";
  const card2 = "#222";

  const tabStyle = (t) => ({
    flex: 1,
    padding: "10px 0",
    background: tab === t ? accent : "transparent",
    color: tab === t ? "#000" : "#888",
    border: "none",
    fontWeight: 700,
    fontSize: 13,
    cursor: "pointer",
    borderRadius: tab === t ? 10 : 0,
    transition: "all 0.2s"
  });

  return (
    <div style={{ background: bg, minHeight: "100vh", color: "#fff", fontFamily: "'Inter', system-ui, sans-serif", maxWidth: 430, margin: "0 auto", paddingBottom: 80 }}>
      {/* Header */}
      <div style={{ padding: "20px 16px 12px", background: "#111", borderBottom: "1px solid #222", position: "sticky", top: 0, zIndex: 100 }}>
        <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start" }}>
          <div>
            <div style={{ fontSize: 11, color: accent, letterSpacing: 2, fontWeight: 700, textTransform: "uppercase" }}>Plano Ceto-Flex</div>
            <div style={{ fontSize: 22, fontWeight: 800, marginTop: 2 }}>{dayName} <span style={{ color: "#555", fontSize: 14, fontWeight: 400 }}>{new Date().toLocaleDateString("pt-BR", { day: "2-digit", month: "short" })}</span></div>
          </div>
          <div style={{ textAlign: "right" }}>
            {today.weight && <div style={{ fontSize: 20, fontWeight: 700, color: accent }}>{today.weight} kg</div>}
            <button onClick={() => { const w = prompt("Peso de hoje (kg):"); if (w) updateToday({ weight: parseFloat(w) }); }}
              style={{ fontSize: 11, color: "#666", background: "none", border: "1px solid #333", borderRadius: 6, padding: "3px 8px", cursor: "pointer", marginTop: 2 }}>
              {today.weight ? "✏️ editar" : "⚖️ registrar peso"}
            </button>
          </div>
        </div>

        {/* Mini progress */}
        <div style={{ display: "flex", gap: 8, marginTop: 12 }}>
          <ProgressRing value={totalKcal} max={2050} color={accent} label="kcal" />
          <ProgressRing value={totalProt} max={220} color="#60a5fa" label="prot g" />
          <ProgressRing value={waterGlasses} max={16} color="#a78bfa" label="água (copos)" />
          <ProgressRing value={exDoneCount} max={Math.max(exCount, 1)} color="#fb923c" label="exercícios" />
        </div>
      </div>

      {/* Tabs */}
      <div style={{ display: "flex", background: "#111", padding: "8px 12px", gap: 6, position: "sticky", top: 108, zIndex: 99 }}>
        {[["hoje","Hoje"],["semana","Semana"],["fotos","Fotos"]].map(([k,l]) => (
          <button key={k} style={tabStyle(k)} onClick={() => setTab(k)}>{l}</button>
        ))}
      </div>

      {/* ---- HOJE TAB ---- */}
      {tab === "hoje" && (
        <div style={{ padding: "12px 14px", display: "flex", flexDirection: "column", gap: 14 }}>

          {/* Schedule strip */}
          <div style={{ background: card, borderRadius: 14, padding: "12px 14px" }}>
            <div style={{ fontSize: 11, color: "#555", fontWeight: 700, marginBottom: 8, letterSpacing: 1 }}>HORÁRIOS DE HOJE</div>
            <div style={{ display: "flex", gap: 6, overflowX: "auto", paddingBottom: 4 }}>
              {[
                { t: "04:30", l: "Acordar", c: "#facc15" },
                { t: "04:35", l: "☕ Chá gengibre", c: accent },
                { t: "05:00", l: "🏋️ Treino", c: "#fb923c" },
                { t: "07:00", l: "🍳 Café da manhã", c: "#60a5fa" },
                { t: "12:00", l: "🥩 Almoço", c: "#60a5fa" },
                { t: "14:00", l: "🌺 Chá hibisco", c: accent },
                { t: "21:00", l: "🥚 Café da noite", c: "#60a5fa" },
                { t: "21:30", l: "🌼 Camomila", c: accent },
                { t: "22:00", l: "😴 Dormir", c: "#facc15" },
              ].map((s, i) => (
                <div key={i} style={{ flexShrink: 0, background: "#111", borderRadius: 10, padding: "6px 10px", textAlign: "center", minWidth: 72 }}>
                  <div style={{ fontSize: 12, fontWeight: 700, color: s.c }}>{s.t}</div>
                  <div style={{ fontSize: 10, color: "#777", marginTop: 2 }}>{s.l}</div>
                </div>
              ))}
            </div>
          </div>

          {/* Meals */}
          {mealNames.map(meal => {
            const mData = today.meals?.[meal] || {};
            const selOpt = mData.option ?? 0;
            const opt = MEALS[meal].options[selOpt];
            const isOpen = expandedMeal === meal;
            return (
              <div key={meal} style={{ background: mData.done ? "#1a2e25" : card, borderRadius: 16, border: `1px solid ${mData.done ? accent + "55" : "#2a2a2a"}`, overflow: "hidden", transition: "all 0.2s" }}>
                <div style={{ display: "flex", alignItems: "center", padding: "14px 14px 12px", cursor: "pointer" }} onClick={() => setExpandedMeal(isOpen ? null : meal)}>
                  <div style={{ flex: 1 }}>
                    <div style={{ display: "flex", alignItems: "center", gap: 8 }}>
                      <div style={{ fontSize: 15, fontWeight: 700 }}>{meal}</div>
                      {mData.done && <span style={{ fontSize: 10, background: accent, color: "#000", borderRadius: 6, padding: "2px 6px", fontWeight: 700 }}>✓ OK</span>}
                    </div>
                    <div style={{ fontSize: 12, color: "#666", marginTop: 2 }}>{opt.label} · {opt.macros.kcal} kcal · {opt.macros.prot}g prot</div>
                  </div>
                  <span style={{ color: "#444", fontSize: 20 }}>{isOpen ? "▲" : "▼"}</span>
                </div>

                {isOpen && (
                  <div style={{ padding: "0 14px 14px", borderTop: "1px solid #222" }}>
                    {/* Option selector */}
                    <div style={{ marginTop: 12, marginBottom: 10 }}>
                      <div style={{ fontSize: 11, color: "#555", marginBottom: 6, fontWeight: 700 }}>ESCOLHA A OPÇÃO:</div>
                      <div style={{ display: "flex", gap: 6, flexWrap: "wrap" }}>
                        {MEALS[meal].options.map((o, i) => (
                          <button key={i} onClick={() => setMealOption(meal, i)}
                            style={{ padding: "5px 10px", borderRadius: 8, border: `1px solid ${selOpt === i ? accent : "#333"}`, background: selOpt === i ? accent + "22" : "transparent", color: selOpt === i ? accent : "#666", fontSize: 12, cursor: "pointer", fontWeight: selOpt === i ? 700 : 400 }}>
                            {o.label}
                          </button>
                        ))}
                      </div>
                    </div>

                    {/* Ingredients */}
                    <div style={{ marginBottom: 12 }}>
                      {opt.items.map((item, i) => (
                        <div key={i} style={{ fontSize: 13, color: "#bbb", padding: "3px 0", borderBottom: "1px solid #1e1e1e" }}>
                          · {item}
                        </div>
                      ))}
                    </div>

                    {/* Macros */}
                    <div style={{ display: "flex", gap: 8, marginBottom: 12 }}>
                      <MacroBadge label="kcal" value={opt.macros.kcal} color={accent} />
                      <MacroBadge label="prot" value={`${opt.macros.prot}g`} color="#60a5fa" />
                      <MacroBadge label="carb" value={`${opt.macros.carb}g`} color="#fb923c" />
                      <MacroBadge label="gord" value={`${opt.macros.fat}g`} color="#a78bfa" />
                    </div>

                    {/* Note */}
                    <textarea placeholder="Nota (substituições, o que comeu diferente...)"
                      value={mData.note || ""}
                      onChange={e => addMealNote(meal, e.target.value)}
                      style={{ width: "100%", background: "#111", border: "1px solid #333", borderRadius: 8, color: "#ccc", padding: "8px 10px", fontSize: 12, resize: "vertical", minHeight: 50, boxSizing: "border-box", fontFamily: "inherit", marginBottom: 10 }} />

                    {/* Photo + Done */}
                    <div style={{ display: "flex", gap: 8 }}>
                      <button onClick={() => { setPhotoModal(meal); fileRef.current.click(); }}
                        style={{ flex: 1, padding: "9px", borderRadius: 10, border: "1px solid #333", background: "#111", color: "#888", fontSize: 13, cursor: "pointer" }}>
                        📷 Foto
                      </button>
                      <button onClick={() => toggleMealDone(meal)}
                        style={{ flex: 2, padding: "9px", borderRadius: 10, border: `1px solid ${mData.done ? accent : "#444"}`, background: mData.done ? accent + "33" : "#111", color: mData.done ? accent : "#888", fontSize: 13, fontWeight: 700, cursor: "pointer" }}>
                        {mData.done ? "✓ Feito" : "Marcar como feito"}
                      </button>
                    </div>
                  </div>
                )}
              </div>
            );
          })}

          {/* Water tracker */}
          <div style={{ background: card, borderRadius: 16, padding: "14px" }}>
            <div style={{ fontSize: 13, fontWeight: 700, marginBottom: 10, color: "#a78bfa" }}>💧 Água — {(waterGlasses * 0.25).toFixed(2)}L / 4L</div>
            <div style={{ display: "flex", flexWrap: "wrap", gap: 6, marginBottom: 10 }}>
              {Array.from({ length: 16 }).map((_, i) => (
                <div key={i} style={{ width: 28, height: 28, borderRadius: 8, background: i < waterGlasses ? "#a78bfa" : "#222", display: "flex", alignItems: "center", justifyContent: "center", fontSize: 14 }}>
                  {i < waterGlasses ? "💧" : ""}
                </div>
              ))}
            </div>
            <div style={{ display: "flex", gap: 8 }}>
              <button onClick={removeWater} style={{ flex: 1, padding: 8, borderRadius: 10, border: "1px solid #333", background: "#111", color: "#888", fontSize: 20, cursor: "pointer" }}>−</button>
              <div style={{ flex: 2, textAlign: "center", fontSize: 13, color: "#666", alignSelf: "center" }}>250ml por copo</div>
              <button onClick={addWater} style={{ flex: 1, padding: 8, borderRadius: 10, border: `1px solid #a78bfa`, background: "#a78bfa33", color: "#a78bfa", fontSize: 20, fontWeight: 700, cursor: "pointer" }}>+</button>
            </div>
          </div>

          {/* Teas */}
          <div style={{ background: card, borderRadius: 16, padding: "14px" }}>
            <div style={{ fontSize: 13, fontWeight: 700, marginBottom: 10, color: accent }}>🍵 Chás</div>
            {TEAS.map((tea, i) => (
              <div key={i} onClick={() => toggleTea(i)} style={{ display: "flex", alignItems: "center", gap: 10, padding: "9px 0", borderBottom: "1px solid #1e1e1e", cursor: "pointer" }}>
                <div style={{ width: 22, height: 22, borderRadius: 6, border: `2px solid ${today.teas?.[i] ? accent : "#444"}`, background: today.teas?.[i] ? accent : "transparent", display: "flex", alignItems: "center", justifyContent: "center", fontSize: 12, flexShrink: 0 }}>
                  {today.teas?.[i] ? "✓" : ""}
                </div>
                <div style={{ flex: 1 }}>
                  <div style={{ fontSize: 13, fontWeight: 600 }}>{tea.name}</div>
                  <div style={{ fontSize: 11, color: "#555" }}>{tea.time} · {tea.role}</div>
                </div>
              </div>
            ))}
          </div>

          {/* Workout */}
          <div style={{ background: card, borderRadius: 16, padding: "14px" }}>
            <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 10 }}>
              <div>
                <div style={{ fontSize: 13, fontWeight: 700, color: "#fb923c" }}>🏋️ Treino de Hoje</div>
                <div style={{ fontSize: 12, color: "#666", marginTop: 2 }}>{workout.focus}</div>
              </div>
              <div style={{ fontSize: 12, color: "#fb923c", fontWeight: 700 }}>{exDoneCount}/{exCount}</div>
            </div>

            {workout.exercises.length === 0 ? (
              <div style={{ color: "#555", fontSize: 13, textAlign: "center", padding: "20px 0" }}>Dia de descanso 💤<br /><span style={{ color: "#444" }}>Caminhada 20–30 min recomendada</span></div>
            ) : (
              <>
                {workout.exercises.map((ex, i) => (
                  <div key={i} onClick={() => toggleExDone(ex.name)}
                    style={{ display: "flex", alignItems: "center", gap: 10, padding: "9px 0", borderBottom: "1px solid #1e1e1e", cursor: "pointer" }}>
                    <div style={{ width: 22, height: 22, borderRadius: 6, border: `2px solid ${exsDone[ex.name] ? "#fb923c" : "#444"}`, background: exsDone[ex.name] ? "#fb923c" : "transparent", display: "flex", alignItems: "center", justifyContent: "center", fontSize: 12, flexShrink: 0 }}>
                      {exsDone[ex.name] ? "✓" : ""}
                    </div>
                    <div style={{ flex: 1 }}>
                      <div style={{ fontSize: 13 }}>{ex.name}</div>
                      <div style={{ fontSize: 11, color: "#555" }}>{ex.sets}x · {ex.reps}</div>
                    </div>
                  </div>
                ))}
                <div style={{ marginTop: 10, background: "#111", borderRadius: 10, padding: "8px 12px" }}>
                  <div style={{ fontSize: 11, color: "#fb923c", fontWeight: 700 }}>🚴 BIKE</div>
                  <div style={{ fontSize: 12, color: "#777", marginTop: 3 }}>{workout.bike}</div>
                </div>
              </>
            )}
          </div>

          {/* Daily macros summary */}
          <div style={{ background: card, borderRadius: 16, padding: "14px" }}>
            <div style={{ fontSize: 13, fontWeight: 700, marginBottom: 12, color: "#fff" }}>📊 Macros do Dia</div>
            <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 10 }}>
              {[
                { label: "Kcal", val: totalKcal, max: 2050, color: accent, unit: "/ 2050" },
                { label: "Proteína", val: totalProt, max: 220, color: "#60a5fa", unit: "/ 220g" },
                { label: "Carb", val: totalCarb, max: 90, color: "#fb923c", unit: "/ 90g" },
                { label: "Gordura", val: totalFat, max: 90, color: "#a78bfa", unit: "/ 90g" },
              ].map(m => (
                <div key={m.label} style={{ background: "#111", borderRadius: 12, padding: "10px 12px" }}>
                  <div style={{ display: "flex", justifyContent: "space-between", marginBottom: 4 }}>
                    <span style={{ fontSize: 12, color: "#666" }}>{m.label}</span>
                    <span style={{ fontSize: 13, fontWeight: 700, color: m.color }}>{m.val} <span style={{ fontSize: 10, color: "#444" }}>{m.unit}</span></span>
                  </div>
                  <div style={{ height: 5, background: "#222", borderRadius: 3 }}>
                    <div style={{ height: 5, background: m.color, borderRadius: 3, width: `${Math.min(m.val / m.max * 100, 100)}%`, transition: "width 0.4s" }} />
                  </div>
                </div>
              ))}
            </div>
          </div>
        </div>
      )}

      {/* ---- SEMANA TAB ---- */}
      {tab === "semana" && (
        <div style={{ padding: "14px" }}>
          <div style={{ fontSize: 16, fontWeight: 800, marginBottom: 12 }}>Últimos 7 dias</div>
          {last7.map(({ key, label, data }) => {
            const w = data.weight;
            const mealsD = data.meals || {};
            const mealsDone = Object.values(mealsD).filter(m => m.done).length;
            const exD = data.exercises || {};
            const dayN = ["Domingo","Segunda","Terça","Quarta","Quinta","Sexta","Sábado"][new Date(key + "T12:00:00").getDay()];
            const wk = WORKOUTS[dayN] || WORKOUTS["Sábado"];
            const exTotal = wk.exercises.length;
            const exDoneC = wk.exercises.filter(e => exD[e.name]).length;
            const isToday = key === todayKey;
            return (
              <div key={key} style={{ background: isToday ? "#1a2e25" : card, border: `1px solid ${isToday ? accent + "55" : "#222"}`, borderRadius: 14, padding: "12px 14px", marginBottom: 10 }}>
                <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center" }}>
                  <div>
                    <div style={{ fontSize: 15, fontWeight: 700 }}>{label} {isToday && <span style={{ fontSize: 11, color: accent }}>· hoje</span>}</div>
                    <div style={{ fontSize: 11, color: "#555" }}>{key}</div>
                  </div>
                  {w && <div style={{ fontSize: 18, fontWeight: 700, color: accent }}>{w} kg</div>}
                </div>
                <div style={{ display: "flex", gap: 8, marginTop: 10 }}>
                  <div style={{ background: "#111", borderRadius: 8, padding: "5px 10px", fontSize: 12 }}>
                    🍽️ {mealsDone}/3 refeições
                  </div>
                  {exTotal > 0 && (
                    <div style={{ background: "#111", borderRadius: 8, padding: "5px 10px", fontSize: 12 }}>
                      🏋️ {exDoneC}/{exTotal}
                    </div>
                  )}
                  <div style={{ background: "#111", borderRadius: 8, padding: "5px 10px", fontSize: 12 }}>
                    💧 {((data.water || 0) * 0.25).toFixed(1)}L
                  </div>
                </div>
                {data.photos?.length > 0 && (
                  <div style={{ display: "flex", gap: 6, marginTop: 8, overflowX: "auto" }}>
                    {data.photos.map((p, i) => (
                      <img key={i} src={p.src} alt={p.label} style={{ height: 60, width: 60, objectFit: "cover", borderRadius: 8, flexShrink: 0, border: "1px solid #333" }} />
                    ))}
                  </div>
                )}
              </div>
            );
          })}

          {/* Weight trend */}
          <div style={{ background: card, borderRadius: 14, padding: "14px", marginTop: 6 }}>
            <div style={{ fontSize: 13, fontWeight: 700, marginBottom: 12, color: accent }}>📉 Evolução do Peso</div>
            <div style={{ display: "flex", alignItems: "flex-end", gap: 4, height: 80 }}>
              {last7.map(({ key, label, data }) => {
                const w = data.weight;
                const h = w ? Math.max(((w - 80) / 30) * 80, 8) : 4;
                return (
                  <div key={key} style={{ flex: 1, display: "flex", flexDirection: "column", alignItems: "center", gap: 3 }}>
                    <div style={{ fontSize: 10, color: accent }}>{w ? w : ""}</div>
                    <div style={{ width: "100%", height: w ? h : 4, background: w ? accent : "#222", borderRadius: 4, transition: "height 0.4s" }} />
                    <div style={{ fontSize: 10, color: "#555" }}>{label}</div>
                  </div>
                );
              })}
            </div>
            <div style={{ marginTop: 12, fontSize: 12, color: "#555", textAlign: "center" }}>Meta: −0,7 a 0,9 kg/semana</div>
          </div>
        </div>
      )}

      {/* ---- FOTOS TAB ---- */}
      {tab === "fotos" && (
        <div style={{ padding: "14px" }}>
          <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 14 }}>
            <div style={{ fontSize: 16, fontWeight: 800 }}>Registro em Fotos</div>
            <button onClick={() => { setPhotoModal("Progresso"); fileRef.current.click(); }}
              style={{ background: accent, color: "#000", border: "none", borderRadius: 10, padding: "8px 14px", fontSize: 13, fontWeight: 700, cursor: "pointer" }}>
              + Adicionar
            </button>
          </div>

          {/* Add photo for meal buttons */}
          <div style={{ background: card, borderRadius: 14, padding: "12px", marginBottom: 14 }}>
            <div style={{ fontSize: 12, color: "#555", marginBottom: 8, fontWeight: 700 }}>FOTO DA REFEIÇÃO (hoje)</div>
            <div style={{ display: "flex", gap: 8, flexWrap: "wrap" }}>
              {mealNames.map(m => (
                <button key={m} onClick={() => { setPhotoModal(m); fileRef.current.click(); }}
                  style={{ padding: "7px 12px", borderRadius: 10, border: "1px solid #333", background: "#111", color: "#888", fontSize: 12, cursor: "pointer" }}>
                  📷 {m}
                </button>
              ))}
            </div>
          </div>

          {/* All photos grouped by day */}
          {Object.entries(allData)
            .filter(([, d]) => d.photos?.length > 0)
            .sort(([a], [b]) => b.localeCompare(a))
            .map(([key, d]) => (
              <div key={key} style={{ marginBottom: 16 }}>
                <div style={{ fontSize: 12, color: "#555", marginBottom: 8, fontWeight: 700 }}>
                  {new Date(key + "T12:00:00").toLocaleDateString("pt-BR", { weekday: "long", day: "2-digit", month: "long" }).toUpperCase()}
                  {d.weight && <span style={{ color: accent, marginLeft: 8 }}>{d.weight} kg</span>}
                </div>
                <div style={{ display: "grid", gridTemplateColumns: "repeat(3, 1fr)", gap: 6 }}>
                  {d.photos.map((p, i) => (
                    <div key={i} style={{ position: "relative", borderRadius: 10, overflow: "hidden", aspectRatio: "1" }}>
                      <img src={p.src} alt={p.label} style={{ width: "100%", height: "100%", objectFit: "cover" }} />
                      <div style={{ position: "absolute", bottom: 0, left: 0, right: 0, background: "rgba(0,0,0,0.7)", padding: "3px 6px", fontSize: 9, color: "#ccc" }}>{p.label}</div>
                    </div>
                  ))}
                </div>
              </div>
            ))
          }
          {!Object.values(allData).some(d => d.photos?.length > 0) && (
            <div style={{ textAlign: "center", padding: "50px 20px", color: "#444" }}>
              <div style={{ fontSize: 40, marginBottom: 12 }}>📷</div>
              <div>Nenhuma foto ainda.</div>
              <div style={{ fontSize: 12, marginTop: 6 }}>Registre suas refeições e progresso!</div>
            </div>
          )}
        </div>
      )}

      {/* Hidden file input */}
      <input ref={fileRef} type="file" accept="image/*" capture="environment" style={{ display: "none" }} onChange={handlePhoto} />
    </div>
  );
}
