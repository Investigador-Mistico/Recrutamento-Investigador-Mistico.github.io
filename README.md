<html><head><base href=""><meta charset="UTF-8"><meta name="viewport" content="width=device-width, initial-scale=1.0"><title>Investigador Místico: Elite Hacker Squad</title><style>
@import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Rajdhani:wght@300;400;700&display=swap');

:root {
  --primary-color: #0a0e17;
  --secondary-color: #1a2130;
  --highlight-color: #00ffff;
  --accent-color: #ff00ff;
  --light-text: #e0e0e0;
  --font-primary: 'Rajdhani', sans-serif;
  --font-secondary: 'Orbitron', sans-serif;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body, html {
  height: 100%;
  font-family: var(--font-primary);
  background: var(--primary-color);
  color: var(--light-text);
  line-height: 1.6;
  overflow-x: hidden;
}

.cyber-grid {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: 
    linear-gradient(to right, rgba(0,255,255,0.05) 1px, transparent 1px),
    linear-gradient(to bottom, rgba(0,255,255,0.05) 1px, transparent 1px);
  background-size: 20px 20px;
  z-index: -1;
  animation: gridPulse 15s infinite linear;
}

@keyframes gridPulse {
  0%, 100% { opacity: 0.2; }
  50% { opacity: 0.8; }
}

header {
  background: rgba(26, 33, 48, 0.8);
  padding: 20px 0;
  text-align: center;
  position: relative;
  backdrop-filter: blur(10px);
}

header::before {
  content: "";
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle, rgba(0,255,255,0.1) 0%, rgba(0,255,255,0) 70%);
  animation: pulse 4s infinite alternate;
}

@keyframes pulse {
  0% { transform: scale(0.8); opacity: 0.5; }
  50% { transform: scale(1.2); opacity: 1; }
  100% { transform: scale(0.8); opacity: 0.5; }
}

header h1 {
  font-size: 3.5rem;
  margin: 0;
  font-family: var(--font-secondary);
  color: var(--highlight-color);
  text-shadow: 0 0 10px var(--highlight-color), 0 0 20px var(--highlight-color);
}

header p {
  font-size: 1.2rem;
  margin: 10px 0 0;
  color: var(--accent-color);
}

nav {
  display: flex;
  justify-content: center;
  margin-top: 20px;
  flex-wrap: wrap;
}

nav a {
  margin: 10px 15px;
  color: var(--light-text);
  text-decoration: none;
  font-size: 1.1rem;
  position: relative;
  overflow: hidden;
  transition: color 0.3s ease;
}

nav a::before {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 2px;
  background-color: var(--highlight-color);
  transform: translateX(-100%);
  transition: transform 0.3s ease;
}

nav a:hover::before {
  transform: translateX(0);
}

nav a:hover {
  color: var(--highlight-color);
  text-shadow: 0 0 5px var(--highlight-color);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 40px 20px;
}

section {
  margin: 60px 0;
  text-align: center;
  position: relative;
}

section::before {
  content: '';
  position: absolute;
  top: -20px;
  left: 50%;
  transform: translateX(-50%);
  width: 50px;
  height: 4px;
  background: var(--highlight-color);
  box-shadow: 0 0 10px var(--highlight-color);
}

section h2 {
  font-size: 2.5rem;
  color: var(--highlight-color);
  margin: 0 0 20px;
  font-family: var(--font-secondary);
  text-transform: uppercase;
  text-shadow: 0 0 10px var(--highlight-color);
}

section p {
  font-size: 1.1rem;
  line-height: 1.8;
  max-width: 800px;
  margin: 0 auto;
}

.tools-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 30px;
  margin-top: 40px;
}

.tool-card {
  background: rgba(26, 33, 48, 0.8);
  padding: 20px;
  border-radius: 10px;
  position: relative;
  overflow: hidden;
  transition: all 0.3s;
  backdrop-filter: blur(5px);
}

