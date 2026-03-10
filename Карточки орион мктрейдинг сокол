<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Карточки компаний — ОРИОН · МК ТРЕЙДИНГ · СОКОЛ</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Mulish:wght@300;400;600;700;900&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #f0f2f5;
  --card: #ffffff;
  --surface: #f9fafc;
  --border: #e4e8ef;
  --text: #1a1f2e;
  --muted: #8a95a8;
  --green: #1e7e4a;

  /* ОРИОН — тёмно-синий + золото (Raiffeisen) */
  --o-accent: #0d2240;
  --o-accent2: #1a4480;
  --o-raif: #ffcb00;
  --o-raif2: #1a1a1a;

  /* МК ТРЕЙДИНГ — синий ВТБ */
  --m-accent: #003087;
  --m-accent2: #0050b3;
  --m-vtb: #009fdf;

  /* СОКОЛ — красный Альфа */
  --s-accent: #145a32;
  --s-accent2: #1e8449;
  --s-alfa: #27ae60;
}
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
body {
  background: var(--bg);
  font-family: 'Mulish', sans-serif;
  color: var(--text);
  min-height: 100vh;
  display: flex; align-items: flex-start; justify-content: center;
  padding: 32px 16px 60px;
}
.wrap { width: 100%; max-width: 700px; }

