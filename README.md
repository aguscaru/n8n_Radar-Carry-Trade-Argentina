# 🇦🇷 Radar de Carry Trade & Análisis con IA (n8n)

Automatiza el cálculo diario del rendimiento del carry trade en Argentina combinando cotizaciones del Dólar MEP, Tasas de Plazo Fijo (TNA), e Inflación (IPC). Utiliza un modelo de Inteligencia Artificial para redactar un veredicto de mercado y envía alertas inteligentes a Telegram únicamente cuando hay un cambio de signo en la rentabilidad.

---

## 🛠️ Stack Tecnológico
* **n8n:** Orquestador de flujos de automatización.
* **ArgentinaDatos API & DolarAPI:** Fuentes públicas para cotizaciones y variables macroeconómicas.
* **Google Sheets:** Persistencia histórica para comparar contra el valor del día anterior.
* **Basic LLM Chain (Groq / Gemini):** Generación automática del veredicto analítico.
* **Telegram:** Canal de notificaciones y alertas.

---

## 🚀 Cómo Usarlo

1. **Importar el Workflow:**
   * Descarga el archivo `radar-carry.json` de este repositorio.
   * En tu instancia de n8n, ve a los tres puntos (menú superior derecho) y selecciona **Import from File**.
2. **Configurar Credenciales:**
   * Configura tu credencial de API para la IA (Groq o Google Gemini).
   * Vincula tu cuenta de Telegram y completa tu **Chat ID** en el nodo correspondiente.
   * Conecta tu cuenta de Google Sheets y asegúrate de mapear la planilla histórica (`fecha`, `carryUSD`, `signo`).
3. **Activar el Monitoreo:**
   * Configura el *Schedule Trigger* a las 9:00 AM y cambia el workflow a **Active**.