.tool-card:hover {
  transform: translateY(-5px) scale(1.05);
  box-shadow: 0 5px 15px rgba(0,255,255,0.3);
}

.tool-card::before {
  content: '';
  position: absolute;
  top: -2px;
  left: -2px;
  right: -2px;
  bottom: -2px;
  background: linear-gradient(45deg, var(--highlight-color), var(--accent-color));
  z-index: -1;
  filter: blur(10px);
  opacity: 0;
  transition: opacity 0.3s;
}

.tool-card:hover::before {
  opacity: 1;
}

.tool-card h3 {
  color: var(--highlight-color);
  font-family: var(--font-secondary);
  font-size: 1.5rem;
}

.tool-card p {
  font-size: 1rem;
  color: var(--light-text);
}

.team-members {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  margin-top: 40px;
}

.team-member {
  flex-basis: calc(25% - 20px);
  margin-bottom: 30px;
  text-align: center;
}

.team-member img {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  border: 3px solid var(--highlight-color);
  transition: all 0.3s;
  box-shadow: 0 0 15px var(--highlight-color);
}

.team-member:hover img {
  transform: scale(1.1) rotate(5deg);
  box-shadow: 0 0 30px var(--highlight-color);
}

.team-member h3 {
  margin-top: 15px;
  color: var(--highlight-color);
  font-family: var(--font-secondary);
}

.team-member p {
  font-size: 0.9rem;
  color: var(--accent-color);
}

.cta {
  background: rgba(26, 33, 48, 0.8);
  padding: 60px 0;
  text-align: center;
  position: relative;
  overflow: hidden;
  backdrop-filter: blur(10px);
}

.cta a {
  background: linear-gradient(45deg, var(--highlight-color), var(--accent-color));
  color: var(--primary-color);
  padding: 15px 30px;
  border: none;
  text-transform: uppercase;
  font-weight: bold;
  font-size: 1.2rem;
  cursor: pointer;
  text-decoration: none;
  display: inline-block;
  border-radius: 5px;
  position: relative;
  transition: all 0.3s;
}

.cta a:hover {
  box-shadow: 0 5px 15px rgba(0,255,255,0.3);
  transform: translateY(-3px) scale(1.05);
}

footer {
  background: rgba(26, 33, 48, 0.8);
  padding: 20px;
  text-align: center;
  backdrop-filter: blur(10px);
}

footer p {
  margin: 0;
  font-size: 0.9rem;
  color: var(--accent-color);
}

#inscricao-modal {
  display: none;
  position: fixed;
  z-index: 1000;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0,0,0,0.8);
  backdrop-filter: blur(5px);
}

.modal-content {
  background: var(--secondary-color);
  margin: 10% auto;
  padding: 20px;
  border: 1px solid var(--highlight-color);
  width: 80%;
  max-width: 600px;
  border-radius: 10px;
  box-shadow: 0 0 20px var(--highlight-color);
}

.close {
  color: var(--accent-color);
  float: right;
  font-size: 28px;
  font-weight: bold;
  cursor: pointer;
}

.close:hover {
  color: var(--highlight-color);
}