/* SWITCHER — 3 вкладки */
.switcher {
  display: flex; background: #dde1e9;
  border-radius: 16px; padding: 5px; margin-bottom: 20px; gap: 4px;
}
.switcher-tab {
  flex: 1; text-align: center; padding: 10px 8px;
  border-radius: 12px; cursor: pointer;
  transition: all 0.28s cubic-bezier(.4,0,.2,1);
  user-select: none;
}
.switcher-tab-name { font-family: 'Bebas Neue', sans-serif; font-size: 18px; letter-spacing: 1.5px; line-height: 1; color: #8a95a8; transition: color 0.25s; }
.switcher-tab-sub  { font-size: 9px; font-weight: 700; letter-spacing: 1px; text-transform: uppercase; margin-top: 3px; color: #b0b8c8; transition: color 0.25s; }
.active-o { background: var(--o-accent); box-shadow: 0 4px 18px rgba(13,34,64,0.35); }
.active-o .switcher-tab-name { color: #fff; }
.active-o .switcher-tab-sub  { color: var(--o-raif); }
.active-m { background: var(--m-accent); box-shadow: 0 4px 18px rgba(0,48,135,0.35); }
.active-m .switcher-tab-name { color: #fff; }
.active-m .switcher-tab-sub  { color: var(--m-vtb); }
.active-s { background: #145a32; box-shadow: 0 4px 18px rgba(20,90,50,0.40); }
.active-s .switcher-tab-name { color: #fff; }
.active-s .switcher-tab-sub  { color: #82e0aa; }

/* КАРТОЧКА */
.company-card { display: none; animation: fadeIn 0.3s ease; }
.company-card.visible { display: block; }
@keyframes fadeIn { from { opacity:0; transform: translateY(6px); } to { opacity:1; transform: translateY(0); } }

/* ШАПКА */
.card-header {
  border-radius: 20px 20px 0 0; padding: 32px 28px 28px;
  position: relative; overflow: hidden;
}
.card-header-orion    { background: linear-gradient(135deg, #0d2240 0%, #1a4480 60%, #0d2240 100%); }
.card-header-mktreid  { background: linear-gradient(135deg, #003087 0%, #0050b3 60%, #003087 100%); }
.card-header-sokol    { background: linear-gradient(135deg, #0d3b1f 0%, #1a6b35 60%, #145a32 100%); }

.card-header::before {
  content: '';
  position: absolute; top: -40px; right: -40px;
  width: 200px; height: 200px; border-radius: 50%;
  background: rgba(255,255,255,0.04);
}
.card-header::after {
  content: '';
  position: absolute; bottom: -60px; left: 30%;
  width: 300px; height: 300px; border-radius: 50%;
  background: rgba(255,255,255,0.03);
}
.header-top { display: flex; justify-content: space-between; align-items: flex-start; gap: 16px; }
.company-name-full { font-size: 11px; font-weight: 700; letter-spacing: 2px; text-transform: uppercase; color: rgba(255,255,255,0.55); margin-bottom: 6px; }
.company-name-short { font-family: 'Bebas Neue', sans-serif; font-size: 42px; letter-spacing: 3px; color: #fff; line-height: 1; }
.header-inn-block { text-align: right; flex-shrink: 0; }
.inn-label { font-size: 9px; font-weight: 700; letter-spacing: 1.5px; text-transform: uppercase; color: rgba(255,255,255,0.45); }
.inn-value { font-family: 'Bebas Neue', sans-serif; font-size: 22px; letter-spacing: 2px; color: rgba(255,255,255,0.9); }
.ogrn-row { font-size: 10px; color: rgba(255,255,255,0.45); margin-top: 2px; font-weight: 600; letter-spacing: 0.5px; }
.header-divider { height: 1px; background: rgba(255,255,255,0.12); margin: 18px 0 16px; }
.header-bottom { display: flex; gap: 28px; flex-wrap: wrap; }
.header-stat { }
.header-stat-label { font-size: 9px; font-weight: 700; letter-spacing: 1.5px; text-transform: uppercase; color: rgba(255,255,255,0.4); }
.header-stat-value { font-size: 13px; font-weight: 700; color: rgba(255,255,255,0.9); margin-top: 2px; }

/* ACCENT BADGE — цвет банка/зоны */
.accent-badge-raif { background: var(--o-raif); color: #111; }
.accent-badge-vtb  { background: var(--m-vtb);  color: #fff; }
.accent-badge-alfa { background: #27ae60; color: #fff; }
.accent-badge { display: inline-flex; align-items: center; gap: 6px; padding: 4px 12px; border-radius: 50px; font-size: 10px; font-weight: 900; letter-spacing: 1px; text-transform: uppercase; margin-top: 12px; }

/* BODY */
.card-body { background: var(--card); border-radius: 0 0 20px 20px; padding: 8px 0 0; }

.section { padding: 20px 28px; border-bottom: 1px solid var(--border); }
.section:last-child { border-bottom: none; }
.section-title {
  font-size: 10px; font-weight: 900; letter-spacing: 2px; text-transform: uppercase;
  margin-bottom: 14px; display: flex; align-items: center; gap: 8px;
}
.section-title-orion   { color: var(--o-accent2); }
.section-title-mktreid { color: var(--m-accent2); }
.section-title-sokol   { color: var(--s-accent2); }

/* INFO GRID */
.info-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
@media (max-width: 480px) { .info-grid { grid-template-columns: 1fr; } }
.info-item { background: var(--surface); border-radius: 10px; padding: 10px 14px; border: 1px solid var(--border); }
.info-item.full { grid-column: 1 / -1; }
.info-label { font-size: 9px; font-weight: 700; letter-spacing: 1.5px; text-transform: uppercase; color: var(--muted); margin-bottom: 4px; }
.info-value { font-size: 13px; font-weight: 700; color: var(--text); line-height: 1.4; }
.info-value a { color: inherit; text-decoration: none; }
.info-value a:hover { text-decoration: underline; }

/* BANK */
.bank-block { border-radius: 14px; padding: 18px 20px; position: relative; overflow: hidden; }

.bank-raif { background: linear-gradient(135deg, #1a1a1a, #2a2a2a); border: 1px solid #333; }
.bank-raif .bank-name { color: var(--o-raif); }
.bank-raif .bank-data-label { color: rgba(255,255,255,0.4); }
.bank-raif .bank-data-value { color: #fff; }

.bank-vtb { background: linear-gradient(135deg, #001850, #003087); border: 1px solid rgba(0,159,223,0.3); }
.bank-vtb .bank-name { color: var(--m-vtb); }
.bank-vtb .bank-data-label { color: rgba(255,255,255,0.4); }
.bank-vtb .bank-data-value { color: #fff; }

.bank-alfa { background: linear-gradient(135deg, #0a1f12, #133d22); border: 1px solid rgba(39,174,96,0.35); }
.bank-alfa .bank-name { color: #2ecc71; }
.bank-alfa .bank-data-label { color: rgba(255,255,255,0.4); }
.bank-alfa .bank-data-value { color: #fff; }

.bank-name { font-family: 'Bebas Neue', sans-serif; font-size: 17px; letter-spacing: 1.5px; margin-bottom: 14px; display: block; }
.bank-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
@media (max-width: 480px) { .bank-grid { grid-template-columns: 1fr; } }
.bank-item { }
.bank-data-label { font-size: 9px; font-weight: 700; letter-spacing: 1px; text-transform: uppercase; margin-bottom: 3px; }
.bank-data-value { font-size: 12px; font-weight: 700; font-family: 'Courier New', monospace; word-break: break-all; }
.bank-acc { grid-column: 1 / -1; }

/* DIRECTOR */
.director-block { display: flex; align-items: center; gap: 14px; }
.director-avatar {
  width: 48px; height: 48px; border-radius: 50%; flex-shrink: 0;
  display: flex; align-items: center; justify-content: center;
  font-family: 'Bebas Neue', sans-serif; font-size: 16px; color: #fff;
  letter-spacing: 1px;
}
.director-avatar-orion   { background: linear-gradient(135deg, var(--o-accent), var(--o-accent2)); }
.director-avatar-mktreid { background: linear-gradient(135deg, var(--m-accent), var(--m-accent2)); }
.director-avatar-sokol   { background: linear-gradient(135deg, var(--s-accent), var(--s-accent2)); }
.director-name { font-size: 15px; font-weight: 800; color: var(--text); }
.director-role { font-size: 11px; font-weight: 600; color: var(--muted); margin-top: 3px; }

/* OKVED */
.okved-chips { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 12px; }
.okved-chip { font-size: 10px; font-weight: 700; padding: 4px 10px; border-radius: 6px; }
.okved-chip-main-o { background: rgba(26,68,128,0.12); color: var(--o-accent2); border: 1px solid rgba(26,68,128,0.2); }
.okved-chip-add-o  { background: rgba(26,68,128,0.05); color: var(--muted); border: 1px solid var(--border); }
.okved-chip-main-m { background: rgba(0,80,179,0.12); color: var(--m-accent2); border: 1px solid rgba(0,80,179,0.2); }
.okved-chip-add-m  { background: rgba(0,80,179,0.05); color: var(--muted); border: 1px solid var(--border); }
.okved-chip-main-s { background: rgba(200,16,46,0.10); color: var(--s-accent2); border: 1px solid rgba(200,16,46,0.2); }
.okved-chip-add-s  { background: rgba(200,16,46,0.04); color: var(--muted); border: 1px solid var(--border); }

/* ЗСК */
.zsk-block { border-radius: 14px; padding: 18px 20px; }
.zsk-green-light { background: linear-gradient(135deg, rgba(30,126,74,0.08), rgba(30,126,74,0.03)); border: 1.5px solid rgba(30,126,74,0.30); }
.zsk-header { display: flex; align-items: center; gap: 12px; }
.zsk-icon { font-size: 26px; }
.zsk-title { font-size: 13px; font-weight: 900; color: var(--green); }
.zsk-sub { font-size: 10px; color: var(--muted); font-weight: 600; margin-top: 2px; }
.zsk-note { font-size: 11px; color: var(--muted); margin-top: 12px; padding-top: 12px; border-top: 1px solid rgba(30,126,74,0.15); }

/* FOOTER */
.card-footer { border-radius: 0 0 20px 20px; padding: 20px 28px 24px; }
.footer-orion   { background: var(--o-accent); }
.footer-mktreid { background: var(--m-accent); }
.footer-sokol   { background: #145a32; }
.footer-contacts { display: flex; flex-wrap: wrap; gap: 8px 20px; margin-bottom: 16px; }
.footer-item { font-size: 12px; font-weight: 600; color: rgba(255,255,255,0.75); }
.footer-item strong { color: #fff; }

.copy-btn {
  width: 100%; padding: 13px 20px; border-radius: 12px; border: none; cursor: pointer;
  font-family: 'Mulish', sans-serif; font-size: 13px; font-weight: 800; letter-spacing: 0.5px;
  transition: all 0.2s; display: flex; align-items: center; justify-content: center; gap: 8px;
}
.copy-btn-orion   { background: var(--o-raif); color: #111; }
.copy-btn-orion:hover   { background: #e6b800; }
.copy-btn-mktreid { background: var(--m-vtb);  color: #fff; }
.copy-btn-mktreid:hover { background: #007ab8; }
.copy-btn-sokol   { background: #27ae60; color: #fff; }
.copy-btn-sokol:hover   { background: #1e8449; }
.copy-btn.copied { opacity: 0.7; }

.note-placeholder {
  background: rgba(255,255,255,0.08); border: 1px solid rgba(255,255,255,0.12);
  border-radius: 10px; padding: 12px 16px; margin-bottom: 14px;
  font-size: 11px; color: rgba(255,255,255,0.55); font-style: italic;
}
</style>
</head>
<body>
<div class="wrap">

  <div class="switcher" id="sw">
    <div class="switcher-tab active-o" onclick="switchTo('o')">
      <div class="switcher-tab-name">ОРИОН</div>
      <div class="switcher-tab-sub">ИНН 9701271862</div>
    </div>
    <div class="switcher-tab" onclick="switchTo('m')">
      <div class="switcher-tab-name">МК ТРЕЙДИНГ</div>
      <div class="switcher-tab-sub">ИНН 5074070731</div>
    </div>
    <div class="switcher-tab" onclick="switchTo('s')">
      <div class="switcher-tab-name">СОКОЛ</div>
      <div class="switcher-tab-sub">ИНН 0522022398</div>
    </div>
  </div>

  <!-- ==================== ОРИОН ==================== -->
  <div class="company-card visible" id="card-o">
    <div class="card-header card-header-orion">
      <div class="header-top">
        <div>
          <div class="company-name-full">Общество с ограниченной ответственностью</div>
          <div class="company-name-short">ОРИОН</div>
          <div class="accent-badge accent-badge-raif">🏦 Райффайзенбанк</div>
        </div>
        <div class="header-inn-block">
          <div class="inn-label">ИНН</div>
          <div class="inn-value">9701271862</div>
          <div class="ogrn-row">КПП 770101001</div>
          <div class="ogrn-row">ОГРН 1237700940982</div>
        </div>
      </div>
      <div class="header-divider"></div>
      <div class="header-bottom">
        <div class="header-stat">
          <div class="header-stat-label">Дата регистрации</div>
          <div class="header-stat-value">26.12.2023</div>
        </div>
        <div class="header-stat">
          <div class="header-stat-label">Уставный капитал</div>
          <div class="header-stat-value">1 100 000 ₽</div>
        </div>
        <div class="header-stat">
          <div class="header-stat-label">Основной ОКВЭД</div>
          <div class="header-stat-value">46.90 — Опт. неспециализированная</div>
        </div>
      </div>
    </div>

    <div class="card-body">

      <div class="section">
        <div class="section-title section-title-orion">📍 Юридический адрес</div>
        <div class="info-grid">
          <div class="info-item full">
            <div class="info-label">Адрес</div>
            <div class="info-value">101000, г. Москва, вн.тер.г. МО Басманный, ул. Мясницкая, д. 30/1/2, стр. 2, помещ. 1/Ч</div>
          </div>
          <div class="info-item">
            <div class="info-label">Налоговый орган</div>
            <div class="info-value">ИФНС № 1 по г. Москве</div>
          </div>
          <div class="info-item">
            <div class="info-label">Регистрирующий орган</div>
            <div class="info-value">МИФНС № 46 по г. Москве</div>
          </div>
        </div>
      </div>

      <div class="section">
        <div class="section-title section-title-orion">🗂 Регистрационные данные</div>
        <div class="info-grid">
          <div class="info-item">
            <div class="info-label">ИНН</div>
            <div class="info-value">9701271862</div>
          </div>
          <div class="info-item">
            <div class="info-label">КПП</div>
            <div class="info-value">770101001</div>
          </div>
          <div class="info-item">
            <div class="info-label">ОГРН</div>
            <div class="info-value">1237700940982</div>
          </div>
          <div class="info-item">
            <div class="info-label">Дата регистрации</div>
            <div class="info-value">26.12.2023</div>
          </div>
          <div class="info-item">
            <div class="info-label">Уставный капитал</div>
            <div class="info-value">1 100 000 руб.</div>
          </div>
          <div class="info-item">
            <div class="info-label">Доля участника</div>
            <div class="info-value">100% — Магомедов И.М.</div>
          </div>
        </div>
      </div>

      <div class="section">
        <div class="section-title section-title-orion">🏦 Банковские реквизиты — Райффайзенбанк</div>
        <div class="bank-block bank-raif">
          <span class="bank-name">🟡 АО «РАЙФФАЙЗЕНБАНК»</span>
          <div class="bank-grid">
            <div class="bank-item bank-acc">
              <div class="bank-data-label">Расчётный счёт</div>
              <div class="bank-data-value">40702 810 3 0000 0298647</div>
            </div>
            <div class="bank-item bank-acc">
              <div class="bank-data-label">Корреспондентский счёт</div>
              <div class="bank-data-value">30101 810 2 0000 0000700</div>
            </div>
            <div class="bank-item">
              <div class="bank-data-label">БИК</div>
              <div class="bank-data-value">044525700</div>
            </div>
            <div class="bank-item">
              <div class="bank-data-label">Лицензия</div>
              <div class="bank-data-value">№ 3292</div>
            </div>
          </div>
        </div>
      </div>

      <div class="section">
        <div class="section-title section-title-orion">📊 Виды деятельности (ОКВЭД)</div>
        <div class="okved-chips">
          <span class="okved-chip okved-chip-main-o">46.90 ★ Опт. неспециализированная</span>
          <span class="okved-chip okved-chip-add-o">46.71 Опт. топливо</span>
          <span class="okved-chip okved-chip-add-o">46.71.9 Прочее топливо</span>
          <span class="okved-chip okved-chip-add-o">46.73 Стройматериалы</span>
        </div>
      </div>

      <div class="section">
        <div class="section-title section-title-orion">🚦 Реестр ЗСК · Банк России</div>
        <div class="zsk-block zsk-green-light">
          <div class="zsk-header">
            <div class="zsk-icon">✅</div>
            <div>
              <div class="zsk-title">В списках не найдено</div>
              <div class="zsk-sub">ЗСК · ИНН 9701271862 · ООО ОРИОН</div>
            </div>
          </div>
          <div class="zsk-note">🏦 В чёрных списках ЦБ, ЗСК, 115-ФЗ и 764-П не найдено. Проверено по реестрам Банка России.</div>
        </div>
      </div>

      <div class="section">
        <div class="section-title section-title-orion">👤 Генеральный директор</div>
        <div class="director-block">
          <div class="director-avatar director-avatar-orion">МИ</div>
          <div>
            <div class="director-name">Магомедов Иса Магомедович</div>
            <div class="director-role">Генеральный директор · ООО «ОРИОН»</div>
          </div>
        </div>
      </div>

    </div>

    <div class="card-footer footer-orion">
      <div class="note-placeholder">📌 Контактные данные уточните у представителя компании</div>
      <button class="copy-btn copy-btn-orion" onclick="copyWA_O(this)">📋 Скопировать для WhatsApp</button>
    </div>
  </div>

  <!-- ==================== МК ТРЕЙДИНГ ==================== -->
  <div class="company-card" id="card-m">
    <div class="card-header card-header-mktreid">
      <div class="header-top">
        <div>
          <div class="company-name-full">Общество с ограниченной ответственностью</div>
          <div class="company-name-short">МК ТРЕЙДИНГ</div>
          <div class="accent-badge accent-badge-vtb">🏦 ВТБ Банк</div>
        </div>
        <div class="header-inn-block">
          <div class="inn-label">ИНН</div>
          <div class="inn-value">5074070731</div>
          <div class="ogrn-row">КПП 507401001</div>
          <div class="ogrn-row">ОГРН 1215000081526</div>
        </div>
      </div>
      <div class="header-divider"></div>
      <div class="header-bottom">
        <div class="header-stat">
          <div class="header-stat-label">Дата регистрации</div>
          <div class="header-stat-value">11.08.2021</div>
        </div>
        <div class="header-stat">
          <div class="header-stat-label">Уставный капитал</div>
          <div class="header-stat-value">10 000 ₽</div>
        </div>
        <div class="header-stat">
          <div class="header-stat-label">Основной ОКВЭД</div>
          <div class="header-stat-value">46.71 — Опт. топливо</div>
        </div>
      </div>
    </div>

    <div class="card-body">

      <div class="section">
        <div class="section-title section-title-mktreid">📍 Юридический адрес</div>
        <div class="info-grid">
          <div class="info-item full">
            <div class="info-label">Адрес</div>
            <div class="info-value">142121, Московская область, г.о. Подольск, г. Подольск, мкр. Кузнечики, ул. Академика Доллежаля, д. 38, кв. 112</div>
          </div>
          <div class="info-item">
            <div class="info-label">Налоговый орган</div>
            <div class="info-value">МИФНС № 5 по Московской области</div>
          </div>
          <div class="info-item">
            <div class="info-label">Регистрирующий орган</div>
            <div class="info-value">МИФНС № 23 по Московской области</div>
          </div>
        </div>
      </div>

      <div class="section">
        <div class="section-title section-title-mktreid">🗂 Регистрационные данные</div>
        <div class="info-grid">
          <div class="info-item">
            <div class="info-label">ИНН</div>
            <div class="info-value">5074070731</div>
          </div>
          <div class="info-item">
            <div class="info-label">КПП</div>
            <div class="info-value">507401001</div>
          </div>
          <div class="info-item">
            <div class="info-label">ОГРН</div>
            <div class="info-value">1215000081526</div>
          </div>
          <div class="info-item">
            <div class="info-label">Дата регистрации</div>
            <div class="info-value">11.08.2021</div>
          </div>
          <div class="info-item">
            <div class="info-label">Уставный капитал</div>
            <div class="info-value">10 000 руб.</div>
          </div>
          <div class="info-item">
            <div class="info-label">Доля участника</div>
            <div class="info-value">100% — Исрафилов И.И.</div>
          </div>
        </div>
      </div>

      <div class="section">
        <div class="section-title section-title-mktreid">🏦 Банковские реквизиты — ВТБ</div>
        <div class="bank-block bank-vtb">
          <span class="bank-name">🔵 ПАО «БАНК ВТБ»</span>
          <div class="bank-grid">
            <div class="bank-item bank-acc">
              <div class="bank-data-label">Расчётный счёт</div>
              <div class="bank-data-value">— уточнить у представителя —</div>
            </div>
            <div class="bank-item bank-acc">
              <div class="bank-data-label">Примечание</div>
              <div class="bank-data-value" style="font-family:'Mulish',sans-serif;font-size:11px;font-weight:400;color:rgba(255,255,255,0.6);">Реквизиты ВТБ подтвердить дополнительно</div>
            </div>
          </div>
        </div>
      </div>

      <div class="section">
        <div class="section-title section-title-mktreid">📊 Виды деятельности (ОКВЭД)</div>
        <div class="okved-chips">
          <span class="okved-chip okved-chip-main-m">46.71 ★ Опт. твёрдое/жидкое топливо</span>
          <span class="okved-chip okved-chip-add-m">46.71.4 Природный газ</span>
          <span class="okved-chip okved-chip-add-m">46.71.5 Сжиженный газ</span>
          <span class="okved-chip okved-chip-add-m">46.71.9 Прочее топливо</span>
          <span class="okved-chip okved-chip-add-m">47.30 Розн. моторное топливо</span>
          <span class="okved-chip okved-chip-add-m">49.41 Грузовые перевозки</span>
          <span class="okved-chip okved-chip-add-m">52.10 Хранение/складирование</span>
          <span class="okved-chip okved-chip-add-m">52.21 Вспом. транспорт</span>
        </div>
      </div>

      <div class="section">
        <div class="section-title section-title-mktreid">🚦 Реестр ЗСК · Банк России</div>
        <div class="zsk-block zsk-green-light">
          <div class="zsk-header">
            <div class="zsk-icon">✅</div>
            <div>
              <div class="zsk-title">В списках не найдено</div>
              <div class="zsk-sub">ЗСК · ИНН 5074070731 · ООО МК ТРЕЙДИНГ</div>
            </div>
          </div>
          <div class="zsk-note">🏦 В чёрных списках ЦБ, ЗСК, 115-ФЗ и 764-П не найдено. Проверено по реестрам Банка России.</div>
        </div>
      </div>

      <div class="section">
        <div class="section-title section-title-mktreid">👤 Генеральный директор</div>
        <div class="director-block">
          <div class="director-avatar director-avatar-mktreid">ИИ</div>
          <div>
            <div class="director-name">Исрафилов Исмаил Исрафилович</div>
            <div class="director-role">Генеральный директор · ООО «МК ТРЕЙДИНГ»</div>
          </div>
        </div>
      </div>

    </div>

    <div class="card-footer footer-mktreid">
      <div class="note-placeholder">📌 Контактные данные уточните у представителя компании</div>
      <button class="copy-btn copy-btn-mktreid" onclick="copyWA_M(this)">📋 Скопировать для WhatsApp</button>
    </div>
  </div>

  <!-- ==================== СОКОЛ ==================== -->
  <div class="company-card" id="card-s">
    <div class="card-header card-header-sokol">
      <div class="header-top">
        <div>
          <div class="company-name-full">Общество с ограниченной ответственностью</div>
          <div class="company-name-short">СОКОЛ</div>
          <div class="accent-badge accent-badge-alfa">🏦 Альфа-Банк</div>
        </div>
        <div class="header-inn-block">
          <div class="inn-label">ИНН</div>
          <div class="inn-value">0522022398</div>
          <div class="ogrn-row">КПП 052201001</div>
          <div class="ogrn-row">ОГРН 1180571009112</div>
        </div>
      </div>
      <div class="header-divider"></div>
      <div class="header-bottom">
        <div class="header-stat">
          <div class="header-stat-label">Дата регистрации</div>
          <div class="header-stat-value">25.07.2018</div>
        </div>
        <div class="header-stat">
          <div class="header-stat-label">Уставный капитал</div>
          <div class="header-stat-value">1 000 000 ₽</div>
        </div>
        <div class="header-stat">
          <div class="header-stat-label">Основной ОКВЭД</div>
          <div class="header-stat-value">46.71 — Опт. топливо</div>
        </div>
      </div>
    </div>

    <div class="card-body">

      <div class="section">
        <div class="section-title section-title-sokol">📍 Юридический адрес</div>
        <div class="info-grid">
          <div class="info-item full">
            <div class="info-label">Адрес</div>
            <div class="info-value">368530, Республика Дагестан, Карабудахкентский р-н, с. Карабудахкент, ул. Акъай Мола, д. 1</div>
          </div>
          <div class="info-item full">
            <div class="info-label">E-mail</div>
            <div class="info-value"><a href="mailto:Sokol.19.09@bk.ru">Sokol&#46;19&#46;09&#64;bk&#46;ru</a></div>
          </div>
          <div class="info-item">
            <div class="info-label">Телефон</div>
            <div class="info-value">+7 (965) 568-00-00</div>
          </div>
          <div class="info-item">
            <div class="info-label">Налоговый орган</div>
            <div class="info-value">УФНС по Республике Дагестан</div>
          </div>
        </div>
      </div>

      <div class="section">
        <div class="section-title section-title-sokol">🗂 Регистрационные данные</div>
        <div class="info-grid">
          <div class="info-item">
            <div class="info-label">ИНН</div>
            <div class="info-value">0522022398</div>
          </div>
          <div class="info-item">
            <div class="info-label">КПП</div>
            <div class="info-value">052201001</div>
          </div>
          <div class="info-item">
            <div class="info-label">ОГРН</div>
            <div class="info-value">1180571009112</div>
          </div>
          <div class="info-item">
            <div class="info-label">ОКПО</div>
            <div class="info-value">32206625</div>
          </div>
          <div class="info-item">
            <div class="info-label">Дата регистрации</div>
            <div class="info-value">25.07.2018</div>
          </div>
          <div class="info-item">
            <div class="info-label">Система нал-ния</div>
            <div class="info-value">ОСНО</div>
          </div>
          <div class="info-item">
            <div class="info-label">Уставный капитал</div>
            <div class="info-value">1 000 000 руб.</div>
          </div>
          <div class="info-item">
            <div class="info-label">Доля участника</div>
            <div class="info-value">100% — Ахмедов С.З.</div>
          </div>
        </div>
      </div>

      <div class="section">
        <div class="section-title section-title-sokol">🏦 Банковские реквизиты — Альфа-Банк</div>
        <div class="bank-block bank-alfa">
          <span class="bank-name">🔴 ФИЛИАЛ «СТАВРОПОЛЬСКИЙ» АО «АЛЬФА-БАНК»</span>
          <div class="bank-grid">
            <div class="bank-item bank-acc">
              <div class="bank-data-label">Расчётный счёт</div>
              <div class="bank-data-value">40702 810 9 5604 0001894</div>
            </div>
            <div class="bank-item bank-acc">
              <div class="bank-data-label">Корреспондентский счёт</div>
              <div class="bank-data-value">30101 810 0 0000 0000752</div>
            </div>
            <div class="bank-item">
              <div class="bank-data-label">БИК</div>
              <div class="bank-data-value">040702752</div>
            </div>
            <div class="bank-item">
              <div class="bank-data-label">Город</div>
              <div class="bank-data-value">г. Ставрополь</div>
            </div>
          </div>
        </div>
      </div>

      <div class="section">
        <div class="section-title section-title-sokol">📊 Виды деятельности (ОКВЭД)</div>
        <div class="okved-chips">
          <span class="okved-chip okved-chip-main-s">46.71 ★ Опт. топливо</span>
          <span class="okved-chip okved-chip-add-s">46.90 Опт. неспециализированная</span>
          <span class="okved-chip okved-chip-add-s">46.32 Мясо и мясопродукты</span>
          <span class="okved-chip okved-chip-add-s">46.31 Фрукты и овощи</span>
          <span class="okved-chip okved-chip-add-s">46.72 Металлы</span>
          <span class="okved-chip okved-chip-add-s">46.73 Стройматериалы</span>
          <span class="okved-chip okved-chip-add-s">49.41 Грузоперевозки</span>
          <span class="okved-chip okved-chip-add-s">47.30 Розн. топливо</span>
        </div>
      </div>

      <div class="section">
        <div class="section-title section-title-sokol">🚦 Реестр ЗСК · Банк России</div>
        <div class="zsk-block zsk-green-light">
          <div class="zsk-header">
            <div class="zsk-icon">✅</div>
            <div>
              <div class="zsk-title">В списках не найдено</div>
              <div class="zsk-sub">ЗСК · ИНН 0522022398 · ООО СОКОЛ</div>
            </div>
          </div>
          <div class="zsk-note">🏦 В чёрных списках ЦБ, ЗСК, 115-ФЗ и 764-П не найдено. Проверено по реестрам Банка России.</div>
        </div>
      </div>

      <div class="section">
        <div class="section-title section-title-sokol">👤 Генеральный директор</div>
        <div class="director-block">
          <div class="director-avatar director-avatar-sokol">АР</div>
          <div>
            <div class="director-name">Абдуллаев Руслан Гасанович</div>
            <div class="director-role">Генеральный директор · ООО «СОКОЛ»</div>
          </div>
        </div>
      </div>

    </div>

    <div class="card-footer footer-sokol">
      <div class="footer-contacts">
        <div class="footer-item"><strong>📞</strong> +7 (965) 568-00-00</div>
        <div class="footer-item"><strong>📧</strong> Sokol&#46;19&#46;09&#64;bk&#46;ru</div>
      </div>
      <button class="copy-btn copy-btn-sokol" onclick="copyWA_S(this)">📋 Скопировать для WhatsApp</button>
    </div>
  </div>

</div>

<script>
var tabs = document.querySelectorAll('.switcher-tab');
function switchTo(c) {
  var co = document.getElementById('card-o');
  var cm = document.getElementById('card-m');
  var cs = document.getElementById('card-s');
  tabs[0].className = 'switcher-tab'; tabs[1].className = 'switcher-tab'; tabs[2].className = 'switcher-tab';
  if (c === 'o') { co.className='company-card visible'; cm.className='company-card'; cs.className='company-card'; tabs[0].className='switcher-tab active-o'; }
  if (c === 'm') { cm.className='company-card visible'; co.className='company-card'; cs.className='company-card'; tabs[1].className='switcher-tab active-m'; }
  if (c === 's') { cs.className='company-card visible'; co.className='company-card'; cm.className='company-card'; tabs[2].className='switcher-tab active-s'; }
}

function doCopy(lines, btn) {
  var text = lines.join('\n');
  var done = function() { btn.textContent = '✅ Скопировано!'; btn.classList.add('copied'); setTimeout(function(){ btn.textContent = '📋 Скопировать для WhatsApp'; btn.classList.remove('copied'); }, 2500); };
  if (navigator.clipboard && navigator.clipboard.writeText) {
    navigator.clipboard.writeText(text).then(done).catch(function() {
      var ta = document.createElement('textarea'); ta.value = text;
      ta.style.cssText = 'position:fixed;opacity:0;top:0;left:0;';
      document.body.appendChild(ta); ta.select();
      try { document.execCommand('copy'); done(); } catch(e) { alert(text); }
      document.body.removeChild(ta);
    });
  } else {
    var ta = document.createElement('textarea'); ta.value = text;
    ta.style.cssText = 'position:fixed;opacity:0;top:0;left:0;';
    document.body.appendChild(ta); ta.select();
    try { document.execCommand('copy'); done(); } catch(e) { alert(text); }
    document.body.removeChild(ta);
  }
}

function copyWA_O(btn) {
  doCopy([
    '*ООО «ОРИОН»*','Общество с ограниченной ответственностью «ОРИОН»','',
    '━━━━━━━━━━━━━━━━━','🗂 *РЕГИСТРАЦИОННЫЕ ДАННЫЕ*','━━━━━━━━━━━━━━━━━',
    '🔑 *ИНН:* 9701271862','🔑 *КПП:* 770101001','📋 *ОГРН:* 1237700940982',
    '🗓 *Дата регистрации:* 26.12.2023','💰 *Уставный капитал:* 1 100 000 руб.','',
    '━━━━━━━━━━━━━━━━━','📍 *АДРЕС*','━━━━━━━━━━━━━━━━━',
    '101000, г. Москва, вн.тер.г. МО Басманный, ул. Мясницкая, д. 30/1/2, стр. 2, помещ. 1/Ч','',
    '━━━━━━━━━━━━━━━━━','🏦 *БАНК — АО «РАЙФФАЙЗЕНБАНК»*','━━━━━━━━━━━━━━━━━',
    '💳 *Р/с:* 40702 810 3 0000 0298647','🔄 *К/с:* 30101 810 2 0000 0000700',
    '🏷 *БИК:* 044525700','📜 *Лицензия:* № 3292','',
    '━━━━━━━━━━━━━━━━━','🚦 *ЗСК · БАНК РОССИИ*','━━━━━━━━━━━━━━━━━',
    '✅ В чёрных списках ЦБ, ЗСК, 115-ФЗ и 764-П *не найдено*','',
    '━━━━━━━━━━━━━━━━━','👤 *ГЕНЕРАЛЬНЫЙ ДИРЕКТОР*','━━━━━━━━━━━━━━━━━',
    'Магомедов Иса Магомедович'
  ], btn);
}

function copyWA_M(btn) {
  doCopy([
    '*ООО «МК ТРЕЙДИНГ»*','Общество с ограниченной ответственностью «МК ТРЕЙДИНГ»','',
    '━━━━━━━━━━━━━━━━━','🗂 *РЕГИСТРАЦИОННЫЕ ДАННЫЕ*','━━━━━━━━━━━━━━━━━',
    '🔑 *ИНН:* 5074070731','🔑 *КПП:* 507401001','📋 *ОГРН:* 1215000081526',
    '🗓 *Дата регистрации:* 11.08.2021','💰 *Уставный капитал:* 10 000 руб.','',
    '━━━━━━━━━━━━━━━━━','📍 *АДРЕС*','━━━━━━━━━━━━━━━━━',
    '142121, МО, г. Подольск, мкр. Кузнечики, ул. Академика Доллежаля, д. 38, кв. 112','',
    '━━━━━━━━━━━━━━━━━','🏦 *БАНК — ПАО «БАНК ВТБ»*','━━━━━━━━━━━━━━━━━',
    '💳 Реквизиты ВТБ уточнить у представителя компании','',
    '━━━━━━━━━━━━━━━━━','🚦 *ЗСК · БАНК РОССИИ*','━━━━━━━━━━━━━━━━━',
    '✅ В чёрных списках ЦБ, ЗСК, 115-ФЗ и 764-П *не найдено*','',
    '━━━━━━━━━━━━━━━━━','👤 *ГЕНЕРАЛЬНЫЙ ДИРЕКТОР*','━━━━━━━━━━━━━━━━━',
    'Исрафилов Исмаил Исрафилович'
  ], btn);
}

function copyWA_S(btn) {
  doCopy([
    '*ООО «СОКОЛ»*','Общество с ограниченной ответственностью «СОКОЛ»','',
    '━━━━━━━━━━━━━━━━━','🗂 *РЕГИСТРАЦИОННЫЕ ДАННЫЕ*','━━━━━━━━━━━━━━━━━',
    '🔑 *ИНН:* 0522022398','🔑 *КПП:* 052201001','📋 *ОГРН:* 1180571009112',
    '📊 *ОКПО:* 32206625','🗓 *Дата регистрации:* 25.07.2018',
    '💰 *Уставный капитал:* 1 000 000 руб.','🧾 *Система н/о:* ОСНО','',
    '━━━━━━━━━━━━━━━━━','📍 *АДРЕС*','━━━━━━━━━━━━━━━━━',
    '368530, Республика Дагестан, Карабудахкентский р-н, с. Карабудахкент, ул. Акъай Мола, д. 1','',
    '━━━━━━━━━━━━━━━━━','📞 *КОНТАКТЫ*','━━━━━━━━━━━━━━━━━',
    '📱 *Тел:* +7 (965) 568-00-00','📧 *E-mail:* Sokol.19.09@bk.ru','',
    '━━━━━━━━━━━━━━━━━','🏦 *БАНК — АЛЬФА-БАНК (Ставрополь)*','━━━━━━━━━━━━━━━━━',
    '💳 *Р/с:* 40702 810 9 5604 0001894','🔄 *К/с:* 30101 810 0 0000 0000752',
    '🏷 *БИК:* 040702752','',
    '━━━━━━━━━━━━━━━━━','🚦 *ЗСК · БАНК РОССИИ*','━━━━━━━━━━━━━━━━━',
    '✅ В чёрных списках ЦБ, ЗСК, 115-ФЗ и 764-П *не найдено*','',
    '━━━━━━━━━━━━━━━━━','👤 *ГЕНЕРАЛЬНЫЙ ДИРЕКТОР*','━━━━━━━━━━━━━━━━━',
    'Абдуллаев Руслан Гасанович'
  ], btn);
}
</script>
</body>
</html>
