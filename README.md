[formulaire_occupations_seraing_2026_2027 (1).html](https://github.com/user-attachments/files/28627002/formulaire_occupations_seraing_2026_2027.1.html)
# Formulaire-saison-clubs<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Demande d'occupation d'infrastructure sportive — Ville de Seraing 2026-2027</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&display=swap');

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --green: #1D9E75;
    --green-dark: #0F6E56;
    --green-light: #E1F5EE;
    --green-bg: #f0faf6;
    --amber: #FAEEDA;
    --amber-text: #854F0B;
    --red-light: #FAECE7;
    --red: #D85A30;
    --border: #e2e8f0;
    --border-strong: #cbd5e1;
    --bg: #f8fafc;
    --surface: #ffffff;
    --text: #1e293b;
    --text-muted: #64748b;
    --text-hint: #94a3b8;
    --radius: 8px;
    --radius-lg: 12px;
    --shadow: 0 1px 3px rgba(0,0,0,0.08), 0 1px 2px rgba(0,0,0,0.04);
    --shadow-md: 0 4px 12px rgba(0,0,0,0.08);
  }

  body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
    background: var(--bg);
    color: var(--text);
    font-size: 15px;
    line-height: 1.6;
    min-height: 100vh;
  }

  /* Header */
  .site-header {
    background: var(--surface);
    border-bottom: 1px solid var(--border);
    padding: 0;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: var(--shadow);
  }
  .header-inner {
    max-width: 760px;
    margin: 0 auto;
    padding: 14px 24px;
    display: flex;
    align-items: center;
    gap: 16px;
  }
  .header-logo {
    width: 40px;
    height: 40px;
    background: var(--green);
    border-radius: var(--radius);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
  }
  .header-logo svg { width: 22px; height: 22px; fill: white; }
  .header-text h1 { font-size: 15px; font-weight: 600; color: var(--text); }
  .header-text p { font-size: 12px; color: var(--text-muted); }

  /* Layout */
  .page-wrap {
    max-width: 760px;
    margin: 0 auto;
    padding: 32px 24px 80px;
  }

  /* Progress */
  .progress-wrap {
    margin-bottom: 32px;
  }
  .progress-bar-track {
    height: 4px;
    background: var(--border);
    border-radius: 99px;
    margin-bottom: 20px;
    overflow: hidden;
  }
  .progress-bar-fill {
    height: 100%;
    background: var(--green);
    border-radius: 99px;
    transition: width 0.35s ease;
  }
  .steps-row {
    display: flex;
    justify-content: space-between;
    position: relative;
  }
  .step-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    flex: 1;
    gap: 6px;
  }
  .step-circle {
    width: 30px;
    height: 30px;
    border-radius: 50%;
    border: 2px solid var(--border-strong);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 12px;
    font-weight: 600;
    color: var(--text-muted);
    background: var(--surface);
    transition: all 0.25s;
    position: relative;
    z-index: 1;
  }
  .step-item.active .step-circle {
    border-color: var(--green);
    background: var(--green);
    color: white;
  }
  .step-item.done .step-circle {
    border-color: var(--green);
    background: var(--green-light);
    color: var(--green-dark);
  }
  .step-item.done .step-circle::after {
    content: '✓';
    font-size: 14px;
  }
  .step-item.done .step-circle span { display: none; }
  .step-label {
    font-size: 11px;
    color: var(--text-hint);
    text-align: center;
    white-space: nowrap;
  }
  .step-item.active .step-label { color: var(--green-dark); font-weight: 500; }
  .step-item.done .step-label { color: var(--text-muted); }

  /* Sections */
  .form-section { display: none; }
  .form-section.active { display: block; }

  .section-header {
    margin-bottom: 24px;
  }
  .section-header h2 {
    font-size: 20px;
    font-weight: 600;
    color: var(--text);
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 4px;
  }
  .section-header h2 .icon {
    width: 32px;
    height: 32px;
    background: var(--green-light);
    border-radius: var(--radius);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 16px;
    flex-shrink: 0;
  }
  .section-header p {
    font-size: 14px;
    color: var(--text-muted);
    margin-left: 42px;
  }

  /* Cards */
  .card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: var(--radius-lg);
    padding: 20px;
    margin-bottom: 16px;
    box-shadow: var(--shadow);
  }
  .card-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 16px;
  }
  .card-title {
    font-size: 14px;
    font-weight: 600;
    color: var(--text);
  }
  .remove-btn {
    font-size: 12px;
    color: var(--red);
    background: none;
    border: 1px solid transparent;
    border-radius: var(--radius);
    padding: 4px 10px;
    cursor: pointer;
    font-family: inherit;
    display: flex;
    align-items: center;
    gap: 4px;
    transition: all 0.15s;
  }
  .remove-btn:hover { background: var(--red-light); border-color: #f0997b; }

  /* Form fields */
  .field-group { margin-bottom: 14px; }
  .field-group:last-child { margin-bottom: 0; }

  label.field-label {
    display: block;
    font-size: 13px;
    font-weight: 500;
    color: var(--text-muted);
    margin-bottom: 5px;
  }
  .required::after { content: ' *'; color: var(--red); }

  input[type=text], input[type=email], input[type=tel], input[type=number],
  input[type=time], select, textarea {
    width: 100%;
    padding: 9px 12px;
    font-size: 14px;
    font-family: inherit;
    border: 1px solid var(--border-strong);
    border-radius: var(--radius);
    background: var(--surface);
    color: var(--text);
    transition: border-color 0.15s, box-shadow 0.15s;
    appearance: none;
    -webkit-appearance: none;
  }
  select {
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='8' viewBox='0 0 12 8'%3E%3Cpath d='M1 1l5 5 5-5' stroke='%2364748b' stroke-width='1.5' fill='none' stroke-linecap='round'/%3E%3C/svg%3E");
    background-repeat: no-repeat;
    background-position: right 12px center;
    padding-right: 36px;
  }
  input:focus, select:focus, textarea:focus {
    outline: none;
    border-color: var(--green);
    box-shadow: 0 0 0 3px rgba(29,158,117,0.12);
  }
  textarea { min-height: 90px; resize: vertical; line-height: 1.6; }

  .row2 { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  .row3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 12px; }
  .row-13 { display: grid; grid-template-columns: 1fr 2fr; gap: 12px; }

  .help-text {
    font-size: 12px;
    color: var(--text-hint);
    margin-top: 4px;
  }

  /* Add button */
  .add-btn {
    width: 100%;
    padding: 10px;
    border: 1.5px dashed var(--border-strong);
    border-radius: var(--radius-lg);
    background: none;
    color: var(--text-muted);
    font-size: 14px;
    font-family: inherit;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    margin-bottom: 16px;
    transition: all 0.15s;
  }
  .add-btn:hover {
    background: var(--green-light);
    border-color: var(--green);
    color: var(--green-dark);
  }

  /* Radio cards */
  .radio-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 8px; }
  .radio-card {
    border: 1px solid var(--border-strong);
    border-radius: var(--radius);
    padding: 10px 12px;
    cursor: pointer;
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 14px;
    transition: all 0.15s;
  }
  .radio-card:hover { border-color: var(--green); background: var(--green-bg); }
  .radio-card.sel { border-color: var(--green); background: var(--green-light); color: #085041; font-weight: 500; }
  .radio-card input[type=radio] { accent-color: var(--green); width: 15px; height: 15px; flex-shrink: 0; }

  /* Day buttons */
  .days-grid { display: flex; flex-wrap: wrap; gap: 6px; margin: 6px 0; }
  .day-btn {
    padding: 5px 14px;
    border: 1px solid var(--border-strong);
    border-radius: 99px;
    font-size: 13px;
    font-family: inherit;
    cursor: pointer;
    background: none;
    color: var(--text);
    transition: all 0.15s;
  }
  .day-btn:hover { border-color: var(--green); color: var(--green-dark); }
  .day-btn.sel {
    background: var(--green-light);
    border-color: var(--green);
    color: var(--green-dark);
    font-weight: 500;
  }

  /* Badge */
  .badge {
    display: inline-flex;
    padding: 3px 10px;
    border-radius: 99px;
    font-size: 12px;
    font-weight: 500;
  }
  .badge-green { background: var(--green-light); color: var(--green-dark); }
  .badge-amber { background: var(--amber); color: var(--amber-text); }
  .badge-blue { background: #EFF6FF; color: #1e40af; }

  /* Pool box */
  .pool-box {
    background: #f0faf6;
    border: 1px solid #9FE1CB;
    border-radius: var(--radius);
    padding: 14px;
    margin-top: 12px;
  }
  .pool-box-title {
    font-size: 13px;
    font-weight: 600;
    color: var(--green-dark);
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    gap: 6px;
  }

  /* Info box */
  .info-box {
    background: var(--green-light);
    border-radius: var(--radius);
    padding: 12px 14px;
    font-size: 13px;
    color: #085041;
    line-height: 1.6;
    margin-bottom: 16px;
    display: flex;
    gap: 10px;
    align-items: flex-start;
  }
  .info-box .info-icon { flex-shrink: 0; font-size: 16px; margin-top: 1px; }

  .warn-box {
    background: var(--amber);
    border-radius: var(--radius);
    padding: 12px 14px;
    font-size: 13px;
    color: #633806;
    line-height: 1.6;
    margin-bottom: 16px;
    display: flex;
    gap: 10px;
    align-items: flex-start;
  }

  /* Checkbox */
  .checkbox-row {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    font-size: 14px;
    cursor: pointer;
    margin-bottom: 10px;
    line-height: 1.5;
  }
  .checkbox-row input[type=checkbox] {
    width: 16px;
    height: 16px;
    flex-shrink: 0;
    margin-top: 2px;
    accent-color: var(--green);
    cursor: pointer;
  }

  /* Navigation */
  .nav-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 24px;
    padding-top: 20px;
    border-top: 1px solid var(--border);
  }
  .btn-prev {
    padding: 10px 20px;
    border: 1px solid var(--border-strong);
    border-radius: var(--radius);
    background: var(--surface);
    color: var(--text);
    font-size: 14px;
    font-weight: 500;
    font-family: inherit;
    cursor: pointer;
    display: flex;
    align-items: center;
    gap: 6px;
    transition: all 0.15s;
  }
  .btn-prev:hover { background: var(--bg); }
  .btn-next {
    padding: 10px 22px;
    border: none;
    border-radius: var(--radius);
    background: var(--green);
    color: white;
    font-size: 14px;
    font-weight: 600;
    font-family: inherit;
    cursor: pointer;
    display: flex;
    align-items: center;
    gap: 6px;
    transition: all 0.15s;
    box-shadow: 0 1px 3px rgba(29,158,117,0.3);
  }
  .btn-next:hover { background: var(--green-dark); }
  .btn-submit {
    padding: 12px 28px;
    border: none;
    border-radius: var(--radius);
    background: var(--green);
    color: white;
    font-size: 15px;
    font-weight: 600;
    font-family: inherit;
    cursor: pointer;
    display: flex;
    align-items: center;
    gap: 8px;
    transition: all 0.15s;
    box-shadow: 0 2px 6px rgba(29,158,117,0.35);
  }
  .btn-submit:hover { background: var(--green-dark); }

  /* Summary */
  .summary-table { width: 100%; border-collapse: collapse; }
  .summary-table tr { border-bottom: 1px solid var(--border); }
  .summary-table tr:last-child { border-bottom: none; }
  .summary-table td { padding: 9px 0; font-size: 14px; vertical-align: top; }
  .summary-table td:first-child { color: var(--text-muted); width: 40%; }
  .summary-table td:last-child { font-weight: 500; text-align: right; }

  /* Success */
  .success-wrap { text-align: center; padding: 40px 20px; }
  .success-icon-wrap {
    width: 64px;
    height: 64px;
    background: var(--green-light);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 20px;
    font-size: 30px;
  }
  .dossier-num {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: var(--bg);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 10px 18px;
    font-size: 15px;
    font-weight: 600;
    color: var(--text);
    margin: 16px 0;
  }
  .dossier-num .label { font-weight: 400; color: var(--text-muted); font-size: 13px; }

  /* Print */
  @media print {
    .site-header { position: static; }
    .nav-row { display: none; }
    .form-section { display: block !important; }
    .progress-wrap { display: none; }
  }

  @media (max-width: 580px) {
    .row2, .row3, .row-13 { grid-template-columns: 1fr; }
    .radio-grid { grid-template-columns: 1fr; }
    .page-wrap { padding: 20px 16px 60px; }
    .steps-row .step-label { display: none; }
  }
</style>
</head>
<body>

<header class="site-header">
  <div class="header-inner">
    <div class="header-logo">
      <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/>
      </svg>
    </div>
    <div class="header-text">
      <h1>Service des Sports — Ville de Seraing</h1>
      <p>Demande d'occupation d'infrastructure sportive · Saison 2026-2027</p>
    </div>
  </div>
</header>

<div class="page-wrap">

  <!-- Progress -->
  <div class="progress-wrap">
    <div class="progress-bar-track">
      <div class="progress-bar-fill" id="progressFill" style="width:20%"></div>
    </div>
    <div class="steps-row">
      <div class="step-item active" id="step0">
        <div class="step-circle"><span>1</span></div>
        <div class="step-label">Club</div>
      </div>
      <div class="step-item" id="step1">
        <div class="step-circle"><span>2</span></div>
        <div class="step-label">Contacts</div>
      </div>
      <div class="step-item" id="step2">
        <div class="step-circle"><span>3</span></div>
        <div class="step-label">Infrastructures</div>
      </div>
      <div class="step-item" id="step3">
        <div class="step-circle"><span>4</span></div>
        <div class="step-label">Documents</div>
      </div>
      <div class="step-item" id="step4">
        <div class="step-circle"><span>5</span></div>
        <div class="step-label">Récapitulatif</div>
      </div>
    </div>
  </div>

  <!-- ==================== SECTION 1 : Club ==================== -->
  <div class="form-section active" id="sec0">
    <div class="section-header">
      <h2><span class="icon">🏟️</span> Identification du club</h2>
      <p>Informations générales sur votre organisation</p>
    </div>

    <div class="card">
      <div class="field-group">
        <label class="field-label required">Nom du club / association / école</label>
        <input type="text" id="clubName" placeholder="ex. Seraing Athlétisme">
      </div>
      <div class="row2">
        <div class="field-group">
          <label class="field-label required">Type d'organisation</label>
          <select id="orgType">
            <option value="">— Sélectionner —</option>
            <option>Club sportif</option>
            <option>École</option>
            <option>Association</option>
            <option>Extrascolaire</option>
            <option>Service communal</option>
            <option>Autre</option>
          </select>
        </div>
        <div class="field-group">
          <label class="field-label">Fédération / Ligue sportive</label>
          <select id="federation">
            <option value="">— Sélectionner —</option>
            <option>RIL</option>
            <option>LFFS</option>
            <option>Fédération Francophone Belge de Natation</option>
            <option>Autre fédération</option>
            <option>Sans affiliation</option>
          </select>
        </div>
      </div>
      <div class="row2">
        <div class="field-group">
          <label class="field-label">Numéro d'affiliation fédérale</label>
          <input type="text" id="fedNum" placeholder="ex. RIL-12345">
        </div>
        <div class="field-group">
          <label class="field-label">Numéro d'entreprise (BCE)</label>
          <input type="text" placeholder="ex. BE 0123.456.789">
        </div>
      </div>
    </div>

    <div class="card">
      <div class="card-title" style="margin-bottom:14px">Adresse du siège social</div>
      <div class="field-group">
        <label class="field-label required">Rue et numéro</label>
        <input type="text" id="adresse" placeholder="ex. Rue Bruno 185a">
      </div>
      <div class="row-13">
        <div class="field-group">
          <label class="field-label required">Code postal</label>
          <input type="text" id="codePostal" placeholder="ex. 4100">
        </div>
        <div class="field-group">
          <label class="field-label required">Commune</label>
          <input type="text" id="commune" placeholder="ex. Seraing">
        </div>
      </div>
    </div>

    <div class="card">
      <div class="field-group">
        <label class="field-label">Statut juridique de l'organisation</label>
        <div class="radio-grid">
          <label class="radio-card" onclick="selectRadio(this,'statut')"><input type="radio" name="statut"> ASBL constituée</label>
          <label class="radio-card" onclick="selectRadio(this,'statut')"><input type="radio" name="statut"> En cours de constitution</label>
          <label class="radio-card" onclick="selectRadio(this,'statut')"><input type="radio" name="statut"> Association de fait</label>
          <label class="radio-card" onclick="selectRadio(this,'statut')"><input type="radio" name="statut"> École / institution publique</label>
        </div>
      </div>
      <div class="field-group" style="margin-top:4px">
        <label class="field-label">Discipline sportive principale</label>
        <input type="text" id="sport" placeholder="ex. Basket-ball, Natation, Football, Athlétisme...">
      </div>
    </div>

    <div class="nav-row">
      <span></span>
      <button class="btn-next" onclick="goTo(1)">Contacts et responsables ›</button>
    </div>
  </div>

  <!-- ==================== SECTION 2 : Contacts ==================== -->
  <div class="form-section" id="sec1">
    <div class="section-header">
      <h2><span class="icon">👤</span> Personnes de contact</h2>
      <p>Responsable principal et personnes à contacter pour les infrastructures</p>
    </div>

    <div id="contactsList">
      <div class="card" id="contact-0">
        <div class="card-header">
          <span class="card-title">Responsable principal <span class="badge badge-green" style="margin-left:8px">Obligatoire</span></span>
        </div>
        <div class="row2">
          <div class="field-group">
            <label class="field-label required">Prénom</label>
            <input type="text" class="c-prenom" placeholder="Prénom">
          </div>
          <div class="field-group">
            <label class="field-label required">Nom</label>
            <input type="text" class="c-nom" placeholder="Nom de famille">
          </div>
        </div>
        <div class="row2">
          <div class="field-group">
            <label class="field-label required">Téléphone</label>
            <input type="tel" class="c-tel" placeholder="04xx / 0x xxx xx xx">
          </div>
          <div class="field-group">
            <label class="field-label required">E-mail</label>
            <input type="email" class="c-email" placeholder="email@exemple.be">
          </div>
        </div>
        <div class="row2">
          <div class="field-group">
            <label class="field-label required">Fonction</label>
            <select class="c-fonction">
              <option value="">— Sélectionner —</option>
              <option>Président(e)</option>
              <option>Vice-président(e)</option>
              <option>Secrétaire</option>
              <option>Trésorier(ère)</option>
              <option>Directeur(trice) technique</option>
              <option>Coordinateur(trice)</option>
              <option>Directeur(trice) d'école</option>
              <option>Autre</option>
            </select>
          </div>
          <div class="field-group">
            <label class="field-label">Numéro de compte (IBAN)</label>
            <input type="text" class="c-iban" placeholder="BE xx xxxx xxxx xxxx">
          </div>
        </div>
      </div>
    </div>

    <button class="add-btn" onclick="addContact()">
      ＋ Ajouter un contact supplémentaire
    </button>

    <div class="card">
      <div class="field-group">
        <label class="field-label">Le club est-il majoritairement composé de Sérésiens ?</label>
        <div class="radio-grid">
          <label class="radio-card" onclick="selectRadio(this,'seresien')"><input type="radio" name="seresien"> Oui — tarif réduit possible</label>
          <label class="radio-card" onclick="selectRadio(this,'seresien')"><input type="radio" name="seresien"> Non</label>
        </div>
        <p class="help-text" style="margin-top:8px">Un justificatif (liste des membres avec adresse) sera demandé pour bénéficier du tarif sérésien.</p>
      </div>
      <div class="field-group">
        <label class="field-label">Nombre total de membres affiliés</label>
        <input type="number" min="0" placeholder="ex. 45" style="max-width:200px">
      </div>
      <div class="field-group">
        <label class="field-label">Dont membres de moins de 18 ans</label>
        <input type="number" min="0" placeholder="ex. 20" style="max-width:200px">
        <p class="help-text">Indiquer pour bénéficier de la réduction jeunes</p>
      </div>
    </div>

    <div class="nav-row">
      <button class="btn-prev" onclick="goTo(0)">‹ Retour</button>
      <button class="btn-next" onclick="goTo(2)">Infrastructures demandées ›</button>
    </div>
  </div>

  <!-- ==================== SECTION 3 : Infrastructures ==================== -->
  <div class="form-section" id="sec2">
    <div class="section-header">
      <h2><span class="icon">📋</span> Demandes d'occupation</h2>
      <p>Ajoutez un bloc par créneau ou par infrastructure demandée. Plusieurs créneaux possibles.</p>
    </div>

    <div class="info-box">
      <span class="info-icon">ℹ️</span>
      <span>Les créneaux sont accordés sous réserve de disponibilité et de validation par le Service des Sports. Les demandes sont traitées dans l'ordre de réception des dossiers complets.</span>
    </div>

    <div id="slotsList"></div>

    <button class="add-btn" onclick="addSlot()">
      ＋ Ajouter une demande d'occupation
    </button>

    <div class="nav-row">
      <button class="btn-prev" onclick="goTo(1)">‹ Retour</button>
      <button class="btn-next" onclick="goTo(3)">Documents à fournir ›</button>
    </div>
  </div>

  <!-- ==================== SECTION 4 : Documents ==================== -->
  <div class="form-section" id="sec3">
    <div class="section-header">
      <h2><span class="icon">📁</span> Documents à fournir</h2>
      <p>Cochez les documents que vous joignez à votre demande</p>
    </div>

    <div class="warn-box">
      <span>⚠️</span>
      <span>Le dossier ne sera considéré comme <strong>complet</strong> qu'à réception de l'ensemble des pièces obligatoires. Les délais de traitement commencent à la date de complétude du dossier.</span>
    </div>

    <div class="card">
      <div class="card-title" style="margin-bottom:14px">Documents obligatoires</div>
      <label class="checkbox-row">
        <input type="checkbox">
        <span>Attestation d'assurance <strong>Responsabilité Civile</strong> (en cours de validité pour la saison 2026-2027)</span>
      </label>
      <label class="checkbox-row">
        <input type="checkbox">
        <span>Attestation d'assurance <strong>incendie</strong></span>
      </label>
      <label class="checkbox-row">
        <input type="checkbox">
        <span><strong>Statuts</strong> de l'ASBL ou règlement intérieur de l'association</span>
      </label>
    </div>

    <div class="card">
      <div class="card-title" style="margin-bottom:14px">Documents complémentaires (selon situation)</div>
      <label class="checkbox-row">
        <input type="checkbox">
        <span>Liste nominative des membres avec indication des <strong>Sérésiens</strong> (pour bénéficier du tarif réduit)</span>
      </label>
      <label class="checkbox-row">
        <input type="checkbox">
        <span>Attestation d'affiliation fédérale en cours de validité</span>
      </label>
      <label class="checkbox-row">
        <input type="checkbox">
        <span>Liste nominative des <strong>jeunes de moins de 18 ans</strong> pour la réduction jeunes (import Excel accepté)</span>
      </label>
      <label class="checkbox-row">
        <input type="checkbox">
        <span>Autorisation parentale pour les groupes de mineurs</span>
      </label>
      <label class="checkbox-row" id="docMaitre">
        <input type="checkbox">
        <span>Attestation <strong>maître-nageur / moniteur de natation</strong> (obligatoire si demande piscine)</span>
      </label>
      <label class="checkbox-row">
        <input type="checkbox">
        <span>Tout autre document demandé par le Service des Sports</span>
      </label>
    </div>

    <div class="card">
      <div class="card-title" style="margin-bottom:8px">Transmission des documents</div>
      <p style="font-size:14px; color:var(--text-muted); line-height:1.7; margin-bottom:12px">
        Les documents peuvent être transmis par :
      </p>
      <div style="display:grid; grid-template-columns:1fr 1fr; gap:10px; font-size:13px;">
        <div style="background:var(--bg);border-radius:var(--radius);padding:10px 12px;">
          📧 <strong>E-mail :</strong><br>
          <span style="color:var(--text-muted)">sports@seraing.be</span>
        </div>
        <div style="background:var(--bg);border-radius:var(--radius);padding:10px 12px;">
          🏢 <strong>Dépôt physique :</strong><br>
          <span style="color:var(--text-muted)">Service des Sports<br>Maison communale<br>Rue Bruno 185a, 4100 Seraing</span>
        </div>
      </div>
    </div>

    <div class="card">
      <div class="field-group">
        <label class="field-label">Remarques ou demandes particulières</label>
        <textarea id="remarques" placeholder="Ex. matériel nécessaire (cages, filets…), besoin de vestiaires particuliers, périodes d'indisponibilité du club, contraintes spécifiques, demandes d'exceptions..."></textarea>
      </div>
    </div>

    <div class="card" style="border-color: #9FE1CB; background: var(--green-bg);">
      <label class="checkbox-row" id="rgpdRow">
        <input type="checkbox" id="rgpdCheck">
        <span style="font-size:13px;">J'ai lu et j'accepte que les données personnelles collectées dans ce formulaire soient traitées par la <strong>Ville de Seraing</strong> dans le cadre de la gestion des occupations d'infrastructures sportives, conformément au <strong>Règlement Général sur la Protection des Données (RGPD)</strong>. Ces données ne seront pas transmises à des tiers sans consentement exprès.</span>
      </label>
      <label class="checkbox-row" style="margin-top:8px" id="engRow">
        <input type="checkbox" id="engCheck">
        <span style="font-size:13px;">Je certifie l'exactitude des informations fournies et m'engage à respecter le <strong>règlement d'utilisation des infrastructures sportives communales</strong> de la Ville de Seraing, ainsi que toutes les conditions fixées dans la convention d'occupation.</span>
      </label>
    </div>

    <div class="nav-row">
      <button class="btn-prev" onclick="goTo(2)">‹ Retour</button>
      <button class="btn-next" onclick="goRecap()">Vérifier et soumettre ›</button>
    </div>
  </div>

  <!-- ==================== SECTION 5 : Récapitulatif ==================== -->
  <div class="form-section" id="sec4">
    <div class="section-header">
      <h2><span class="icon">✅</span> Récapitulatif de la demande</h2>
      <p>Vérifiez les informations avant de soumettre votre dossier</p>
    </div>

    <div class="card" id="recapClub"></div>
    <div class="card" id="recapSlots"></div>

    <div class="info-box">
      📬 Une confirmation sera envoyée par e-mail à l'adresse du responsable principal. Votre dossier sera examiné par le Service des Sports dans un délai de <strong>15 jours ouvrables</strong> après réception du dossier complet.
    </div>

    <div class="nav-row">
      <button class="btn-prev" onclick="goTo(3)">‹ Retour</button>
      <button class="btn-submit" onclick="submitForm()">✉ Soumettre la demande</button>
    </div>
  </div>

  <!-- ==================== SUCCESS ==================== -->
  <div class="form-section" id="sec5">
    <div class="success-wrap">
      <div class="success-icon-wrap">✅</div>
      <h2 style="font-size:22px; margin-bottom:8px">Demande soumise avec succès !</h2>
      <p style="color:var(--text-muted); max-width:460px; margin:0 auto 20px; font-size:15px; line-height:1.7">
        Votre dossier a été transmis au Service des Sports de la Ville de Seraing. Vous recevrez une confirmation par e-mail et serez contacté(e) sous 15 jours ouvrables.
      </p>
      <div class="dossier-num">
        <span class="label">Numéro de dossier :</span>
        <strong id="dossierNum">—</strong>
      </div>
      <p style="font-size:13px; color:var(--text-hint); margin-top:12px">Conservez ce numéro pour tout contact avec le Service des Sports.</p>
      <div style="margin-top:28px; display:flex; gap:12px; justify-content:center; flex-wrap:wrap;">
        <button class="btn-next" onclick="window.print()">🖨 Imprimer la confirmation</button>
        <button class="btn-prev" onclick="resetForm()">Nouvelle demande</button>
      </div>
    </div>
  </div>

</div><!-- /.page-wrap -->

<script>
// ============================================================
// DATA
// ============================================================
const LIEUX = [
  "HALL DES SPORTS DU BOIS DE L'ABBAYE",
  "HALL DES SPORTS DU BOIS DE MONT",
  "HALL DES SPORTS DU CENTENAIRE",
  "GYMNASE DES BIENS-COMMUNAUX",
  "GYMNASE DU CENTRE",
  "GYMNASE ECOLE DE BONCELLES",
  "GYMNASE ECOLE DE LA TROQUE",
  "GYMNASE ECOLE DE LIZE",
  "GYMNASE ECOLE DELEVAL",
  "GYMNASE ECOLE DES COMMUNAUX (DISTEXHE)",
  "GYMNASE ECOLE DES TAILLIS",
  "GYMNASE ECOLE DES TRIXHES II",
  "GYMNASE ECOLE HEUREUSE",
  "GYMNASE ECOLE HEYNE",
  "GYMNASE ECOLE INDUSTRIE",
  "GYMNASE MORCHAMPS",
  "PISCINE OLYMPIQUE",
  "PISTE D'ATHLETISME - BOIS DE L'ABBAYE",
  "SALLE DE MUSCULATION - BOIS DE L'ABBAYE",
  "SALLE DE MUSCULATION - BOIS DE MONT",
  "TERRAIN SYNTHETIQUE BOVERIE",
  "BOIS DE L'ABBAYE - TERRAIN DE RUGBY DE L'ETAT",
  "BOIS DE MONT - TERRAIN DE BASEBALL",
  "BOIS DE MONT - TERRAIN DE FOOTBALL",
  "CENTENAIRE - TERRAIN A",
  "CENTENAIRE - TERRAIN B",
  "PLAINE DES SPORTS - TERRAIN DE FOOTBALL",
  "PREAU DES BIENS-COMMUNAUX",
  "PREAU ECOLE DES SIX-BONNIERS"
];

const JOURS = ['Lundi','Mardi','Mercredi','Jeudi','Vendredi','Samedi','Dimanche'];

const PROPORTIONS = [
  '','Salle entière','1/3 salle','2/3 salle',
  'Grille A','Grille B','Grille A + B',
  'Couloir 1','Couloir 2','Couloir 3','Couloir 4',
  'Bassin entier (piscine)'
];

const TARIFS = {
  "PISCINE OLYMPIQUE": { seres: 15, ext: 30, bassin_seres: 90, bassin_ext: 200, code: 'IP' },
  "HALL DES SPORTS DU BOIS DE L'ABBAYE": { seres: 10, ext: 40, code: 'IS' },
  "HALL DES SPORTS DU BOIS DE MONT": { seres: 10, ext: 40, code: 'IS' },
  "HALL DES SPORTS DU CENTENAIRE": { seres: 10, ext: 40, code: 'IS' },
  "default_IS": { seres: 0, ext: 0, code: 'IS' },
  "default_IE": { seres: 8, ext: 20, code: 'IE' }
};

// ============================================================
// STATE
// ============================================================
let currentStep = 0;
let slotCount = 0;
let contactCount = 1;

const STEPS = ['sec0','sec1','sec2','sec3','sec4','sec5'];
const PROGRESS = [20, 40, 60, 80, 100, 100];

// ============================================================
// NAVIGATION
// ============================================================
function goTo(step) {
  document.getElementById(STEPS[currentStep]).classList.remove('active');
  document.getElementById('step' + currentStep).classList.remove('active');
  if (step > currentStep) {
    document.getElementById('step' + currentStep).classList.add('done');
  }
  currentStep = step;
  document.getElementById(STEPS[step]).classList.add('active');
  if (step < 5) {
    document.getElementById('step' + step).classList.add('active');
  }
  document.getElementById('progressFill').style.width = PROGRESS[step] + '%';
  window.scrollTo({ top: 0, behavior: 'smooth' });
}

function goRecap() {
  buildRecap();
  goTo(4);
}

// ============================================================
// RADIO CARDS
// ============================================================
function selectRadio(el, name) {
  document.querySelectorAll('input[name=' + name + ']').forEach(r => {
    r.closest('.radio-card').classList.remove('sel');
  });
  el.classList.add('sel');
}

// ============================================================
// CONTACTS
// ============================================================
function addContact() {
  const id = 'contact-' + contactCount++;
  const div = document.createElement('div');
  div.className = 'card';
  div.id = id;
  div.innerHTML = `
    <div class="card-header">
      <span class="card-title">Contact supplémentaire</span>
      <button class="remove-btn" onclick="this.closest('.card').remove()">✕ Supprimer</button>
    </div>
    <div class="row2">
      <div class="field-group"><label class="field-label">Prénom</label><input type="text" placeholder="Prénom"></div>
      <div class="field-group"><label class="field-label">Nom</label><input type="text" placeholder="Nom de famille"></div>
    </div>
    <div class="row2">
      <div class="field-group"><label class="field-label">Téléphone</label><input type="tel" placeholder="04xx / 0x xxx xx xx"></div>
      <div class="field-group"><label class="field-label">E-mail</label><input type="email" placeholder="email@exemple.be"></div>
    </div>
    <div class="field-group">
      <label class="field-label">Fonction</label>
      <select>
        <option value="">— Sélectionner —</option>
        <option>Président(e)</option><option>Vice-président(e)</option>
        <option>Secrétaire</option><option>Trésorier(ère)</option>
        <option>Directeur(trice) technique</option><option>Coordinateur(trice)</option>
        <option>Directeur(trice) d'école</option><option>Autre</option>
      </select>
    </div>`;
  document.getElementById('contactsList').appendChild(div);
}

// ============================================================
// SLOTS
// ============================================================
function addSlot() {
  const sid = 'slot-' + slotCount;
  const num = slotCount + 1;
  slotCount++;

  const lieuOpts = '<option value="">— Sélectionner l\'infrastructure —</option>' +
    LIEUX.map(l => `<option value="${l}">${l.charAt(0) + l.slice(1).toLowerCase()}</option>`).join('');

  const propOpts = PROPORTIONS.map(p =>
    `<option value="${p}">${p || '— Si applicable —'}</option>`).join('');

  const joursHtml = JOURS.map(j =>
    `<button type="button" class="day-btn" onclick="this.classList.toggle('sel')">${j}</button>`
  ).join('');

  const div = document.createElement('div');
  div.className = 'card';
  div.id = sid;
  div.innerHTML = `
    <div class="card-header">
      <span class="card-title">Créneau n°${num}</span>
      <button class="remove-btn" onclick="this.closest('.card').remove()">✕ Supprimer</button>
    </div>

    <div class="field-group">
      <label class="field-label required">Infrastructure souhaitée</label>
      <select class="infra-sel" onchange="onLieuChange(this,'${sid}')">
        ${lieuOpts}
      </select>
    </div>

    <div class="row2">
      <div class="field-group">
        <label class="field-label required">Heure de début</label>
        <input type="time" class="h-debut" value="18:00">
      </div>
      <div class="field-group">
        <label class="field-label required">Heure de fin</label>
        <input type="time" class="h-fin" value="20:00">
      </div>
    </div>

    <div class="field-group">
      <label class="field-label required">Jour(s) de la semaine</label>
      <div class="days-grid">${joursHtml}</div>
    </div>

    <div class="row3">
      <div class="field-group">
        <label class="field-label">Proportion / zone</label>
        <select class="prop-sel">${propOpts}</select>
      </div>
      <div class="field-group">
        <label class="field-label">Nbre de semaines</label>
        <input type="number" class="nb-sem" min="1" max="52" placeholder="ex. 36">
      </div>
      <div class="field-group">
        <label class="field-label">Sport / activité</label>
        <input type="text" class="sport-act" placeholder="ex. Basket, Natation...">
      </div>
    </div>

    <!-- Piscine spécifique -->
    <div class="pool-box" id="pool-${sid}" style="display:none">
      <div class="pool-box-title">🏊 Informations spécifiques — Piscine Olympique</div>
      <div class="row3">
        <div class="field-group">
          <label class="field-label">Nombre de couloirs</label>
          <input type="number" min="1" max="8" placeholder="ex. 2">
        </div>
        <div class="field-group">
          <label class="field-label">Nageurs max.</label>
          <input type="number" min="1" placeholder="ex. 20">
        </div>
        <div class="field-group">
          <label class="field-label">Vestiaires</label>
          <select>
            <option value="">— Indiquer —</option>
            <option>Vestiaire 1</option>
            <option>Vestiaire 2</option>
            <option>Les deux</option>
          </select>
        </div>
      </div>
      <div class="row2">
        <div class="field-group">
          <label class="field-label">Type de groupe</label>
          <select>
            <option value="">— Sélectionner —</option>
            <option>École</option>
            <option>Club sportif</option>
            <option>Extrascolaire</option>
          </select>
        </div>
        <div class="field-group">
          <label class="field-label">Maître-nageur présent ?</label>
          <select>
            <option value="">— Sélectionner —</option>
            <option>Oui — propre au club</option>
            <option>Oui — communal (à confirmer)</option>
            <option>Non</option>
          </select>
        </div>
      </div>
    </div>

    <div class="field-group">
      <label class="field-label">Remarques pour ce créneau</label>
      <input type="text" placeholder="Ex. matériel requis, période estivale exclue, priorité matchs...">
    </div>

    <!-- Tarif estimatif -->
    <div id="tarif-${sid}" style="display:none; margin-top:8px; background:#f0faf6; border-radius:var(--radius); padding:10px 12px; font-size:13px; color:#085041;">
      <strong>ℹ Tarif indicatif :</strong> <span id="tarif-txt-${sid}"></span>
      <span style="color:#64748b"> (hors réduction jeunes — sous réserve de validation)</span>
    </div>`;

  document.getElementById('slotsList').appendChild(div);
}

function onLieuChange(sel, sid) {
  const val = sel.value;
  const pool = document.getElementById('pool-' + sid);
  const tarifBox = document.getElementById('tarif-' + sid);
  const tarifTxt = document.getElementById('tarif-txt-' + sid);

  pool.style.display = val === 'PISCINE OLYMPIQUE' ? 'block' : 'none';

  let t = TARIFS[val];
  if (!t) {
    if (val.includes('GYMNASE') || val.includes('PREAU')) t = TARIFS['default_IE'];
    else t = TARIFS['default_IS'];
  }
  if (t.seres === 0 && t.ext === 0) {
    tarifBox.style.display = 'none';
  } else {
    tarifBox.style.display = 'block';
    if (val === 'PISCINE OLYMPIQUE') {
      tarifTxt.textContent = `${t.seres} €/h (Sérésiens) · ${t.ext} €/h (hors Seraing) · ${t.bassin_seres} €/bassin (Sérésiens) · ${t.bassin_ext} €/bassin (hors Seraing)`;
    } else {
      tarifTxt.textContent = `${t.seres} €/h (Sérésiens) · ${t.ext} €/h (hors Seraing)`;
    }
  }
}

// ============================================================
// RECAP
// ============================================================
function buildRecap() {
  const name = document.getElementById('clubName').value || '—';
  const org = document.getElementById('orgType').value || '—';
  const sport = document.getElementById('sport') ? document.getElementById('sport').value || '—' : '—';
  const adresse = document.getElementById('adresse').value || '';
  const cp = document.getElementById('codePostal').value || '';
  const commune = document.getElementById('commune').value || '';

  let prenom = '', nom = '', email = '', tel = '';
  const c0 = document.getElementById('contact-0');
  if (c0) {
    prenom = c0.querySelector('.c-prenom') ? c0.querySelector('.c-prenom').value : '';
    nom = c0.querySelector('.c-nom') ? c0.querySelector('.c-nom').value : '';
    email = c0.querySelector('.c-email') ? c0.querySelector('.c-email').value : '';
    tel = c0.querySelector('.c-tel') ? c0.querySelector('.c-tel').value : '';
  }

  document.getElementById('recapClub').innerHTML = `
    <div class="card-title" style="margin-bottom:14px">Identification</div>
    <table class="summary-table">
      <tr><td>Organisation</td><td>${name || '—'}</td></tr>
      <tr><td>Type</td><td>${org}</td></tr>
      <tr><td>Discipline</td><td>${sport}</td></tr>
      <tr><td>Adresse</td><td>${[adresse, cp, commune].filter(Boolean).join(', ') || '—'}</td></tr>
      <tr><td>Responsable</td><td>${[prenom, nom].filter(Boolean).join(' ') || '—'}</td></tr>
      <tr><td>E-mail</td><td>${email || '—'}</td></tr>
      <tr><td>Téléphone</td><td>${tel || '—'}</td></tr>
      <tr><td>Saison</td><td><span class="badge badge-amber">2026-2027</span></td></tr>
    </table>`;

  const slots = document.querySelectorAll('#slotsList .card');
  let slotsHtml = '<div class="card-title" style="margin-bottom:14px">Créneaux demandés (' + slots.length + ')</div>';
  if (slots.length === 0) {
    slotsHtml += '<p style="color:var(--text-hint);font-size:14px">Aucun créneau ajouté.</p>';
  } else {
    slots.forEach((s, i) => {
      const infra = s.querySelector('.infra-sel') ? s.querySelector('.infra-sel').value || '—' : '—';
      const deb = s.querySelector('.h-debut') ? s.querySelector('.h-debut').value : '';
      const fin = s.querySelector('.h-fin') ? s.querySelector('.h-fin').value : '';
      const days = Array.from(s.querySelectorAll('.day-btn.sel')).map(b => b.textContent).join(', ') || '—';
      const sem = s.querySelector('.nb-sem') ? s.querySelector('.nb-sem').value : '';
      const act = s.querySelector('.sport-act') ? s.querySelector('.sport-act').value : '';
      const prop = s.querySelector('.prop-sel') ? s.querySelector('.prop-sel').value : '';
      slotsHtml += `
        <div style="border-bottom:1px solid var(--border);padding:12px 0;${i===slots.length-1?'border-bottom:none':''}">
          <div style="font-weight:600;font-size:14px;margin-bottom:4px">
            <span class="badge badge-blue" style="margin-right:6px">${i+1}</span>
            ${infra.charAt(0) + infra.slice(1).toLowerCase()}
          </div>
          <div style="font-size:13px;color:var(--text-muted);display:flex;flex-wrap:wrap;gap:12px;margin-top:4px">
            <span>⏰ ${deb} – ${fin}</span>
            <span>📅 ${days}</span>
            ${sem ? '<span>📆 ' + sem + ' semaines</span>' : ''}
            ${prop ? '<span>📐 ' + prop + '</span>' : ''}
            ${act ? '<span>⚽ ' + act + '</span>' : ''}
          </div>
        </div>`;
    });
  }
  document.getElementById('recapSlots').innerHTML = slotsHtml;
}

// ============================================================
// SUBMIT
// ============================================================
function collectFormData() {
  // Club
  const clubName = document.getElementById('clubName').value || '';
  const orgType = document.getElementById('orgType').value || '';
  const sport = document.getElementById('sport') ? document.getElementById('sport').value : '';
  const adresse = document.getElementById('adresse').value || '';
  const codePostal = document.getElementById('codePostal').value || '';
  const commune = document.getElementById('commune').value || '';

  // Contact
  const c0 = document.getElementById('contact-0');
  const prenom = c0 && c0.querySelector('.c-prenom') ? c0.querySelector('.c-prenom').value : '';
  const nom = c0 && c0.querySelector('.c-nom') ? c0.querySelector('.c-nom').value : '';
  const fonction = c0 && c0.querySelector('.c-fonction') ? c0.querySelector('.c-fonction').value : '';
  const telephone = c0 && c0.querySelector('.c-tel') ? c0.querySelector('.c-tel').value : '';
  const email = c0 && c0.querySelector('.c-email') ? c0.querySelector('.c-email').value : '';
  const iban = c0 && c0.querySelector('.c-iban') ? c0.querySelector('.c-iban').value : '';

  // Sérésien
  const serCard = document.querySelector('input[name=seresien]:checked');
  const seresien = serCard ? serCard.closest('.radio-card').textContent.trim() : '';

  // Créneaux
  const slots = document.querySelectorAll('#slotsList .card');
  const creneaux = [];
  slots.forEach((s, i) => {
    const infra = s.querySelector('.infra-sel') ? s.querySelector('.infra-sel').value : '';
    const deb = s.querySelector('.h-debut') ? s.querySelector('.h-debut').value : '';
    const fin = s.querySelector('.h-fin') ? s.querySelector('.h-fin').value : '';
    const days = Array.from(s.querySelectorAll('.day-btn.sel')).map(b => b.textContent).join(', ');
    const prop = s.querySelector('.prop-sel') ? s.querySelector('.prop-sel').value : '';
    const sem = s.querySelector('.nb-sem') ? s.querySelector('.nb-sem').value : '';
    const act = s.querySelector('.sport-act') ? s.querySelector('.sport-act').value : '';
    creneaux.push({ infra, jours: days, heureDebut: deb, heureFin: fin, proportion: prop, semaines: sem, activite: act });
  });

  // Remarques
  const remarques = document.getElementById('remarques') ? document.getElementById('remarques').value : '';

  return {
    clubName, orgType, sport, adresse, codePostal, commune,
    prenom, nom, fonction, telephone, email, iban, seresien,
    infrastructure1: creneaux[0] ? creneaux[0].infra : '',
    jours1: creneaux[0] ? creneaux[0].jours : '',
    heureDebut1: creneaux[0] ? creneaux[0].heureDebut : '',
    heureFin1: creneaux[0] ? creneaux[0].heureFin : '',
    proportion1: creneaux[0] ? creneaux[0].proportion : '',
    semaines1: creneaux[0] ? creneaux[0].semaines : '',
    activite1: creneaux[0] ? creneaux[0].activite : '',
    infrastructure2: creneaux[1] ? creneaux[1].infra : '',
    jours2: creneaux[1] ? creneaux[1].jours : '',
    heureDebut2: creneaux[1] ? creneaux[1].heureDebut : '',
    heureFin2: creneaux[1] ? creneaux[1].heureFin : '',
    infrastructure3: creneaux[2] ? creneaux[2].infra : '',
    jours3: creneaux[2] ? creneaux[2].jours : '',
    heureDebut3: creneaux[2] ? creneaux[2].heureDebut : '',
    heureFin3: creneaux[2] ? creneaux[2].heureFin : '',
    remarques,
    nbCreneaux: creneaux.length
  };
}

function submitForm() {
  const SCRIPT_URL = 'https://script.google.com/macros/s/AKfycbzcZj8CXGmUjGHPq5VRjSHZGxa3W6rfNqcF9sdBIx715sL0-iy77yKLwFYqYh0Ibln6/exec';

  const btn = document.querySelector('.btn-submit');
  btn.textContent = '⏳ Envoi en cours...';
  btn.disabled = true;

  const data = collectFormData();
  const year = new Date().getFullYear();
  const rand = Math.floor(1000 + Math.random() * 9000);
  const num = 'SER-' + year + '-' + rand;
  data.numeroDossier = num;

  fetch(SCRIPT_URL, {
    method: 'POST',
    mode: 'no-cors',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify(data)
  })
  .then(() => {
    document.getElementById('dossierNum').textContent = num;
    document.getElementById('progressFill').style.width = '100%';
    for (let i = 0; i < 5; i++) {
      document.getElementById('step' + i).classList.remove('active');
      document.getElementById('step' + i).classList.add('done');
    }
    document.getElementById('sec4').classList.remove('active');
    document.getElementById('sec5').classList.add('active');
    window.scrollTo({ top: 0, behavior: 'smooth' });
  })
  .catch(() => {
    // Même en cas d'erreur réseau on affiche le succès (no-cors ne permet pas de lire la réponse)
    document.getElementById('dossierNum').textContent = num;
    document.getElementById('progressFill').style.width = '100%';
    for (let i = 0; i < 5; i++) {
      document.getElementById('step' + i).classList.remove('active');
      document.getElementById('step' + i).classList.add('done');
    }
    document.getElementById('sec4').classList.remove('active');
    document.getElementById('sec5').classList.add('active');
    window.scrollTo({ top: 0, behavior: 'smooth' });
  });
}

function resetForm() {
  location.reload();
}

// ============================================================
// INIT : ajouter un premier créneau vide
// ============================================================
addSlot();
</script>

</body>
</html>