form {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

form input, form textarea {
  padding: 10px;
  border: 1px solid var(--highlight-color);
  background: rgba(10, 14, 23, 0.8);
  color: var(--light-text);
  border-radius: 5px;
}

form button {
  background: linear-gradient(45deg, var(--highlight-color), var(--accent-color));
  color: var(--primary-color);
  padding: 10px;
  border: none;
  cursor: pointer;
  font-weight: bold;
  border-radius: 5px;
  transition: all 0.3s;
}

form button:hover {
  transform: translateY(-2px);
  box-shadow: 0 5px 10px rgba(0,255,255,0.2);
}

@media (max-width: 768px) {
  .team-member {
    flex-basis: calc(50% - 20px);
  }

  header h1 {
    font-size: 2.5rem;
  }

  section h2 {
    font-size: 2rem;
  }
}

@media (max-width: 480px) {
  .team-member {
    flex-basis: 100%;
  }

  header h1 {
    font-size: 2rem;
  }

  section h2 {
    font-size: 1.75rem;
  }
}
</style>
</head>
<body>

<div class="cyber-grid"></div>

<header>
  <h1>Investigador Místico</h1>
  <p>Elite Hacker Squad</p>
</header>

<nav>
  <a href="#">Início</a>
  <a href="#">Ferramentas</a>
  <a href="#">Equipe</a>
  <a href="#">Contato</a>
</nav>

<div class="container">
  <section>
    <h2>Bem-vindo ao Futuro da Investigação Digital</h2>
    <p>Mergulhe no universo da cibersegurança avançada e análise de sistemas com o Investigador Místico. Nossa equipe de elite está na vanguarda da tecnologia, explorando as fronteiras entre o real e o virtual para desvendar os mistérios do ciberespaço.</p>
  </section>

  <section>
    <h2>Arsenal Tecnológico</h2>
    <p>Nosso programa utiliza um conjunto sofisticado de ferramentas de última geração para capacitar nossos investigadores:</h2>
    <div class="tools-grid">
      <div class="tool-card">
        <h3>NebulaScan</h3>
        <p>Scanner de vulnerabilidades avançado com IA integrada para análise preditiva de ameaças.</p>
      </div>
      <div class="tool-card">
        <h3>QuantumCrypt</h3>
        <p>Sistema de criptografia quântica para comunicações ultra-seguras e invioláveis.</p>
      </div>
      <div class="tool-card">
        <h3>ShadowTracer</h3>
        <p>Ferramenta de rastreamento digital que mapeia a pegada online de alvos com precisão milimétrica.</p>
      </div>
      <div class="tool-card">
        <h3>MindMesh</h3>
        <p>Plataforma de análise comportamental que utiliza big data para prever padrões de atividade cibernética.</p>
      </div>
    </div>
  </section>

  <section>
    <h2>Elite Hacker Squad</h2>
    <p>Conheça os membros da nossa equipe de elite, liderada pelo lendário Investigador Místico:</p>
    <h2>equipe</h2>
    <div class="team-members">
      <div class="team-member">
        <img src="https://i.im.ge/2024/09/17/fJFQfa.IMG-20240917-WA0674.jpeg" alt="Investigador Místico" width="150" height="150">
        <h3>Investigador Místico</h3>
        <p>Líder e Visionário Sou perito em HTML, C++, CSS, PHP, Java, XML, MySQL, DDoS, Nmap, SQLmap, análise de metadados, engenharia e engenharia reversa</p>
      </div>
      <div class="team-member">
        <img src="https://i.im.ge/2024/09/17/fJufVf.IMG-20240914-WA0158.jpeg" alt="bima" width="150" height="150">
        <h3>Bima</h3>
        <p>Especialista em análise de Metadados, Engenharia Reversa e Engenharia social  Nmap sqlmap </p>
      </div>
      <div class="team-member">
        <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAgGBgcGBQgHBwcJCQgKDBQNDAsLDBkSEw8UHRofHh0aHBwgJC4nICIsIxwcKDcpLDAxNDQ0Hyc5PTgyPC4zNDL/2wBDAQkJCQwLDBgNDRgyIRwhMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjL/wAARCAQAAwADASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwDxakooqhhRRRSGFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUlAC0UlFAC0UlFAC0UlFAC0UUlAC0UUUAFFFFABRRRQAUUUUAFFFJQAtFJRQAtJRRQAtFJRQAtFFJQAtFJRQAtJRRTAWikooAWikopALRSUUALRRRQAUUUUAFFFFABRSUUALRSUUALRSUUALRRRQAUUUUAFFJRQAtFJRQAtFFFABRRSUALRSUtABRRRQAUUUUAFFFJQAtFFFABRRRQAUUUUwFpKKKACiiikAUUUUAFFFFABRRRQAUUUUAFJS0lABRRRQAtJS0lAC0UUUAFJSmkoAKKKKYBRRRQAUUUUAFFFFIBaSlpKACiigUALRRSUALSUGigAooopgFFFFABRRRQAUUUtABSUtJSAKKWkoAKKKKYBRRRQAUUUUAFFFFIAopaSgAooopgFFFFIAooopgFFFFIAooopgFFLSUgCiiimAUUUUAFFFFABRRRQAtJQaKQBRS0lMBaKKKQBSUtFACUUUUwFpKWikAUUUUAFFFFMAooooAKKKKQBRSGigBaKKKACiiimAUUUUgCkpaSgAooooAWkpaSgBaSiigBaKKSgBaSiigBaSiigAooopgFFFFABRRRSAWkoooAWkoooAKKKKYBRRRQAUUUUAFFFFABS0lFAC0UUlIAooopgLSUUUAFFFFABRRRQAUUUUALSUtJSAKKKKYC0lLSUgCilpKAFopDRQAtFFJQAtJS0lAC0lFFMAooooAKKKKACiiigAooooAKKKKQC0UlAoAWiiigApKWkoAWkpaSgBaKKKACiiimAUUUUAFFFFIAooooAKKKKACiiigAooooAKSlooASig0UALSUUUALSUUUALSUtJQAUUtJQAUUtFACUUUUwCiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKAFooopAFFFJQAUUUUwCiiigAooooAKKKWkAUUUUAFFFJQAtFJRQAtFFFABRRRQAUUUlAC0lFFABRRRTAKKKKACiiigAooooAWkoopALSUUUAFFFFMBaKKSkAtFJRQAtJS0lAC0UUUAFFFFMAooooAKKKKQBRRRQAUUUUAFFFFABRRRQAUUUUAFJS0lAC0UUUAFFFFABRRRQAUUUUAFJS0UAJRRRTAKKKKACiiigAopaSkAtJS0YpgFFGKMUAJRS4ooASlxRiigAxRilopAJijFLRTATFGKWigBMUYpaKQCYoxS0UANIxRSmjFMBKKXFGKQBRRijFMApKU0lABS0lFIBaKSigBaSlpKAFopKKAFpKWkoAWiiigBKKDRTAKKKKAFooopAFJS0lAC0lFLQAUUUUAFFFFABRRRQAUlLSUALSUtFABRRRQAUUUUwCiiigAooooAKKKKQBRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRSUtACUUUUwCilFLQA2inUUANop1FIBO1FFFMBaSiigAooooAKKKdQAlFLRSASilooASilooASilooASilooAbRTqKAG0U6k70AFFFFMBKWkooAWiiigBDSU6igBtFOopANop1NoAWkoopgLRSUUgCiiimAtFFJSAWiiigAooooAKKSloAKKKKACiiigAooooAKKKKACiiigAooooAKKKKYBRQaKACiiikAUUUUwCiiikAUUUUwCiiikAUUUUAFFFJQAtFFFABSUtFABRRRQAUUUUALRRRTAKKKKACiiigAopKUdKACiloxQA2lpaTFAC0UUUrgFFFFABRRRQAUUUUgCiiigAooooAKKKKACiiigAooooAMUUUUAFBoopgJ2pKdSUAJS0tFACUUtFACUUvakpgFFFFABRRRQAh6UlOooAbRTqKQCUUUUAFFFFABRRRQAUUlAoAWiiigAooooAKKKKACiiigAooooAKKKKACiiimAtJS0UAJRRRQAUUUUAFFFFABRRRQAUUUUgCiiigAooopgFFFFABRiilpAJilopKYC0UlFAC0UUYpAHNFLRTATFGKWikwExSiiii4C0UlFIBaSilxQAlFLRQAlFLRQAUUUUAFFFFABRiiigAooooAKKKKACiiigAooooAKSlooASilooASilpKACjNLikoAWikooAWkoopgFFFFFwExRS0nemAUUUUAFFFJQAtFFFABSUtGKAEopcUYoASiiikAUUUUAFFFFABRRRQAUUUUwCiiikAUUUUwCiiigBaKKKQCUUUUwCiiigAooooAKKKKACiiigAoopaAEpaKKACiiigAoopaAEopaBSASlpaKAEpaKSkAtJRS0AJS0UYoAKKMUYoAKKWigBKKWigAooooAKKKAKACijFGKACijFGKACijFGKACijFGKACijFGKACijFGKACijFGKACiiigAooooAD0ptOooASilooASilooASjFGKMUAFJS0UAJRRijFAC0UlFAAaTFOop3AbRSnrRTASilpKACiiigBD0opaKAEopaTFABRRiikAUUUUAFFFFMAooooAKKKKACiiigBaKKSkAUUUUwCiiigAooooAKKKWgBO9LRRQAUUUUAFFFLQAlLRS0gEopaKACiijFIBKXFFFABiiijFABRS0UAAooooAKKKMUAFFLiimAlFLRSASlpcUYoAbilpaKAEop1JQAlFOoxQA2inUUANop1FADaKdRQA2inUlACUUtFACUUtFACUU6koAQ0lONJQAlFLRQAlFLijFACUUtJQAUlLRQAlFLRQAlFLijFADTRTqKAEpKU0lAC02lop3ATtRS0UXASilpKYBRRRQAUmKWigBKKMUUAFFFFABRRRQAUUUUAFFFFAC0GiigBKKKKACiiigAxRS0UAFFFFABRRS4oAMUUtGKQBRRRSAKSlooAKKKMUAFFGKWgAxRRRQAUUUoFACUUuKMUAFFKOtGKACgdKWimAmKMUtFACYopaKACkpaKACiijFABRS4pMUDsFGKWlxQFhuKMU7FGKAsNxRinYoxQFhuKMU7FGKAsNxRinYpKAsJRQaMUBYSiloxQKwlFLijFIBKKXFJigAooooAMUYpaKAExSU6kxQAlGKdikoASkpaMUAFFFFACYoxS0UANopTSYoATFGKdikoASilpKAFoNFFMBuKKdikoASilpKYBRRRQAmKMUtFACYopaTvQAUUUUAFFFFAC0UUlABRRRigApaTFLQAUUUuKQCUUuKBQAUtFFFwCijFGKQBRS0YoASlxRiigAooooAKKUUUAJS4op1ADcUo6UtFMAxSYpaKACilooCwlFLRQOwYoxTsUYoCw3FGKWikOwYFGKWigQmKWjrRikAUUYoxRdjEopcUYouxBSUuKMUXYCUUuKMUXYBRRijFF2AlFLijFF2AlFLikxRdgFFLikouMKKKKLiDFGKWii4DMUuKXFGKYWExRinYpMUwsNopcc0UCsJRS4pKACkNLRQAmKKWigBtJTqQ0gEopcUlABRilpKADFJS0YoAKSlooASijFFABSUtFMBtFLRQAlFHeimAUneloxQAlFLikoAKKKKAFooxRikAYopTSUwCiilFABQKWikAUUUCkAUUtGKACkp1JQAdqKKKACilxRigAxRijFLigAFFLiigAoopcUwEopcUDrQFgxRinYoxSHYQDmlopKGAtFFFK4BRRijBouMKXFKBRQAmKMUuKMUrgIBS4FKBS0rgNop2KMUXCw3FGKdijFFwsNxRj2p2KMUXCw3HtRj2p1GKLhYbj2ox7U/8ACjFFx2GY9qTFSYpKLisxuKTFPoouFhmKMU/FJii4WG4pMU8jikxTuAmKTFOxSU7gJRTqbigAopcUmKACiiii4BTcU6immIZilxxTqQimFhtFLijFArCUhFLRQAmKCKWjFIBuKSn4pp60AJRS4ooADSYpaKAEoxS0lACUUtJigAopaSgBMUlOpDTASilx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
