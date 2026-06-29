<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
<title>Juan Falconi - KAM Scorecard Mayo 2025</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{background:#04060e;color:#dce4f5;font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;font-size:14px}
::-webkit-scrollbar{width:4px;height:4px}
::-webkit-scrollbar-thumb{background:#1a2438;border-radius:2px}
.page{display:none;height:100vh;overflow:hidden;flex-direction:column}
.page.active{display:flex}
.scroll{overflow-y:auto;flex:1;padding:14px 16px}
.header{padding:12px 16px;background:linear-gradient(180deg,#0a1020,#04060e);border-bottom:1px solid #1a2438;flex-shrink:0}
.breadcrumb{display:flex;align-items:center;gap:8px;flex-wrap:wrap}
.breadcrumb button{background:none;border:none;color:#4f7ef8;font-size:11px;cursor:pointer;padding:4px 8px;border-radius:6px;font-family:inherit}
.breadcrumb button:last-child{background:#111828;color:#dce4f5;font-weight:700;font-size:12px}
.breadcrumb span{color:#252f48}
.btn-back{padding:6px 14px;border-radius:8px;border:1px solid #1a2438;background:#111828;color:#5a6e96;font-size:11px;font-weight:700;cursor:pointer;font-family:inherit}
.grid-2{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}
.grid-4{display:grid;grid-template-columns:repeat(4,1fr);gap:10px}
.card{background:#0b0f1e;border:1px solid #1a2438;border-radius:10px;overflow:hidden;margin-bottom:12px}
.card-header{padding:10px 14px;border-bottom:1px solid #111828;display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:6px}
.card-header h3{font-size:10px;font-weight:800;color:#5a6e96;letter-spacing:1.5px;text-transform:uppercase}
.card-header small{font-size:9px;color:#252f48}
.card-body{padding:8px 12px}
.kpi-box{background:#0d1224;border:1px solid #1a2438;border-radius:8px;padding:10px 12px}
.kpi-box label{font-size:9px;color:#5a6e96;text-transform:uppercase;letter-spacing:.5px;display:block;margin-bottom:4px}
.kpi-box .val{font-size:20px;font-weight:900;font-family:monospace}
.kpi-box .sub{font-size:10px;color:#5a6e96;margin-top:3px}
.bar-wrap{background:#111828;border-radius:99px;height:6px;overflow:hidden;margin-top:4px}
.bar{height:100%;border-radius:99px;transition:width .5s ease}
.pill{font-size:11px;font-weight:800;font-family:monospace;padding:2px 8px;border-radius:6px;display:inline-block}
.pill.green{background:#062415;color:#1fd67a}
.pill.yellow{background:#241a04;color:#f5c030}
.pill.red{background:#200404;color:#ef4444}
.tag{font-size:9px;font-weight:700;padding:2px 6px;border-radius:4px;display:inline-block;margin-top:2px}
.row-item{display:grid;gap:8px;align-items:center;padding:8px 10px;border-radius:7px;border-left:3px solid transparent;margin-bottom:3px;cursor:pointer;transition:background .12s}
.row-item:hover{background:#161e30!important}
.row-item.even{background:#0d1224}
.row-item.odd{background:#0b0f1e}
.col-name{font-size:11px;font-weight:600;color:#dce4f5;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.col-val{text-align:right;font-size:14px;font-weight:800;font-family:monospace}
.col-pto{text-align:right;font-size:11px;color:#5a6e96;font-family:monospace}
.col-delta{text-align:right;font-size:11px;font-weight:700;font-family:monospace}
.total-row{background:#0b1840!important;border:1px solid rgba(79,126,248,.3)!important;border-radius:7px;margin-top:4px}
.total-row .col-name{color:#4f7ef8;font-weight:800;font-size:12px}
.total-row .col-val{font-size:15px}
.tabs{display:flex;gap:0;background:#111828;border-radius:8px;padding:3px;margin-bottom:12px;width:fit-content}
.tab{padding:7px 14px;border-radius:6px;border:none;background:transparent;color:#5a6e96;font-size:11px;font-weight:700;cursor:pointer;font-family:inherit;transition:all .15s}
.tab.active{background:#0d1224;color:#dce4f5}
.aging-bar{display:flex;height:9px;border-radius:99px;overflow:hidden;gap:1px}
.ag-120{background:#f5c030}
.ag-150{background:#f97316}
.ag-180{background:#ef4444}
.ag-360{background:#7f1d1d}
.section-kpi{margin-bottom:12px}
.insight{border-left:4px solid;border-radius:8px;padding:9px 12px;margin-bottom:6px;display:flex;gap:10px;align-items:flex-start}
.insight-icon{width:18px;height:18px;border-radius:4px;display:flex;align-items:center;justify-content:center;font-size:10px;font-weight:900;flex-shrink:0;margin-top:1px}
.insight p{font-size:12px;color:#dce4f5;line-height:1.5}
.score-ring{position:relative;flex-shrink:0}
.col-sort{cursor:pointer;user-select:none}
.col-sort:hover{color:#4f7ef8}
</style>
</head>
<body>

<!-- ═══ HOME ═══ -->
<div id="page-home" class="page active">
  <div class="header">
    <div style="display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:10px;margin-bottom:10px">
      <div>
        <div style="font-size:9px;letter-spacing:3px;color:#4f7ef8;font-weight:700;margin-bottom:3px">KAM SCORECARD · MAYO 2025 · CADENAS A</div>
        <div style="font-size:22px;font-weight:900;background:linear-gradient(120deg,#dce4f5,#7b9ef0,#a78bfa);-webkit-background-clip:text;-webkit-text-fill-color:transparent">Juan Falconi</div>
        <div style="font-size:10px;color:#5a6e96;margin-top:2px">Presupuesto vs Real · Sell-In · Sell-Out · Consignacion</div>
      </div>
      <div style="display:flex;align-items:center;gap:10px">
        <canvas id="scoreCanvas" width="68" height="68"></canvas>
        <div id="globalKpis" style="display:flex;gap:8px;flex-wrap:wrap"></div>
      </div>
    </div>
    <div class="tabs" id="mainTabs">
      <button class="tab active" onclick="showTab('si')">Sell-In</button>
      <button class="tab" onclick="showTab('so')">Sell-Out</button>
      <button class="tab" onclick="showTab('consign')">Consignacion +120d</button>
      <button class="tab" onclick="showTab('modelos')">Top Modelos</button>
    </div>
  </div>
  <div class="scroll" id="homeContent"></div>
</div>

<!-- ═══ DRILL ═══ -->
<div id="page-drill" class="page">
  <div class="header">
    <div class="breadcrumb" id="drillBreadcrumb"></div>
  </div>
  <div class="scroll" id="drillContent"></div>
</div>

<script>
// ═══════════════════════════════════════════════
// DATA
// ═══════════════════════════════════════════════
var SI_CAD=[
  {c:"MARCIMEX",    vta:322,pto:749,col:"#4f7ef8"},
  {c:"LA GANGA",   vta:295,pto:455,col:"#1fd67a"},
  {c:"UNICOMER",   vta:247,pto:633,col:"#f5c030"},
  {c:"CORP. JARRIN",vta:30, pto:159,col:"#f97316"},
  {c:"ASANTECORP", vta:12, pto:50, col:"#a78bfa"}
];
var SI_CAT=[
  {cat:"UTILITARIA",    vta:388,pto:898,col:"#4f7ef8"},
  {cat:"ENDURO",        vta:186,pto:328,col:"#1fd67a"},
  {cat:"DEPORTIVA",     vta:182,pto:450,col:"#f43f5e"},
  {cat:"SCOOTER",       vta:86, pto:155,col:"#22d3ee"},
  {cat:"CABALLITO",     vta:37, pto:136,col:"#a78bfa"},
  {cat:"DOBLE PROP.",   vta:24, pto:61, col:"#f97316"},
  {cat:"CLASICA",       vta:2,  pto:16, col:"#f5c030"},
  {cat:"CUADRON",       vta:1,  pto:2,  col:"#22c55e"}
];
var SO_CAD=[
  {c:"MARCIMEX",  so:405,pto:790,col:"#4f7ef8"},
  {c:"UNICOMER",  so:360,pto:657,col:"#f5c030"},
  {c:"LA GANGA",  so:251,pto:462,col:"#1fd67a"},
  {c:"CRESA",     so:145,pto:278,col:"#22d3ee"},
  {c:"UNNOPARTS", so:111,pto:248,col:"#f43f5e"},
  {c:"JAHER",     so:31, pto:94, col:"#84cc16"}
];
var SO_CAT=[
  {c:"MARCIMEX",cat:"UTILITARIA",so:215},{c:"MARCIMEX",cat:"ENDURO",so:85},{c:"MARCIMEX",cat:"DEPORTIVA",so:63},{c:"MARCIMEX",cat:"SCOOTER",so:20},{c:"MARCIMEX",cat:"DOBLE PROP.",so:9},{c:"MARCIMEX",cat:"CABALLITO",so:8},{c:"MARCIMEX",cat:"CUADRON",so:5},
  {c:"UNICOMER",cat:"UTILITARIA",so:120},{c:"UNICOMER",cat:"DEPORTIVA",so:86},{c:"UNICOMER",cat:"ENDURO",so:63},{c:"UNICOMER",cat:"SCOOTER",so:56},{c:"UNICOMER",cat:"CABALLITO",so:30},{c:"UNICOMER",cat:"DOBLE PROP.",so:4},{c:"UNICOMER",cat:"CLASICA",so:1},
  {c:"LA GANGA",cat:"UTILITARIA",so:70},{c:"LA GANGA",cat:"DEPORTIVA",so:59},{c:"LA GANGA",cat:"ENDURO",so:58},{c:"LA GANGA",cat:"SCOOTER",so:35},{c:"LA GANGA",cat:"DOBLE PROP.",so:15},{c:"LA GANGA",cat:"CABALLITO",so:14},
  {c:"CRESA",cat:"UTILITARIA",so:109},{c:"CRESA",cat:"SCOOTER",so:27},{c:"CRESA",cat:"ENDURO",so:3},{c:"CRESA",cat:"DOBLE PROP.",so:3},{c:"CRESA",cat:"CUADRON",so:2},{c:"CRESA",cat:"DEPORTIVA",so:1},
  {c:"UNNOPARTS",cat:"DEPORTIVA",so:48},{c:"UNNOPARTS",cat:"ENDURO",so:18},{c:"UNNOPARTS",cat:"UTILITARIA",so:17},{c:"UNNOPARTS",cat:"SCOOTER",so:13},{c:"UNNOPARTS",cat:"DOBLE PROP.",so:10},{c:"UNNOPARTS",cat:"CUADRON",so:2},{c:"UNNOPARTS",cat:"CABALLITO",so:2},{c:"UNNOPARTS",cat:"CLASICA",so:1},
  {c:"JAHER",cat:"UTILITARIA",so:22},{c:"JAHER",cat:"ENDURO",so:5},{c:"JAHER",cat:"DEPORTIVA",so:3},{c:"JAHER",cat:"CLASICA",so:1}
];
var SO_TIENDA=[
  {c:"MARCIMEX",ag:"MX EL EMPALME (118)",so:22,pto:22},{c:"MARCIMEX",ag:"MX MILAGRO (110)",so:18,pto:25},{c:"MARCIMEX",ag:"MP ATACAMES",so:15,pto:21},{c:"MARCIMEX",ag:"MP XP NARANJAL",so:14,pto:24},{c:"MARCIMEX",ag:"MX BABAHOYO (155)",so:13,pto:20},{c:"MARCIMEX",ag:"MX XP SANTA LUCIA",so:13,pto:23},{c:"MARCIMEX",ag:"MX VINCES (129)",so:12,pto:30},{c:"MARCIMEX",ag:"MP QUININDE",so:11,pto:11},{c:"MARCIMEX",ag:"MX PORTOVIEJO CHILE",so:11,pto:27},{c:"MARCIMEX",ag:"MP MILAGRO",so:10,pto:25},{c:"MARCIMEX",ag:"MP STO DOMINGO CENTRO",so:9,pto:12},{c:"MARCIMEX",ag:"MX XP QUINSALOMA",so:8,pto:12},{c:"MARCIMEX",ag:"MX XP FLAVIO ALFARO",so:7,pto:8},{c:"MARCIMEX",ag:"MX XP TOSAGUA",so:7,pto:7},{c:"MARCIMEX",ag:"MX BUCAY (116)",so:7,pto:15},{c:"MARCIMEX",ag:"MX GYE PEDRO CARBO",so:7,pto:22},{c:"MARCIMEX",ag:"MX ATACAMES",so:6,pto:8},{c:"MARCIMEX",ag:"MX CALCETA",so:6,pto:13},{c:"MARCIMEX",ag:"MX DAULE (107)",so:6,pto:22},{c:"MARCIMEX",ag:"MX CHONE (133)",so:6,pto:12},
  {c:"UNICOMER",ag:"ART MOTORS LA LIBERTAD 3673",so:13,pto:16},{c:"UNICOMER",ag:"ART MOTORS PORTOVIEJO 3669",so:13,pto:6},{c:"UNICOMER",ag:"ART HOGAR LIBERTAD 3684",so:11,pto:17},{c:"UNICOMER",ag:"ART MOTORS MILAGRO 3665",so:10,pto:13},{c:"UNICOMER",ag:"TIENDA PORTETE 936",so:9,pto:11},{c:"UNICOMER",ag:"TV ARTEFACTA BABAHOYO 3657",so:7,pto:4},{c:"UNICOMER",ag:"TIENDA NARANJAL 716",so:7,pto:8},{c:"UNICOMER",ag:"ART MOTORS AKT 38 3675",so:6,pto:8},{c:"UNICOMER",ag:"ART MOTORS MANTA 3670",so:6,pto:9},{c:"UNICOMER",ag:"TV ARTEFACTA 9 OCT 3618",so:6,pto:8},{c:"UNICOMER",ag:"TV LA PRENSA 3340",so:6,pto:8},{c:"UNICOMER",ag:"TIENDA MANTA 1313",so:6,pto:11},{c:"UNICOMER",ag:"TIENDA SAT PEDRO CARBO 1038",so:6,pto:5},{c:"UNICOMER",ag:"TIENDA SAT SALITRE 1061",so:6,pto:13},{c:"UNICOMER",ag:"ART MOTORS BABAHOYO 3667",so:5,pto:5},{c:"UNICOMER",ag:"ART MOTORS EL RECREO 3671",so:5,pto:13},{c:"UNICOMER",ag:"ART MOTORS LA PRENSA 3672",so:5,pto:9},{c:"UNICOMER",ag:"ART MOTORS MACAS 3682",so:5,pto:2},{c:"UNICOMER",ag:"PORTAL SHOPPING 3521",so:5,pto:4},{c:"UNICOMER",ag:"TIENDA COCA 1602",so:5,pto:3},
  {c:"LA GANGA",ag:"Portoviejo 4",so:7,pto:5},{c:"LA GANGA",ag:"BABA",so:5,pto:1},{c:"LA GANGA",ag:"CALIFORNIA",so:5,pto:8},{c:"LA GANGA",ag:"GMOTOS MILAGRO",so:5,pto:15},{c:"LA GANGA",ag:"GMOTOS NARANJAL",so:5,pto:12},{c:"LA GANGA",ag:"GMOTOS VINCES",so:5,pto:10},{c:"LA GANGA",ag:"POSORJA",so:5,pto:2},{c:"LA GANGA",ag:"GMOTOS PORTOVIEJO",so:4,pto:7},{c:"LA GANGA",ag:"GMOTOS PEDERNALES",so:4,pto:5},{c:"LA GANGA",ag:"MANTA",so:4,pto:5},{c:"LA GANGA",ag:"NARANJAL",so:4,pto:6},{c:"LA GANGA",ag:"SANTA LUCIA",so:4,pto:1},{c:"LA GANGA",ag:"TULCAN",so:4,pto:3},{c:"LA GANGA",ag:"9 DE OCTUBRE 5",so:3,pto:7},{c:"LA GANGA",ag:"GMOTOS CHONE",so:3,pto:6},{c:"LA GANGA",ag:"GMOTOS LA CONCORDIA",so:3,pto:5},{c:"LA GANGA",ag:"GMOTOS MANTA",so:3,pto:8},{c:"LA GANGA",ag:"DURAN SHOPPING",so:3,pto:5},{c:"LA GANGA",ag:"COTOCOLLAO 2",so:3,pto:6},{c:"LA GANGA",ag:"7 LAGOS",so:3,pto:2},
  {c:"CRESA",ag:"CRECOS PORTOVIEJO 2",so:6,pto:5},{c:"CRESA",ag:"MOTOZONE VINCES",so:6,pto:3},{c:"CRESA",ag:"ORVE PORTOVIEJO 3",so:6,pto:4},{c:"CRESA",ag:"CRECOS PARQUE CALIFORNIA",so:5,pto:4},{c:"CRESA",ag:"CRECOS NARANJAL",so:4,pto:4},{c:"CRESA",ag:"CRECOS RIOCENTRO SUR",so:4,pto:4},{c:"CRESA",ag:"ORVE ESMERALDAS",so:4,pto:2},{c:"CRESA",ag:"CRECOS 9 OCT 1",so:3,pto:3},{c:"CRESA",ag:"CRECOS MILAGRO",so:3,pto:4},{c:"CRESA",ag:"ORVE LA PRENSA",so:2,pto:3},
  {c:"UNNOPARTS",ag:"10 DE AGOSTO",so:10,pto:20},{c:"UNNOPARTS",ag:"GYE ALBORADA",so:7,pto:12},{c:"UNNOPARTS",ag:"PORTOVIEJO",so:7,pto:7},{c:"UNNOPARTS",ag:"MILAGRO",so:6,pto:17},{c:"UNNOPARTS",ag:"CALDERON",so:5,pto:5},{c:"UNNOPARTS",ag:"GYE 9 OCT",so:5,pto:14},{c:"UNNOPARTS",ag:"NARANJAL",so:5,pto:7},{c:"UNNOPARTS",ag:"SHYRIS",so:5,pto:10},{c:"UNNOPARTS",ag:"STO DOMINGO",so:5,pto:4},{c:"UNNOPARTS",ag:"STO DOMINGO 3",so:5,pto:5},
  {c:"JAHER",ag:"DAU. Daule",so:5,pto:4},{c:"JAHER",ag:"MLG. Milagro",so:4,pto:5},{c:"JAHER",ag:"BBH. Babahoyo",so:3,pto:4},{c:"JAHER",ag:"GYE California II",so:3,pto:5},{c:"JAHER",ag:"PTV. Portoviejo III",so:3,pto:4},{c:"JAHER",ag:"OTAVALO",so:2,pto:2},{c:"JAHER",ag:"SEL. La Libertad",so:2,pto:3}
];
var SI_MOD=[
  {c:"MARCIMEX",desc:"DY150 WORKFORCE.",cat:"UTILITARIA",vta:131,pto:250},
  {c:"MARCIMEX",desc:"DY180 WORKFORCE PRO",cat:"UTILITARIA",vta:46,pto:40},
  {c:"UNICOMER",desc:"DY150 WORKFORCE.",cat:"UTILITARIA",vta:29,pto:80},
  {c:"MARCIMEX",desc:"DY200 SCORPION",cat:"DEPORTIVA",vta:28,pto:38},
  {c:"UNICOMER",desc:"DY200 WING EVO II",cat:"DEPORTIVA",vta:28,pto:65},
  {c:"LA GANGA",desc:"DY180 WORKFORCE PRO",cat:"UTILITARIA",vta:27,pto:13},
  {c:"LA GANGA",desc:"DY250 SCORPION",cat:"DEPORTIVA",vta:26,pto:37},
  {c:"LA GANGA",desc:"DY200 WING EVO II",cat:"DEPORTIVA",vta:26,pto:62},
  {c:"LA GANGA",desc:"DY150 WORKFORCE.",cat:"UTILITARIA",vta:24,pto:60},
  {c:"LA GANGA",desc:"DY200 CRUCERO",cat:"UTILITARIA",vta:22,pto:27},
  {c:"MARCIMEX",desc:"DY200 WING EVO II",cat:"DEPORTIVA",vta:22,pto:59},
  {c:"UNICOMER",desc:"DY200 CRUCERO",cat:"UTILITARIA",vta:22,pto:40},
  {c:"MARCIMEX",desc:"DY250 SCORPION",cat:"DEPORTIVA",vta:21,pto:37},
  {c:"UNICOMER",desc:"DY200 SCORPION",cat:"DEPORTIVA",vta:19,pto:10},
  {c:"LA GANGA",desc:"DY180 S1 ADV CROSS",cat:"ENDURO",vta:16,pto:18},
  {c:"UNICOMER",desc:"DY250 SCORPION",cat:"DEPORTIVA",vta:16,pto:44},
  {c:"LA GANGA",desc:"DY250 WOLF",cat:"ENDURO",vta:15,pto:12},
  {c:"LA GANGA",desc:"DY150 EAGLE 5",cat:"UTILITARIA",vta:15,pto:14},
  {c:"UNICOMER",desc:"DY180 WORKFORCE PRO",cat:"UTILITARIA",vta:14,pto:28},
  {c:"UNICOMER",desc:"DY125 TANQ",cat:"UTILITARIA",vta:13,pto:43},
  {c:"LA GANGA",desc:"DY250 GP-1 R",cat:"ENDURO",vta:13,pto:17},
  {c:"LA GANGA",desc:"DY200 EAGLE Z",cat:"ENDURO",vta:13,pto:15},
  {c:"MARCIMEX",desc:"DY200 CRUCERO",cat:"UTILITARIA",vta:12,pto:22},
  {c:"LA GANGA",desc:"DY200 SCORPION",cat:"DEPORTIVA",vta:12,pto:12},
  {c:"LA GANGA",desc:"DY150 BIT SE",cat:"UTILITARIA",vta:12,pto:17},
  {c:"MARCIMEX",desc:"DY150 CRUCERO",cat:"UTILITARIA",vta:12,pto:55},
  {c:"UNICOMER",desc:"DY180 S1 ADV CROSS",cat:"ENDURO",vta:11,pto:33},
  {c:"UNICOMER",desc:"DY200 PREDATOR",cat:"DEPORTIVA",vta:10,pto:12},
  {c:"UNICOMER",desc:"DY200 EAGLE Z",cat:"ENDURO",vta:10,pto:18},
  {c:"UNICOMER",desc:"DY150 CRUCERO",cat:"UTILITARIA",vta:10,pto:60},
  {c:"LA GANGA",desc:"DY125 TANQ",cat:"UTILITARIA",vta:9,pto:19},
  {c:"UNICOMER",desc:"DY150 EAGLE 5",cat:"UTILITARIA",vta:8,pto:24},
  {c:"LA GANGA",desc:"DY300 EVEREST",cat:"ENDURO",vta:8,pto:5},
  {c:"LA GANGA",desc:"DY150 DYNAMIC PRO",cat:"UTILITARIA",vta:8,pto:18},
  {c:"MARCIMEX",desc:"DY150 BIT SE",cat:"UTILITARIA",vta:7,pto:28},
  {c:"CORP. JARRIN",desc:"DY150 WORKFORCE.",cat:"UTILITARIA",vta:7,pto:45},
  {c:"LA GANGA",desc:"DY200 SHARK",cat:"DEPORTIVA",vta:7,pto:7},
  {c:"MARCIMEX",desc:"DY150 EAGLE 5",cat:"UTILITARIA",vta:6,pto:29},
  {c:"CORP. JARRIN",desc:"DY200 CRUCERO",cat:"UTILITARIA",vta:6,pto:14},
  {c:"UNICOMER",desc:"DY125 CX7 PRO",cat:"UTILITARIA",vta:3,pto:13},
  {c:"CORP. JARRIN",desc:"DY250 SCORPION",cat:"DEPORTIVA",vta:5,pto:27},
  {c:"ASANTECORP",desc:"DY200 WING EVO II",cat:"DEPORTIVA",vta:4,pto:6},
  {c:"MARCIMEX",desc:"DY125 TANQ",cat:"UTILITARIA",vta:4,pto:42},
  {c:"CORP. JARRIN",desc:"DY250 GP-1",cat:"ENDURO",vta:3,pto:6},
  {c:"CORP. JARRIN",desc:"DY180 WORKFORCE PRO",cat:"UTILITARIA",vta:3,pto:7}
];
var CONSIGN=[
  {c:"UNICOMER",d120:0,d150:12,d180:95,d360:19,col:"#f5c030",
   tiendas:[
     {t:"ART MOTORS MILAGRO 3665",d120:0,d150:0,d180:5,d360:3},
     {t:"ART MOTORS 3S 3720",d120:0,d150:0,d180:4,d360:2},
     {t:"ART MOTORS MANTA 3670",d120:0,d150:1,d180:3,d360:1},
     {t:"ART HOGAR LIBERTAD 3684",d120:0,d150:0,d180:2,d360:1},
     {t:"ART MOTORS DAULE 3666",d120:0,d150:1,d180:2,d360:0},
     {t:"TIENDA PLAYAS 945",d120:0,d150:2,d180:2,d360:0},
     {t:"ART MOTORS EL RECREO",d120:0,d150:0,d180:1,d360:1},
     {t:"ART HOGAR IBARRA 3687",d120:0,d150:0,d180:0,d360:1},
     {t:"ART MOTORS CALIFORNIA",d120:0,d150:1,d180:1,d360:0},
     {t:"ART MOTORS LA LIBERTAD",d120:0,d150:0,d180:2,d360:0}
   ],
   modelos:[{m:"DY200 CRUCERO",tot:18},{m:"DY150 CRUCERO",tot:15},{m:"DY125 TANQ",tot:12},{m:"DY125 CX7 PRO",tot:10},{m:"DY180 S1 ADVENTURE",tot:9},{m:"DY200 PREDATOR",tot:8},{m:"DY250 TEKKEN EVO",tot:7},{m:"DY200 WING EVO II",tot:6},{m:"DY150 EAGLE 5",tot:5}]
  },
  {c:"LA GANGA",d120:34,d150:11,d180:67,d360:8,col:"#1fd67a",
   tiendas:[
     {t:"GMOTOS CHONE",d120:3,d150:0,d180:2,d360:0},
     {t:"GMOTOS VINCES",d120:2,d150:1,d180:2,d360:0},
     {t:"GMOTOS EL CARMEN",d120:2,d150:0,d180:2,d360:1},
     {t:"GMOTOS TENA",d120:2,d150:1,d180:2,d360:0},
     {t:"GMOTOS LA CONCORDIA",d120:1,d150:1,d180:2,d360:0},
     {t:"RIOBAMBA 2",d120:2,d150:0,d180:2,d360:0},
     {t:"GMOTOS PLAYAS",d120:1,d150:1,d180:1,d360:1},
     {t:"GMOTOS LA LIBERTAD",d120:2,d150:0,d180:2,d360:0},
     {t:"GMOTOS NARANJITO",d120:2,d150:1,d180:1,d360:0},
     {t:"GMOTOS PEDERNALES",d120:1,d150:0,d180:2,d360:1}
   ],
   modelos:[{m:"DY200 CRUCERO",tot:14},{m:"DY150 CRUCERO",tot:12},{m:"DY150 EAGLE 5",tot:11},{m:"DY125 TANQ",tot:8},{m:"DY250 GP-1",tot:8},{m:"DY200 WING EVO II",tot:6},{m:"DY125 BIT",tot:6},{m:"DY150 WORKFORCE",tot:5}]
  },
  {c:"MARCIMEX",d120:4,d150:2,d180:18,d360:2,col:"#4f7ef8",
   tiendas:[
     {t:"MX ECOMMERCE CS",d120:2,d150:1,d180:3,d360:1},
     {t:"MP QUEVEDO",d120:1,d150:0,d180:2,d360:1},
     {t:"MX GYE CARBO",d120:0,d150:1,d180:2,d360:0},
     {t:"MP SANTO DOMINGO",d120:1,d150:0,d180:2,d360:0},
     {t:"MX EL EMPALME",d120:0,d150:0,d180:2,d360:0}
   ],
   modelos:[{m:"DY150 WORKFORCE.",tot:8},{m:"DY200 CRUCERO",tot:5},{m:"DY180 WORKFORCE PRO",tot:4},{m:"DY125 TANQ",tot:3},{m:"DY150 EAGLE 5",tot:2}]
  },
  {c:"CORP. JARRIN",d120:0,d150:0,d180:1,d360:0,col:"#f97316",
   tiendas:[{t:"JARRIN HERRERA PRINCIPAL",d120:0,d150:0,d180:1,d360:0}],
   modelos:[{m:"DY250 SCRAMBLER",tot:1}]
  },
  {c:"ASANTECORP",d120:0,d150:0,d180:1,d360:0,col:"#a78bfa",
   tiendas:[{t:"ASANTECORP PRINCIPAL",d120:0,d150:0,d180:1,d360:0}],
   modelos:[{m:"DY200 WING EVO II",tot:1}]
  }
];
var CATCOL={"UTILITARIA":"#4f7ef8","ENDURO":"#1fd67a","DEPORTIVA":"#f43f5e","SCOOTER":"#22d3ee","CABALLITO":"#a78bfa","DOBLE PROP.":"#f97316","CLASICA":"#f5c030","CUADRON":"#22c55e"};
var CCOL={"MARCIMEX":"#4f7ef8","LA GANGA":"#1fd67a","UNICOMER":"#f5c030","CORP. JARRIN":"#f97316","ASANTECORP":"#a78bfa","CRESA":"#22d3ee","UNNOPARTS":"#f43f5e","JAHER":"#84cc16"};

// ═══════════════════════════════════════════════
// UTILS
// ═══════════════════════════════════════════════
function pct(r,b){return b>0?(r/b)*100:0}
function pillClass(v){return v>=100?"green":v>=80?"yellow":"red"}
function pillHtml(v){return '<span class="pill '+pillClass(v)+'">'+v.toFixed(1)+'%</span>'}
function barHtml(v,color){var w=Math.min(v,120)/120*100;return '<div class="bar-wrap"><div class="bar" style="width:'+w+'%;background:'+color+'"></div></div>'}
function deltaHtml(vta,pto,col){if(!pto)return '<span style="color:#5a6e96">--</span>';var d=vta-pto;return '<span style="color:'+(d>=0?"#1fd67a":"#ef4444")+'">'+(d>=0?"+":"")+d+'</span>'}
function agBarHtml(d120,d150,d180,d360){
  var tot=d120+d150+d180+d360;
  if(!tot)return '<div style="font-size:10px;color:#1fd67a">Sin criticos</div>';
  var h='<div class="aging-bar">';
  if(d120)h+='<div class="ag-120" style="flex:'+d120+'"></div>';
  if(d150)h+='<div class="ag-150" style="flex:'+d150+'"></div>';
  if(d180)h+='<div class="ag-180" style="flex:'+d180+'"></div>';
  if(d360)h+='<div class="ag-360" style="flex:'+d360+'"></div>';
  return h+'</div>';
}
function scoreColor(s){return s>=80?"#1fd67a":s>=65?"#f5c030":s>=50?"#f97316":"#ef4444"}

// Draw score ring on canvas
function drawScore(score){
  var c=document.getElementById('scoreCanvas');
  if(!c)return;
  var ctx=c.getContext('2d');
  var cx=34,cy=34,r=28,lw=6;
  ctx.clearRect(0,0,68,68);
  ctx.beginPath();ctx.arc(cx,cy,r,0,Math.PI*2);ctx.strokeStyle='#1a2438';ctx.lineWidth=lw;ctx.stroke();
  var angle=-Math.PI/2+Math.PI*2*(score/100);
  ctx.beginPath();ctx.arc(cx,cy,r,-Math.PI/2,angle);
  ctx.strokeStyle=scoreColor(score);ctx.lineWidth=lw;ctx.lineCap='round';ctx.stroke();
  ctx.fillStyle=scoreColor(score);ctx.font='bold 16px monospace';ctx.textAlign='center';ctx.textBaseline='middle';
  ctx.fillText(score,cx,cy);
}

// ═══════════════════════════════════════════════
// TABLE BUILDER
// ═══════════════════════════════════════════════
function buildTable(rows, opts){
  // opts: {nameKey, nameLabel, colorKey, vta, pto, onClick, soMode}
  var soMode=opts.soMode;
  var vtaKey=soMode?"so":"vta";
  var sorted=[].concat(rows);
  var totVta=sorted.reduce(function(s,r){return s+(r[vtaKey]||0)},0);
  var totPto=sorted.reduce(function(s,r){return s+(r.pto||0)},0);
  var maxV=Math.max.apply(null,sorted.map(function(r){return r[vtaKey]||0}));
  var tCumpl=pct(totVta,totPto);
  var grid="1fr 58px 58px 88px 100px 50px";
  var h='<div style="display:grid;grid-template-columns:'+grid+';gap:6px;padding:5px 10px 3px;margin-bottom:2px">';
  h+='<div style="font-size:9px;color:#5a6e96;font-weight:700">'+opts.nameLabel+'</div>';
  h+='<div style="font-size:9px;color:#5a6e96;font-weight:700;text-align:right">REAL</div>';
  h+='<div style="font-size:9px;color:#5a6e96;font-weight:700;text-align:right">PTO</div>';
  h+='<div style="font-size:9px;color:#5a6e96;font-weight:700;text-align:center">CUMPL.</div>';
  h+='<div style="font-size:9px;color:#5a6e96;font-weight:700">BARRA</div>';
  h+='<div style="font-size:9px;color:#5a6e96;font-weight:700;text-align:right">DELTA</div>';
  h+='</div>';
  sorted.forEach(function(r,i){
    var vta=r[vtaKey]||0;
    var pto=r.pto||0;
    var p=pct(vta,pto);
    var col=r[opts.colorKey||"col"]||opts.defaultColor||"#4f7ef8";
    var clk=opts.onClick?'onclick="'+opts.onClick+'(\''+r[opts.nameKey||"c"]+'\')"':'';
    h+='<div class="row-item '+(i%2===0?"even":"odd")+'" style="grid-template-columns:'+grid+';border-left-color:'+col+'" '+clk+'>';
    h+='<div class="col-name">'+r[opts.nameKey||"c"]+'</div>';
    h+='<div class="col-val" style="color:'+col+'">'+vta+'</div>';
    h+='<div class="col-pto">'+(pto||"--")+'</div>';
    h+='<div style="text-align:center">'+(pto>0?pillHtml(p):'<span style="color:#a78bfa;font-size:10px">s/p</span>')+'</div>';
    h+='<div>'+barHtml(pto>0?p:50, pto>0?(p>=100?"#1fd67a":p>=80?"#f5c030":"#ef4444"):col)+'</div>';
    h+='<div class="col-delta">'+deltaHtml(vta,pto)+'</div>';
    h+='</div>';
  });
  // Total row
  h+='<div class="row-item total-row" style="grid-template-columns:'+grid+';border-left-color:#4f7ef8">';
  h+='<div class="col-name" style="color:#4f7ef8;font-weight:800">TOTAL</div>';
  h+='<div class="col-val" style="font-size:15px;color:#dce4f5">'+totVta+'</div>';
  h+='<div class="col-pto">'+totPto+'</div>';
  h+='<div style="text-align:center">'+pillHtml(tCumpl)+'</div>';
  h+=barHtml(Math.min(tCumpl,120),(tCumpl>=100?"#1fd67a":tCumpl>=80?"#f5c030":"#ef4444"));
  h+='<div class="col-delta">'+deltaHtml(totVta,totPto)+'</div>';
  h+='</div>';
  return h;
}

// ═══════════════════════════════════════════════
// GLOBAL KPI STRIP
// ═══════════════════════════════════════════════
function initGlobal(){
  var siVta=SI_CAD.reduce(function(s,r){return s+r.vta},0);
  var siPto=SI_CAD.reduce(function(s,r){return s+r.pto},0);
  var soVta=SO_CAD.reduce(function(s,r){return s+r.so},0);
  var soPto=SO_CAD.reduce(function(s,r){return s+r.pto},0);
  var cons=CONSIGN.reduce(function(s,r){return s+r.d120+r.d150+r.d180+r.d360},0);
  var c360=CONSIGN.reduce(function(s,r){return s+r.d360},0);
  var score=Math.min(Math.round(Math.min(pct(siVta,siPto),120)*.40+Math.min(pct(soVta,soPto),120)*.30+Math.max(0,100-(cons/350)*100)*.30),100);
  drawScore(score);
  var kpis=[
    {l:"SI Real",v:siVta+"u",p:pct(siVta,siPto)},
    {l:"SI Ppto",v:siPto+"u",p:null,c:"#5a6e96"},
    {l:"SO Real",v:soVta+"u",p:pct(soVta,soPto)},
    {l:"Consign+120",v:cons+"u",c:"#ef4444",sub:c360+" a +360d"}
  ];
  var h="";
  kpis.forEach(function(k){
    var col=k.c||(k.p!==null?scoreColor(k.p):"#5a6e96");
    h+='<div style="background:#0b0f1e;border:1px solid #1a2438;border-radius:8px;padding:6px 12px;text-align:center">';
    h+='<div style="font-size:9px;color:#5a6e96">'+k.l+'</div>';
    h+='<div style="font-size:15px;font-weight:900;color:'+col+';font-family:monospace">'+k.v+'</div>';
    if(k.p!==null&&k.p!==undefined)h+='<div style="margin-top:2px">'+pillHtml(k.p)+'</div>';
    if(k.sub)h+='<div style="font-size:9px;color:#5a6e96">'+k.sub+'</div>';
    h+='</div>';
  });
  document.getElementById('globalKpis').innerHTML=h;
}

// ═══════════════════════════════════════════════
// HOME TABS
// ═══════════════════════════════════════════════
var activeTab='si';
function showTab(t){
  activeTab=t;
  document.querySelectorAll('#mainTabs .tab').forEach(function(b,i){b.classList.remove('active')});
  event.target.classList.add('active');
  renderHome();
}

function renderHome(){
  var h="";
  if(activeTab==='si'){
    h+='<div class="card"><div class="card-header"><h3>SELL-IN POR CADENA - Real vs Presupuesto</h3><span>'+pillHtml(pct(SI_CAD.reduce(function(s,r){return s+r.vta},0),SI_CAD.reduce(function(s,r){return s+r.pto},0)))+'</span></div>';
    h+='<div class="card-body"><div style="font-size:9px;color:#252f48;margin-bottom:6px">Toca una cadena para ver categorias y modelos</div>';
    h+=buildTable(SI_CAD,{nameKey:"c",nameLabel:"CADENA",colorKey:"col",onClick:"drillSICadena"});
    h+='</div></div>';
    h+='<div class="card"><div class="card-header"><h3>SELL-IN POR CATEGORIA - Real vs Presupuesto</h3></div>';
    h+='<div class="card-body"><div style="font-size:9px;color:#252f48;margin-bottom:6px">Toca una categoria para ver modelos</div>';
    h+=buildTable(SI_CAT,{nameKey:"cat",nameLabel:"CATEGORIA",defaultColor:"#4f7ef8",onClick:"drillSICat"});
    h+='</div></div>';
  }
  else if(activeTab==='so'){
    h+='<div class="card"><div class="card-header"><h3>SELL-OUT POR CADENA - Real vs Presupuesto</h3><span>'+pillHtml(pct(SO_CAD.reduce(function(s,r){return s+r.so},0),SO_CAD.reduce(function(s,r){return s+r.pto},0)))+'</span></div>';
    h+='<div class="card-body"><div style="font-size:9px;color:#252f48;margin-bottom:6px">Toca para ver por categoria y tiendas</div>';
    h+=buildTable(SO_CAD,{nameKey:"c",nameLabel:"CADENA",colorKey:"col",soMode:true,onClick:"drillSOCadena"});
    h+='</div></div>';
    // SO por categoria consolidado
    var catAgg={};
    SO_CAT.forEach(function(r){catAgg[r.cat]=(catAgg[r.cat]||0)+r.so});
    var catRows=Object.keys(catAgg).map(function(k){return{cat:k,so:catAgg[k],pto:0,col:CATCOL[k]||"#4f7ef8"}}).sort(function(a,b){return b.so-a.so});
    h+='<div class="card"><div class="card-header"><h3>SELL-OUT POR CATEGORIA (consolidado)</h3></div>';
    h+='<div class="card-body">';
    h+=buildTable(catRows,{nameKey:"cat",nameLabel:"CATEGORIA",colorKey:"col",soMode:true});
    h+='</div></div>';
  }
  else if(activeTab==='consign'){
    var totC=CONSIGN.reduce(function(s,r){return s+r.d120+r.d150+r.d180+r.d360},0);
    h+='<div class="card"><div class="card-header"><h3>CONSIGNACION +120 DIAS POR CADENA</h3>';
    h+='<div style="display:flex;gap:8px;align-items:center">';
    [{l:"+120d",c:"#f5c030"},{l:"+180d",c:"#ef4444"},{l:"+360d",c:"#7f1d1d"}].forEach(function(s){
      h+='<div style="display:flex;align-items:center;gap:4px"><div style="width:7px;height:7px;background:'+s.c+';border-radius:2px"></div><span style="font-size:9px;color:#5a6e96">'+s.l+'</span></div>';
    });
    h+='<span style="font-size:12px;font-weight:800;color:#ef4444;font-family:monospace">'+totC+'u</span>';
    h+='</div></div><div class="card-body">';
    h+='<div style="font-size:9px;color:#252f48;margin-bottom:8px">Toca una cadena para ver tiendas y modelos</div>';
    CONSIGN.forEach(function(r){
      var tot=r.d120+r.d150+r.d180+r.d360;
      h+='<div class="row-item even" style="grid-template-columns:140px 1fr 220px 20px;border-left-color:'+r.col+'" onclick="drillConsign(\''+r.c+'\')">';
      h+='<div><div style="font-size:12px;font-weight:700">'+r.c+'</div>';
      h+='<div style="font-size:10px;color:'+(tot>20?"#ef4444":tot>5?"#f5c030":"#1fd67a")+';font-weight:600;margin-top:2px">'+tot+' motos criticas</div></div>';
      h+=agBarHtml(r.d120,r.d150,r.d180,r.d360);
      h+='<div style="display:flex;gap:10px;justify-content:flex-end">';
      [{v:r.d120,c:"#f5c030",l:"+120"},{v:r.d150,c:"#f97316",l:"+150"},{v:r.d180,c:"#ef4444",l:"+180"},{v:r.d360,c:"#7f1d1d",l:"+360"}].forEach(function(s){
        h+='<div style="text-align:center;opacity:'+(s.v===0?0.25:1)+'"><div style="font-size:14px;font-weight:800;color:'+s.c+';font-family:monospace">'+s.v+'</div><div style="font-size:8px;color:#5a6e96">'+s.l+'</div></div>';
      });
      h+='</div><span style="color:#5a6e96;font-size:14px">›</span></div>';
    });
    h+='</div></div>';
  }
  else if(activeTab==='modelos'){
    var top=SI_MOD.slice().sort(function(a,b){return b.vta-a.vta}).slice(0,30);
    var mRows=top.map(function(m){return{c:m.desc+" ("+m.c+")",col:CATCOL[m.cat]||"#4f7ef8",vta:m.vta,pto:m.pto}});
    h+='<div class="card"><div class="card-header"><h3>TOP 30 MODELOS SELL-IN - Real vs Presupuesto</h3></div>';
    h+='<div class="card-body">';
    h+=buildTable(mRows,{nameKey:"c",nameLabel:"MODELO / CADENA",colorKey:"col"});
    h+='</div></div>';
  }
  document.getElementById('homeContent').innerHTML=h;
}

// ═══════════════════════════════════════════════
// DRILL FUNCTIONS
// ═══════════════════════════════════════════════
function showDrill(breadcrumbs, html){
  document.getElementById('page-home').classList.remove('active');
  document.getElementById('page-drill').classList.add('active');
  var bc='<button class="btn-back" onclick="goHome()">← Volver</button>';
  breadcrumbs.forEach(function(b,i){
    bc+='<span>›</span><button'+(i===breadcrumbs.length-1?' style="color:#dce4f5;font-weight:800"':'')+'onclick="goHome()">'+b+'</button>';
  });
  document.getElementById('drillBreadcrumb').innerHTML=bc;
  document.getElementById('drillContent').innerHTML=html;
  document.getElementById('drillContent').scrollTop=0;
}
function goHome(){
  document.getElementById('page-drill').classList.remove('active');
  document.getElementById('page-home').classList.add('active');
}

// DRILL: SI por Cadena
function drillSICadena(cadena){
  var si=SI_CAD.filter(function(r){return r.c===cadena})[0]||{vta:0,pto:0};
  var mods=SI_MOD.filter(function(m){return m.c===cadena}).sort(function(a,b){return b.vta-a.vta});
  var so=SO_CAD.filter(function(r){return r.c===cadena})[0]||{so:0,pto:0};
  var soCats=SO_CAT.filter(function(r){return r.c===cadena}).sort(function(a,b){return b.so-a.so});
  var col=CCOL[cadena]||"#4f7ef8";
  // Cat summary
  var cats={};
  mods.forEach(function(m){if(!cats[m.cat])cats[m.cat]={cat:m.cat,vta:0,pto:0,col:CATCOL[m.cat]||"#4f7ef8"};cats[m.cat].vta+=m.vta;cats[m.cat].pto+=m.pto});
  var catRows=Object.values(cats).sort(function(a,b){return b.vta-a.vta});

  var h='';
  // KPIs
  h+='<div class="grid-4 section-kpi">';
  var pSI=pct(si.vta,si.pto),pSO=pct(so.so,so.pto);
  [{l:"Sell-In Real",v:si.vta+"u",col:col},{l:"Presupuesto SI",v:si.pto+"u",col:"#5a6e96"},{l:"Cumpl. Sell-In",v:pillHtml(pSI),bar:pSI},{l:"Sell-Out",v:so.so+"u / "+so.pto+"u",pill:pSO,col:"#a78bfa"}].forEach(function(k){
    h+='<div class="kpi-box" style="border-top:2px solid '+(k.col||"#4f7ef8")+'">';
    h+='<label>'+k.l+'</label>';
    if(k.pill!==undefined){h+=pillHtml(k.pill);}
    else if(k.bar!==undefined){h+=k.v;h+='<div class="bar-wrap" style="margin-top:6px"><div class="bar" style="width:'+Math.min(k.bar,120)/120*100+'%;background:'+(k.bar>=100?"#1fd67a":k.bar>=80?"#f5c030":"#ef4444")+'"></div></div>';}
    else{h+='<div class="val" style="color:'+(k.col||col)+'">'+k.v+'</div>';}
    h+='</div>';
  });
  h+='</div>';

  // Cat + SO side by side
  h+='<div class="grid-2">';
  h+='<div class="card"><div class="card-header"><h3>SELL-IN POR CATEGORIA</h3></div><div class="card-body">';
  h+=buildTable(catRows,{nameKey:"cat",nameLabel:"CATEGORIA",colorKey:"col"});
  h+='</div></div>';
  h+='<div class="card"><div class="card-header"><h3>SELL-OUT POR CATEGORIA</h3><span style="font-size:11px;font-weight:700;color:#a78bfa;font-family:monospace">'+so.so+'u</span></div><div class="card-body">';
  if(soCats.length){
    var maxSO=Math.max.apply(null,soCats.map(function(r){return r.so}));
    soCats.forEach(function(r){
      var cc=CATCOL[r.cat]||"#4f7ef8";
      h+='<div style="display:grid;grid-template-columns:130px 40px 1fr;gap:6px;align-items:center;padding:5px 8px;background:#0d1224;border-radius:6px;border-left:3px solid '+cc+';margin-bottom:3px">';
      h+='<div style="font-size:11px;color:#dce4f5;font-weight:600;overflow:hidden;text-overflow:ellipsis;white-space:nowrap">'+r.cat+'</div>';
      h+='<div style="text-align:right;font-size:13px;font-weight:800;color:#a78bfa;font-family:monospace">'+r.so+'</div>';
      h+=barHtml(r.so/maxSO*100,"#a78bfa");
      h+='</div>';
    });
  }else{h+='<div style="color:#5a6e96;font-size:11px;padding:10px">Sin datos</div>';}
  h+='</div></div></div>';

  // Modelos
  var mRows=mods.map(function(m){return{c:m.desc,col:CATCOL[m.cat]||"#4f7ef8",vta:m.vta,pto:m.pto}});
  h+='<div class="card"><div class="card-header"><h3>MODELOS - Real vs Presupuesto</h3></div><div class="card-body">';
  h+=buildTable(mRows,{nameKey:"c",nameLabel:"MODELO",colorKey:"col"});
  h+='</div></div>';

  showDrill(["Sell-In",cadena],h);
}

// DRILL: SI por Categoria
function drillSICat(cat){
  var cat_=cat;
  var mods=SI_MOD.filter(function(m){return m.cat===cat_}).sort(function(a,b){return b.vta-a.vta});
  var catData=SI_CAT.filter(function(r){return r.cat===cat_})[0]||{vta:0,pto:0};
  var col=CATCOL[cat_]||"#4f7ef8";
  var soTotal=SO_CAT.filter(function(r){return r.cat===cat_}).reduce(function(s,r){return s+r.so},0);

  // By cadena
  var cads={};
  mods.forEach(function(m){
    if(!cads[m.c])cads[m.c]={c:m.c,col:CCOL[m.c]||"#4f7ef8",vta:0,pto:0,so:0};
    cads[m.c].vta+=m.vta;cads[m.c].pto+=m.pto;
  });
  SO_CAT.filter(function(r){return r.cat===cat_}).forEach(function(r){if(cads[r.c])cads[r.c].so+=r.so});
  var cadRows=Object.values(cads).sort(function(a,b){return b.vta-a.vta});

  var h='';
  var p=pct(catData.vta,catData.pto);
  h+='<div class="grid-4 section-kpi">';
  [{l:"Sell-In Real",v:catData.vta+"u",col:col},{l:"Presupuesto",v:catData.pto+"u",col:"#5a6e96"},{l:"Cumplimiento",bar:p},{l:"Sell-Out",v:soTotal+"u",col:"#a78bfa"}].forEach(function(k){
    h+='<div class="kpi-box" style="border-top:2px solid '+(k.col||col)+'">';
    h+='<label>'+k.l+'</label>';
    if(k.bar!==undefined){h+=pillHtml(k.bar)+'<div class="bar-wrap" style="margin-top:6px"><div class="bar" style="width:'+Math.min(k.bar,120)/120*100+'%;background:'+(k.bar>=100?"#1fd67a":k.bar>=80?"#f5c030":"#ef4444")+'"></div></div>';}
    else{h+='<div class="val" style="color:'+(k.col||col)+'">'+k.v+'</div>';}
    h+='</div>';
  });
  h+='</div>';

  h+='<div class="card"><div class="card-header"><h3>SELL-IN POR CADENA en '+cat_+'</h3></div><div class="card-body">';
  h+=buildTable(cadRows,{nameKey:"c",nameLabel:"CADENA",colorKey:"col"});
  h+='</div></div>';

  var mRows=mods.map(function(m){return{c:m.desc+" ("+m.c+")",col:col,vta:m.vta,pto:m.pto}});
  h+='<div class="card"><div class="card-header"><h3>MODELOS - Real vs Presupuesto</h3></div><div class="card-body">';
  h+=buildTable(mRows,{nameKey:"c",nameLabel:"MODELO / CADENA",colorKey:"col"});
  h+='</div></div>';

  showDrill(["Sell-In x Categoria",cat_],h);
}

// DRILL: SO por Cadena
function drillSOCadena(cadena){
  var soData=SO_CAD.filter(function(r){return r.c===cadena})[0]||{so:0,pto:0};
  var cats=SO_CAT.filter(function(r){return r.c===cadena}).sort(function(a,b){return b.so-a.so});
  var tiendas=SO_TIENDA.filter(function(r){return r.c===cadena}).sort(function(a,b){return b.so-a.so});
  var col=CCOL[cadena]||"#4f7ef8";
  var p=pct(soData.so,soData.pto);

  var h='';
  h+='<div class="grid-3 section-kpi">';
  h+='<div class="kpi-box" style="border-top:2px solid #a78bfa"><label>Sell-Out Real</label><div class="val" style="color:#a78bfa">'+soData.so+'u</div></div>';
  h+='<div class="kpi-box" style="border-top:2px solid #5a6e96"><label>Presupuesto SO</label><div class="val" style="color:#5a6e96">'+soData.pto+'u</div></div>';
  h+='<div class="kpi-box" style="border-top:2px solid '+(p>=100?"#1fd67a":p>=80?"#f5c030":"#ef4444")+'"><label>Cumplimiento</label>'+pillHtml(p)+'<div class="bar-wrap" style="margin-top:8px"><div class="bar" style="width:'+Math.min(p,120)/120*100+'%;background:'+(p>=100?"#1fd67a":p>=80?"#f5c030":"#ef4444")+'"></div></div></div>';
  h+='</div>';

  var catRows=cats.map(function(r){return{c:r.cat,col:CATCOL[r.cat]||"#4f7ef8",so:r.so,pto:0}});
  h+='<div class="card"><div class="card-header"><h3>SELL-OUT POR CATEGORIA</h3></div><div class="card-body">';
  h+=buildTable(catRows,{nameKey:"c",nameLabel:"CATEGORIA",colorKey:"col",soMode:true});
  h+='</div></div>';

  var tRows=tiendas.map(function(r){return{c:r.ag,col:col,so:r.so,pto:r.pto}});
  h+='<div class="card"><div class="card-header"><h3>SELL-OUT vs PRESUPUESTO POR TIENDA</h3></div><div class="card-body">';
  h+=buildTable(tRows,{nameKey:"c",nameLabel:"TIENDA / AGENCIA",colorKey:"col",soMode:true});
  h+='</div></div>';

  showDrill(["Sell-Out",cadena],h);
}

// DRILL: Consignacion por Cadena
function drillConsign(cadena){
  var data=CONSIGN.filter(function(r){return r.c===cadena})[0];
  if(!data)return;
  var col=data.col;
  var tot=data.d120+data.d150+data.d180+data.d360;

  var h='';
  h+='<div class="grid-4 section-kpi">';
  [{l:"Total +120d",v:tot,c:col},{l:"+180 dias",v:data.d180,c:"#ef4444"},{l:"+360 dias",v:data.d360,c:"#7f1d1d"},{l:"+120d exactos",v:data.d120,c:"#f5c030"}].forEach(function(k){
    h+='<div class="kpi-box" style="border-top:3px solid '+k.c+'"><label>'+k.l+'</label><div class="val" style="color:'+k.c+'">'+k.v+'</div></div>';
  });
  h+='</div>';

  h+='<div class="card"><div class="card-body">';
  h+='<div style="font-size:10px;font-weight:800;color:#5a6e96;letter-spacing:1px;margin-bottom:8px">DISTRIBUCION POR ANTIGUEDAD</div>';
  h+='<div style="margin-bottom:8px">'+agBarHtml(data.d120,data.d150,data.d180,data.d360)+'</div>';
  h+='<div style="display:flex;gap:12px">';
  [{l:"+120d",c:"#f5c030",v:data.d120},{l:"+150d",c:"#f97316",v:data.d150},{l:"+180d",c:"#ef4444",v:data.d180},{l:"+360d",c:"#7f1d1d",v:data.d360}].forEach(function(s){
    h+='<div style="text-align:center;opacity:'+(s.v===0?0.3:1)+'"><div style="font-size:20px;font-weight:900;color:'+s.c+';font-family:monospace">'+s.v+'</div><div style="font-size:10px;color:#5a6e96">'+s.l+'</div></div>';
  });
  h+='</div></div></div>';

  h+='<div style="display:flex;gap:0;background:#111828;border-radius:8px;padding:3px;margin-bottom:12px;width:fit-content">';
  h+='<button class="tab active" id="tabTienda" onclick="switchConsignTab(\'tiendas\')">Por Tienda ('+data.tiendas.length+')</button>';
  h+='<button class="tab" id="tabModelo" onclick="switchConsignTab(\'modelos\')">Por Modelo ('+data.modelos.length+')</button>';
  h+='</div>';

  h+='<div id="consignTiendas">';
  data.tiendas.slice().sort(function(a,b){return(b.d120+b.d150+b.d180+b.d360)-(a.d120+a.d150+a.d180+a.d360)}).forEach(function(t){
    var tt=t.d120+t.d150+t.d180+t.d360;
    h+='<div class="card" style="margin-bottom:8px"><div class="card-body">';
    h+='<div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:7px;flex-wrap:wrap;gap:6px">';
    h+='<span style="font-size:12px;font-weight:700">'+t.t+'</span>';
    h+='<div style="display:flex;gap:8px;align-items:center">';
    [{v:t.d120,c:"#f5c030",l:"+120"},{v:t.d150,c:"#f97316",l:"+150"},{v:t.d180,c:"#ef4444",l:"+180"},{v:t.d360,c:"#7f1d1d",l:"+360"}].forEach(function(s){
      if(s.v>0)h+='<div style="text-align:center"><div style="font-size:13px;font-weight:800;color:'+s.c+';font-family:monospace">'+s.v+'</div><div style="font-size:8px;color:#5a6e96">'+s.l+'</div></div>';
    });
    h+='<div style="border-left:1px solid #1a2438;padding-left:8px;text-align:center"><div style="font-size:16px;font-weight:900;color:'+(tt>4?"#ef4444":"#f5c030")+';font-family:monospace">'+tt+'</div><div style="font-size:8px;color:#5a6e96">total</div></div>';
    h+='</div></div>';
    h+=agBarHtml(t.d120,t.d150,t.d180,t.d360);
    h+='</div></div>';
  });
  h+='</div>';

  h+='<div id="consignModelos" style="display:none">';
  var maxM=Math.max.apply(null,data.modelos.map(function(m){return m.tot}));
  data.modelos.forEach(function(m,i){
    h+='<div style="display:grid;grid-template-columns:22px 1fr 50px;gap:8px;align-items:center;padding:8px 10px;background:'+(i%2===0?"#0d1224":"#0b0f1e")+';border-radius:6px;margin-bottom:3px">';
    h+='<div style="font-size:11px;color:'+(i<3?"#f5c030":"#252f48")+';font-weight:800;text-align:center">'+(i+1)+'</div>';
    h+='<div><div style="font-size:12px;color:#dce4f5;font-weight:600;margin-bottom:3px">'+m.m+'</div>'+barHtml(m.tot/maxM*100,col)+'</div>';
    h+='<div style="text-align:right;font-size:15px;font-weight:900;color:'+(m.tot>=10?"#ef4444":"#f97316")+';font-family:monospace">'+m.tot+'</div>';
    h+='</div>';
  });
  h+='</div>';

  showDrill(["Consignacion +120d",cadena],h);
}

function switchConsignTab(tab){
  document.getElementById('consignTiendas').style.display=tab==='tiendas'?"block":"none";
  document.getElementById('consignModelos').style.display=tab==='modelos'?"block":"none";
  document.getElementById('tabTienda').classList.toggle('active',tab==='tiendas');
  document.getElementById('tabModelo').classList.toggle('active',tab==='modelos');
}

// ═══════════════════════════════════════════════
// INIT
// ═══════════════════════════════════════════════
initGlobal();
renderHome();
</script>
</body>
</html>
