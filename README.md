[continental_scorecard.html](https://github.com/user-attachments/files/28719996/continental_scorecard.html)
# COMERCIAL<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Continental - Canal Horizontal Scorecard</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{background:#05080f;color:#dce4f5;font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;font-size:14px}
::-webkit-scrollbar{width:4px;height:4px}
::-webkit-scrollbar-thumb{background:#1a2438;border-radius:2px}
.page{display:none;height:100vh;overflow:hidden;flex-direction:column}
.page.active{display:flex}
.scroll{overflow-y:auto;flex:1;padding:14px 16px}
.hdr{padding:12px 16px;background:linear-gradient(180deg,#0a1020,#05080f);border-bottom:1px solid #1a2438;flex-shrink:0}
.tabs{display:flex;gap:0;background:#0d1120;border-radius:8px;padding:3px;width:fit-content;margin-top:10px}
.tab{padding:7px 14px;border-radius:6px;border:none;background:transparent;color:#5a6e96;font-size:11px;font-weight:700;cursor:pointer;font-family:inherit;transition:all .15s}
.tab.active{background:#151f38;color:#dce4f5}
.card{background:#0b0f1e;border:1px solid #1a2438;border-radius:10px;overflow:hidden;margin-bottom:12px}
.card-hdr{padding:10px 14px;border-bottom:1px solid #0d1120;display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:6px}
.card-hdr h3{font-size:10px;font-weight:800;color:#5a6e96;letter-spacing:1.5px;text-transform:uppercase}
.card-body{padding:8px 12px}
.kpi-box{background:#0d1224;border:1px solid #1a2438;border-radius:8px;padding:10px 12px}
.kpi-box label{font-size:9px;color:#5a6e96;text-transform:uppercase;letter-spacing:.5px;display:block;margin-bottom:4px}
.kpi-val{font-size:20px;font-weight:900;font-family:monospace}
.kpi-sub{font-size:10px;color:#5a6e96;margin-top:3px}
.g2{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.g3{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}
.g4{display:grid;grid-template-columns:repeat(4,1fr);gap:10px}
.g5{display:grid;grid-template-columns:repeat(5,1fr);gap:10px}
.bar-w{background:#111828;border-radius:99px;height:6px;overflow:hidden;margin-top:4px}
.bar{height:100%;border-radius:99px}
.pill{font-size:11px;font-weight:800;font-family:monospace;padding:2px 8px;border-radius:6px;display:inline-block;white-space:nowrap}
.g{background:#062415;color:#1fd67a}
.y{background:#241a04;color:#f5c030}
.r{background:#200404;color:#ef4444}
.b{background:#0b1840;color:#4f7ef8}
.p{background:#160d38;color:#a78bfa}
.row{display:grid;gap:6px;align-items:center;padding:8px 10px;border-radius:7px;border-left:3px solid transparent;margin-bottom:3px;cursor:pointer;transition:background .12s}
.row:hover{background:#161e30!important}
.ev{background:#0d1224}
.od{background:#0b0f1e}
.tot-row{background:#0b1840!important;border:1px solid rgba(79,126,248,.3)!important;border-radius:7px;margin-top:4px}
.btn-back{padding:6px 14px;border-radius:8px;border:1px solid #1a2438;background:#0d1120;color:#5a6e96;font-size:11px;font-weight:700;cursor:pointer;font-family:inherit}
.bc{display:flex;align-items:center;gap:6px;flex-wrap:wrap;margin-bottom:0}
.bc span{color:#252f48;font-size:12px}
.bc b{font-size:13px;font-weight:800;color:#dce4f5;padding:3px 8px;background:#111828;border-radius:6px}
.vcard{border-radius:12px;padding:16px;cursor:pointer;transition:all .2s;border:1px solid transparent}
.vcard:hover{transform:translateY(-2px)}
.sec-title{font-size:10px;font-weight:800;color:#5a6e96;letter-spacing:1.5px;text-transform:uppercase;margin-bottom:8px}
.insight{border-left:4px solid;border-radius:8px;padding:9px 12px;margin-bottom:6px;display:flex;gap:10px;align-items:flex-start}
.insight p{font-size:12px;color:#dce4f5;line-height:1.5}
.badge{font-size:9px;font-weight:700;padding:2px 7px;border-radius:4px;display:inline-block}
</style>
</head>
<body>

<!-- HOME -->
<div id="page-home" class="page active">
  <div class="hdr">
    <div style="display:flex;justify-content:space-between;align-items:flex-start;flex-wrap:wrap;gap:10px">
      <div>
        <div style="font-size:9px;letter-spacing:3px;color:#f97316;font-weight:700;margin-bottom:3px">SCORECARD · CANAL HORIZONTAL · CONTINENTAL</div>
        <div style="font-size:22px;font-weight:900;background:linear-gradient(120deg,#dce4f5,#fb923c,#f5c030);-webkit-background-clip:text;-webkit-text-fill-color:transparent">Electrodomesticos Continental</div>
        <div style="font-size:10px;color:#5a6e96;margin-top:2px">Sell-In · Real vs Presupuesto vs Ano Anterior</div>
      </div>
      <div style="display:flex;align-items:center;gap:10px" id="globalKpis"></div>
    </div>
    <div class="tabs" id="mainTabs">
      <button class="tab active" onclick="showTab('resumen',this)">Resumen</button>
      <button class="tab" onclick="showTab('lineas',this)">Lineas</button>
      <button class="tab" onclick="showTab('skus',this)">Modelos/SKU</button>
      <button class="tab" onclick="showTab('clientes',this)">Clientes</button>
      <button class="tab" onclick="showTab('vendedores',this)">Vendedores</button>
    </div>
  </div>
  <div class="scroll" id="homeContent"></div>
</div>

<!-- DRILL -->
<div id="page-drill" class="page">
  <div class="hdr">
    <div class="bc" id="drillBC"></div>
  </div>
  <div class="scroll" id="drillContent"></div>
</div>

<script>
// ═══════════════════════════════
// DATA REAL DE ARCHIVOS EXCEL
// ═══════════════════════════════

// GLOBAL
var GLOBAL = {ly:10011, ty:8187, pto:6446};

// LINEAS DE PRODUCTO (del archivo VENTAS_POR_PRODUCTO_Y_CLIENTE)
var LINEAS = [
  {cat:"CONGELADOR",        ly:455,  ty:1024, pto:915,  col:"#22d3ee"},
  {cat:"MINI BAR",          ly:446,  ty:846,  pto:665,  col:"#06b6d4"},
  {cat:"REFRIGERADORAS",    ly:380,  ty:780,  pto:884,  col:"#4f7ef8"},
  {cat:"COCINETA",          ly:414,  ty:564,  pto:890,  col:"#f97316"},
  {cat:"CAMPANA DE OLOR",   ly:44,   ty:487,  pto:240,  col:"#a78bfa"},
  {cat:"ENCIMERA",          ly:21,   ty:398,  pto:465,  col:"#c084fc"},
  {cat:"COCINA GAS",        ly:270,  ty:332,  pto:504,  col:"#f59e0b"},
  {cat:"AIRE ACONDICIONADO",ly:725,  ty:331,  pto:440,  col:"#0ea5e9"},
  {cat:"LICUADORA",         ly:155,  ty:282,  pto:350,  col:"#84cc16"},
  {cat:"DISPENSADOR AGUA",  ly:34,   ty:246,  pto:362,  col:"#14b8a6"},
  {cat:"CALEFONES",         ly:217,  ty:190,  pto:0,    col:"#f43f5e"},
  {cat:"VITRINA",           ly:139,  ty:148,  pto:145,  col:"#8b5cf6"},
  {cat:"VINERA",            ly:92,   ty:112,  pto:128,  col:"#ec4899"},
  {cat:"HORNO ELECTRICO",   ly:53,   ty:75,   pto:78,   col:"#ef4444"},
  {cat:"LAVADORAS",         ly:174,  ty:56,   pto:115,  col:"#f97316"},
  {cat:"REGULADOR DE GAS",  ly:6298, ty:2534, pto:0,    col:"#6b7280"},
  {cat:"VENTILACION",       ly:95,   ty:0,    pto:265,  col:"#9ca3af"},
];

// TOP SKUs GLOBALES (data22)
var SKUS = [
  {sku:"CONG33 - CONGELADOR SD-210Q T/V",         cat:"CONGELADOR",        ly:102, ty:272, pto:170, col:"#22d3ee"},
  {sku:"CO195 - COCINETA ALABAMA 6Q",              cat:"COCINETA",          ly:215, ty:255, pto:340, col:"#f97316"},
  {sku:"REF280 - MINIBAR CO-101SS",                cat:"MINI BAR",          ly:0,   ty:233, pto:130, col:"#06b6d4"},
  {sku:"REF246 - REFRIGERADORA BCD-138 VCM",       cat:"REFRIGERADORAS",    ly:0,   ty:227, pto:205, col:"#4f7ef8"},
  {sku:"LIC66 - LICUADORA 500W PN-Y86N",           cat:"LICUADORA",         ly:0,   ty:222, pto:350, col:"#84cc16"},
  {sku:"ENCI005 - ENCIMERA GB7612GB VIDRIO",       cat:"ENCIMERA",          ly:0,   ty:217, pto:230, col:"#c084fc"},
  {sku:"AIRES94 - AC INVERTER CSDC-12DA",          cat:"AIRE ACONDICIONADO",ly:0,   ty:197, pto:300, col:"#0ea5e9"},
  {sku:"REF239 - MINIBAR TAPA VIDRIO CO-101BGD",   cat:"MINI BAR",          ly:40,  ty:174, pto:110, col:"#06b6d4"},
  {sku:"CONG50 - CONGELADOR SD-168Q T/V",          cat:"CONGELADOR",        ly:67,  ty:165, pto:170, col:"#22d3ee"},
  {sku:"REF208WD - REFRIGERADORA MRF-225SS DISP",  cat:"REFRIGERADORAS",    ly:26,  ty:149, pto:160, col:"#4f7ef8"},
  {sku:"CO221 - COCINETA VITORIA 5Q TRIPLE",       cat:"COCINETA",          ly:0,   ty:149, pto:190, col:"#f97316"},
  {sku:"REF138 - REFRIGERADORA BCD-138 NG",        cat:"REFRIGERADORAS",    ly:92,  ty:143, pto:155, col:"#4f7ef8"},
  {sku:"REF234 - REFRIGERADORA DEFROST MRF-192",   cat:"REFRIGERADORAS",    ly:0,   ty:135, pto:160, col:"#4f7ef8"},
  {sku:"REF209 - REFRIGERADORA MRF-265SS",         cat:"REFRIGERADORAS",    ly:0,   ty:127, pto:140, col:"#4f7ef8"},
  {sku:"DISP-008 - DISPENSADOR BOTELLA OCULTA",    cat:"DISPENSADOR AGUA",  ly:29,  ty:126, pto:140, col:"#14b8a6"},
  {sku:"REF237 - REFRIGERADORA DEFROST-K MRF-162", cat:"REFRIGERADORAS",    ly:97,  ty:124, pto:110, col:"#4f7ef8"},
  {sku:"CONG44 - CONGELADOR SD-268Q T/V",          cat:"CONGELADOR",        ly:62,  ty:117, pto:100, col:"#22d3ee"},
  {sku:"CO207 - COCINA CONTINENTAL SANTOS",        cat:"COCINA GAS",        ly:0,   ty:109, pto:70,  col:"#f59e0b"},
  {sku:"CAMP-008 - CAMPANA 90 BLACK",              cat:"CAMPANA DE OLOR",   ly:11,  ty:106, pto:45,  col:"#a78bfa"},
  {sku:"CALEF016 - CALEFON 20LT",                  cat:"CALEFONES",         ly:0,   ty:106, pto:0,   col:"#f43f5e"},
  {sku:"CONG53 - CONGELADOR SD-308Q T/V",          cat:"CONGELADOR",        ly:27,  ty:99,  pto:120, col:"#22d3ee"},
  {sku:"ENCI004 - ENCIMERA WQG5298",               cat:"ENCIMERA",          ly:2,   ty:99,  pto:75,  col:"#c084fc"},
  {sku:"CO220 - COCINETA PALMAS 5Q",               cat:"COCINETA",          ly:0,   ty:93,  pto:190, col:"#f97316"},
  {sku:"CAMP-004 - CAMPANA 60 BLACK",              cat:"CAMPANA DE OLOR",   ly:11,  ty:92,  pto:30,  col:"#a78bfa"},
  {sku:"CONG66 - CONGELADOR BD-250Q M",            cat:"CONGELADOR",        ly:0,   ty:90,  pto:73,  col:"#22d3ee"},
  {sku:"CAMP-006 - CAMPANA 76 BLACK",              cat:"CAMPANA DE OLOR",   ly:10,  ty:88,  pto:40,  col:"#a78bfa"},
  {sku:"ENCI006 - ENCIMERA GB6094GB 4Q VIDRIO",    cat:"ENCIMERA",          ly:6,   ty:82,  pto:160, col:"#c084fc"},
  {sku:"DISP-009 - DISPENSADOR BOTELLON OCULTO",   cat:"DISPENSADOR AGUA",  ly:0,   ty:78,  pto:115, col:"#14b8a6"},
  {sku:"REF284 - MINIBAR CO-101VCM",               cat:"MINI BAR",          ly:0,   ty:72,  pto:55,  col:"#06b6d4"},
  {sku:"CO216 - COCINETA MISURI 2Q",               cat:"COCINETA",          ly:0,   ty:68,  pto:80,  col:"#f97316"},
];

// TOP CLIENTES
var CLIENTES = [
  {cli:"MORALES PUNGUIL GUIDO ENRIQUE",      ty:602, ly:45,  pto:149, col:"#4f7ef8"},
  {cli:"CEPEDA GUACHO ISABEL JOHANNA",        ty:300, ly:400, pto:0,   col:"#1fd67a"},
  {cli:"CASTRO TELLO JUAN ROSENDO",           ty:271, ly:67,  pto:527, col:"#f97316"},
  {cli:"GALLARDO AGUILAR EMANUEL ANDRES",     ty:239, ly:0,   pto:42,  col:"#a78bfa"},
  {cli:"TIENDAS INDUST. ASOC. TIA S.A.",      ty:224, ly:0,   pto:0,   col:"#22d3ee"},
  {cli:"SIMBAINA LOJA SEGUNDO MARCELO",       ty:220, ly:800, pto:7,   col:"#f5c030"},
  {cli:"PEREZ ABAD JUAN FELIX",               ty:196, ly:45,  pto:68,  col:"#f43f5e"},
  {cli:"CRESA-RETAIL S.A.S.",                 ty:167, ly:0,   pto:79,  col:"#06b6d4"},
  {cli:"DISTRIBUIDORA M Y S",                 ty:150, ly:0,   pto:0,   col:"#84cc16"},
  {cli:"ALMC. Y FERRETERIA STAMARIA S.A.",    ty:140, ly:0,   pto:54,  col:"#f97316"},
  {cli:"CARANQUI QUISHPI PEDRO",              ty:122, ly:310, pto:56,  col:"#8b5cf6"},
  {cli:"CORPORACION EL ROSADO S.A",           ty:121, ly:0,   pto:0,   col:"#f59e0b"},
  {cli:"PARCO YUQUILEMA MARIO RUBEN",         ty:120, ly:0,   pto:3,   col:"#14b8a6"},
  {cli:"JARAMILLO AYALA EDISON PAUL",         ty:118, ly:0,   pto:19,  col:"#ec4899"},
  {cli:"GUAYCHA CUENCA JULIO ALCIBAR",        ty:115, ly:0,   pto:4,   col:"#22c55e"},
  {cli:"BRAVO VERA JUAN CARLOS",              ty:115, ly:603, pto:83,  col:"#ef4444"},
  {cli:"DMARCO JUCA DISTRIBUCIONES",          ty:101, ly:1,   pto:1,   col:"#c084fc"},
  {cli:"CEDENO RIVAS ORLANDO FABIAN",         ty:100, ly:0,   pto:0,   col:"#fb923c"},
  {cli:"MENDOZA ALAVA RICCY GERMANIA",        ty:100, ly:0,   pto:0,   col:"#4f7ef8"},
  {cli:"VALDEZ MOROCHO JORGE ARMANDO",        ty:99,  ly:20,  pto:107, col:"#1fd67a"},
];

// VENDEDORES
var VENDEDORES = [
  {
    nombre:"Juan Cordero",
    zona:"SC",
    ly:0, ty:593, pto:571,
    col:"#4f7ef8",
    skus:[
      {sku:"VENTI18 - VENTILADOR 18 OUIF-45-3H",       cat:"VENTILACION",       ly:0,ty:81, pto:1},
      {sku:"VENTI17 - VENTILADOR 18 OUIF 45-6",         cat:"VENTILACION",       ly:0,ty:70, pto:1},
      {sku:"AIRES94 - AC INVERTER CSDC-12DA",           cat:"AIRE ACONDICIONADO",ly:0,ty:61, pto:73},
      {sku:"CL029 - REGULADOR GR-49 DORADO",            cat:"REGULADOR DE GAS",  ly:0,ty:50, pto:0},
      {sku:"DISP-008 - DISPENSADOR BOTELLA OCULTA",     cat:"DISPENSADOR AGUA",  ly:0,ty:45, pto:35},
      {sku:"CO195 - COCINETA ALABAMA 6Q",               cat:"COCINETA",          ly:0,ty:43, pto:51},
      {sku:"VENTI120 - VENTILADOR 18 3 EN 1",           cat:"VENTILACION",       ly:0,ty:30, pto:0},
      {sku:"CO221 - COCINETA VITORIA 5Q TRIPLE",        cat:"COCINETA",          ly:0,ty:21, pto:32},
      {sku:"CONG33 - CONGELADOR SD-210Q T/V",           cat:"CONGELADOR",        ly:0,ty:20, pto:9},
      {sku:"REF138 - REFRIGERADORA BCD-138 NG",         cat:"REFRIGERADORAS",    ly:0,ty:18, pto:9},
      {sku:"LIC66 - LICUADORA 500W PN-Y86N",            cat:"LICUADORA",         ly:0,ty:16, pto:13},
      {sku:"ENCI004 - ENCIMERA WQG5298",                cat:"ENCIMERA",          ly:0,ty:14, pto:2},
      {sku:"TO-18T - HORNO ELECTRICO 20L",              cat:"HORNO ELECTRICO",   ly:0,ty:13, pto:13},
      {sku:"ENCI005 - ENCIMERA GB7612GB VIDRIO",        cat:"ENCIMERA",          ly:0,ty:12, pto:10},
      {sku:"CAMP-005 - CAMPANA 60 INOX",                cat:"CAMPANA DE OLOR",   ly:0,ty:11, pto:2},
    ],
    clientes:[
      {cli:"ALMACENES Y FERRETERIA STAMARIA S.A.",ty:140,pto:54},
      {cli:"MENENDEZ BAZURTO KEVIN ARIEL",        ty:59, pto:8},
      {cli:"CEVALLOS RODRIGUEZ BENIGNO JOSE",     ty:54, pto:16},
      {cli:"SANTOS CENTENO FEDERICO ALBERTO",     ty:50, pto:35},
      {cli:"OSEJOS VALENCIA ANTONIO RENATO",      ty:48, pto:11},
      {cli:"VILLACRESES FIGUEROA PACO ESTEBAN",   ty:36, pto:19},
      {cli:"MACIAS SALTOS JUAN CARLOS",           ty:35, pto:28},
      {cli:"CHAVEZ PISCO FREDDY JACINTO",         ty:34, pto:27},
      {cli:"GUTIERREZ ANCHUNDIA JERSY STEEVEN",   ty:27, pto:18},
      {cli:"CARMIGNIANI GUERRA MILTON FABIAN",    ty:25, pto:21},
    ]
  },
  {
    nombre:"Pablo Flores",
    zona:"Centro",
    ly:249, ty:0, pto:441,
    col:"#f43f5e",
    nota:"Ventas TY negativas segun archivo - revisar con supervision",
    skus:[
      {sku:"CONG33 - CONGELADOR SD-210Q T/V",          cat:"CONGELADOR",     ly:20,ty:44, pto:19},
      {sku:"CONG50 - CONGELADOR SD-168Q T/V",          cat:"CONGELADOR",     ly:3, ty:32, pto:14},
      {sku:"ENCI005 - ENCIMERA GB7612GB VIDRIO",       cat:"ENCIMERA",       ly:0, ty:32, pto:21},
      {sku:"REF246 - REFRIGERADORA BCD-138 VCM",       cat:"REFRIGERADORAS", ly:0, ty:28, pto:12},
      {sku:"CONG44 - CONGELADOR SD-268Q T/V",          cat:"CONGELADOR",     ly:8, ty:28, pto:11},
      {sku:"CO195 - COCINETA ALABAMA 6Q",              cat:"COCINETA",       ly:4, ty:26, pto:19},
      {sku:"LIC66 - LICUADORA 500W PN-Y86N",           cat:"LICUADORA",      ly:0, ty:24, pto:22},
      {sku:"CONG53 - CONGELADOR SD-308Q T/V",          cat:"CONGELADOR",     ly:4, ty:19, pto:13},
      {sku:"REF208WD - REFRIGERADORA MRF-225SS DISP",  cat:"REFRIGERADORAS", ly:0, ty:17, pto:12},
      {sku:"REF237 - REFRIGERADORA DEFROST-K MRF-162", cat:"REFRIGERADORAS", ly:3, ty:15, pto:6},
      {sku:"CONG49 - CONGELADOR BD-400Q",              cat:"CONGELADOR",     ly:1, ty:13, pto:6},
      {sku:"CO221 - COCINETA VITORIA 5Q TRIPLE",       cat:"COCINETA",       ly:0, ty:11, pto:7},
      {sku:"REF234 - REFRIGERADORA DEFROST MRF-192",   cat:"REFRIGERADORAS", ly:0, ty:11, pto:11},
      {sku:"REF239 - MINIBAR TAPA VIDRIO CO-101BGD",   cat:"MINI BAR",       ly:0, ty:10, pto:7},
      {sku:"CONG60 - CONGELADOR BD-500Q",              cat:"CONGELADOR",     ly:1, ty:10, pto:7},
    ],
    clientes:[
      {cli:"ALMACENES MEGA ECONOMAX S.A.S.",         ty:70, pto:16},
      {cli:"TROYA NARANJO TANIA PATRICIA",           ty:47, pto:27},
      {cli:"SANCHEZ CACUANGO JONATHAN ANDRES",       ty:44, pto:34},
      {cli:"TKVELECTROS S.A.",                       ty:43, pto:65},
      {cli:"RAPID PHOTO",                            ty:29, pto:39},
      {cli:"SALAZAR MOLINA MARIELA ELIZABETH",       ty:26, pto:16},
      {cli:"SANCHEZ CACUANGO EDISON GERARDO",        ty:21, pto:11},
      {cli:"CALUGUILLIN QUILUMBAQUIN MAYRA CECILIA", ty:19, pto:5},
      {cli:"GUERRERO QUINTERO JAVIER ERLEY",         ty:17, pto:33},
      {cli:"MONTENEGRO ARCINIEGA ISAC MOISES",       ty:15, pto:0},
    ]
  }
];

// ═══════════════════════════════
// UTILS
// ═══════════════════════════════
function pct(r,b){return b>0?(r/b)*100:0}
function yoy(ty,ly){return ly>0?((ty-ly)/ly)*100:null}
function pc(v,d){d=d||1;return v===null?'--':v.toFixed(d)+'%'}
function pillCls(v){return v>=100?'g':v>=80?'y':'r'}
function pill(v){return '<span class="pill '+pillCls(v)+'">'+v.toFixed(1)+'%</span>'}
function yoyBadge(ty,ly){
  if(!ly||ly===0)return'';
  var d=((ty-ly)/ly)*100;
  var col=d>=0?'#1fd67a':'#ef4444';
  return'<span style="font-size:10px;font-weight:700;color:'+col+';font-family:monospace">'+(d>=0?'▲':'▼')+Math.abs(d).toFixed(0)+'% YoY</span>';
}
function bar(v,col,max){
  max=max||120;
  var w=Math.min(v,max)/max*100;
  return'<div class="bar-w"><div class="bar" style="width:'+w+'%;background:'+col+'"></div></div>';
}
function barColor(v){return v>=100?'#1fd67a':v>=80?'#f5c030':'#ef4444'}

// ═══════════════════════════════
// TABLE BUILDER
// ═══════════════════════════════
var COLS="1fr 50px 55px 55px 85px 95px 50px";
function tHead(){
  return'<div style="display:grid;grid-template-columns:'+COLS+';gap:6px;padding:4px 10px 3px;margin-bottom:2px">'+
  ['NOMBRE','TY','LY','PTO','CUMPL.','BARRA','YoY'].map(function(l,i){
    return'<div style="font-size:9px;color:#5a6e96;font-weight:700;text-align:'+(i===0?'left':'center')+'">'+l+'</div>';
  }).join('')+'</div>';
}
function tRow(name, ty, ly, pto, col, i, onclick){
  var p=pto>0?pct(ty,pto):null;
  var bc=p!==null?barColor(p):col;
  var lyD=ly>0?ly:0;
  var yoyD=lyD>0?((ty-lyD)/lyD)*100:null;
  return'<div class="row '+(i%2===0?'ev':'od')+'" style="grid-template-columns:'+COLS+';border-left-color:'+col+'"'+(onclick?' onclick="'+onclick+'"':'')+'>'
    +'<div style="font-size:11px;font-weight:600;color:#dce4f5;overflow:hidden;text-overflow:ellipsis;white-space:nowrap">'+name+'</div>'
    +'<div style="text-align:right;font-size:14px;font-weight:800;color:'+col+';font-family:monospace">'+ty+'</div>'
    +'<div style="text-align:right;font-size:11px;color:#5a6e96;font-family:monospace">'+(lyD||'--')+'</div>'
    +'<div style="text-align:right;font-size:11px;color:#5a6e96;font-family:monospace">'+(pto||'--')+'</div>'
    +'<div style="text-align:center">'+(p!==null?pill(p):'<span class="pill b">s/p</span>')+'</div>'
    +bar(p!==null?Math.min(p,120):50, bc, 120)
    +'<div style="text-align:center;font-size:10px;font-weight:700;color:'+(yoyD!==null?(yoyD>=0?'#1fd67a':'#ef4444'):'#5a6e96')+';font-family:monospace">'+(yoyD!==null?(yoyD>=0?'▲':'▼')+Math.abs(yoyD).toFixed(0)+'%':'--')+'</div>'
  +'</div>';
}
function tTot(ty,ly,pto,col){
  var p=pto>0?pct(ty,pto):null;
  var yoyD=ly>0?((ty-ly)/ly)*100:null;
  return'<div class="tot-row" style="display:grid;grid-template-columns:'+COLS+';gap:6px;padding:8px 10px;align-items:center;margin-top:4px">'
    +'<div style="font-size:12px;font-weight:800;color:#4f7ef8">TOTAL</div>'
    +'<div style="text-align:right;font-size:15px;font-weight:900;color:#dce4f5;font-family:monospace">'+ty+'</div>'
    +'<div style="text-align:right;font-size:11px;color:#5a6e96;font-family:monospace">'+(ly||'--')+'</div>'
    +'<div style="text-align:right;font-size:11px;color:#5a6e96;font-family:monospace">'+(pto||'--')+'</div>'
    +'<div style="text-align:center">'+(p!==null?pill(p):'<span class="pill b">s/p</span>')+'</div>'
    +bar(p!==null?Math.min(p,120):50, p!==null?barColor(p):'#4f7ef8', 120)
    +'<div style="text-align:center;font-size:10px;font-weight:700;color:'+(yoyD!==null?(yoyD>=0?'#1fd67a':'#ef4444'):'#5a6e96')+';font-family:monospace">'+(yoyD!==null?(yoyD>=0?'▲':'▼')+Math.abs(yoyD).toFixed(0)+'%':'--')+'</div>'
  +'</div>';
}

// ═══════════════════════════════
// GLOBAL KPIs
// ═══════════════════════════════
function initGlobal(){
  var p=pct(GLOBAL.ty,GLOBAL.pto);
  var yoyV=((GLOBAL.ty-GLOBAL.ly)/GLOBAL.ly)*100;
  var kpis=[
    {l:"Venta TY",v:GLOBAL.ty+"u",c:p>=100?'#1fd67a':p>=80?'#f5c030':'#ef4444'},
    {l:"vs Presup.",v:pill(p)},
    {l:"Venta LY",v:GLOBAL.ly+"u",c:"#5a6e96"},
    {l:"YoY",v:(yoyV>=0?'▲':'▼')+Math.abs(yoyV).toFixed(1)+'%',c:yoyV>=0?'#1fd67a':'#ef4444'},
  ];
  var h=kpis.map(function(k){
    return'<div style="background:#0b0f1e;border:1px solid #1a2438;border-radius:8px;padding:6px 12px;text-align:center">'
      +'<div style="font-size:9px;color:#5a6e96">'+k.l+'</div>'
      +(k.v&&k.v.indexOf('pill')>-1?'<div style="margin-top:2px">'+k.v+'</div>':'<div style="font-size:15px;font-weight:900;color:'+(k.c||'#dce4f5')+';font-family:monospace;margin-top:2px">'+k.v+'</div>')
      +'</div>';
  }).join('');
  document.getElementById('globalKpis').innerHTML=h;
}

// ═══════════════════════════════
// HOME TABS
// ═══════════════════════════════
var activeTab='resumen';
function showTab(t,el){
  activeTab=t;
  document.querySelectorAll('#mainTabs .tab').forEach(function(b){b.classList.remove('active')});
  if(el)el.classList.add('active');
  renderHome();
}

function renderHome(){
  var h='';

  // ── RESUMEN
  if(activeTab==='resumen'){
    var p=pct(GLOBAL.ty,GLOBAL.pto);
    var yoyV=((GLOBAL.ty-GLOBAL.ly)/GLOBAL.ly)*100;

    // KPI boxes
    h+='<div class="g4" style="margin-bottom:14px">';
    [{l:"Ventas TY",v:GLOBAL.ty+"u",c:p>=100?'#1fd67a':'#f5c030',accent:'#f97316'},{l:"Presupuesto",v:GLOBAL.pto+"u",c:"#5a6e96",accent:"#5a6e96"},{l:"Cumpl. Presupuesto",pill:p,accent:barColor(p)},{l:"Venta LY",v:GLOBAL.ly+"u",c:"#5a6e96",yoy:yoyV,accent:"#5a6e96"}].forEach(function(k){
      h+='<div class="kpi-box" style="border-top:2px solid '+k.accent+'">';
      h+='<label>'+k.l+'</label>';
      if(k.pill!==undefined){h+=pill(k.pill);h+='<div class="bar-w" style="margin-top:6px"><div class="bar" style="width:'+Math.min(k.pill,120)/120*100+'%;background:'+barColor(k.pill)+'"></div></div>';}
      else{h+='<div class="kpi-val" style="color:'+k.c+'">'+k.v+'</div>';}
      if(k.yoy!==undefined)h+='<div class="kpi-sub">'+(k.yoy>=0?'▲':'▼')+Math.abs(k.yoy).toFixed(1)+'% vs ano anterior</div>';
      h+='</div>';
    });
    h+='</div>';

    // Top lineas resumen
    h+='<div class="g2">';
    // Top 5 lineas por ventas
    var topLineas=LINEAS.slice().sort(function(a,b){return b.ty-a.ty}).slice(0,8);
    h+='<div class="card"><div class="card-hdr"><h3>TOP LINEAS - Ventas TY</h3></div><div class="card-body">';
    var maxTL=topLineas[0].ty;
    topLineas.forEach(function(l,i){
      var p2=l.pto>0?pct(l.ty,l.pto):null;
      h+='<div style="display:grid;grid-template-columns:130px 45px 1fr 65px;gap:6px;align-items:center;padding:5px 8px;background:'+(i%2===0?'#0d1224':'#0b0f1e')+';border-radius:6px;border-left:3px solid '+l.col+';margin-bottom:3px;cursor:pointer" onclick="drillLinea(\''+l.cat+'\')">'
        +'<div style="font-size:11px;font-weight:700;overflow:hidden;text-overflow:ellipsis;white-space:nowrap">'+l.cat+'</div>'
        +'<div style="text-align:right;font-size:13px;font-weight:800;color:'+l.col+';font-family:monospace">'+l.ty+'</div>'
        +bar(l.ty/maxTL*100,l.col,100)
        +(p2!==null?pill(p2):'<span class="pill b">s/p</span>')
        +'</div>';
    });
    h+='</div></div>';
    // Vendedores resumen
    h+='<div class="card"><div class="card-hdr"><h3>VENDEDORES - Performance</h3><span style="font-size:9px;color:#252f48">Toca para ver detalle</span></div><div class="card-body">';
    VENDEDORES.forEach(function(v){
      var p3=v.pto>0?pct(v.ty,v.pto):0;
      h+='<div class="vcard" style="background:'+v.col+'15;border-color:'+v.col+'40;margin-bottom:8px" onclick="drillVendedor(\''+v.nombre+'\')"> '
        +'<div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:8px">'
        +'<div><div style="font-size:14px;font-weight:800">'+v.nombre+'</div><div style="font-size:10px;color:#5a6e96">Zona '+v.zona+'</div></div>'
        +'<div style="text-align:right"><div style="font-size:20px;font-weight:900;color:'+v.col+';font-family:monospace">'+v.ty+'u</div>'
        +(v.pto>0?'<div>'+pill(p3)+'</div>':'<div style="font-size:10px;color:#5a6e96">Ppto: '+v.pto+'u</div>')+'</div></div>'
        +'<div class="bar-w"><div class="bar" style="width:'+Math.min(p3,120)/120*100+'%;background:'+v.col+'"></div></div>';
      if(v.nota)h+='<div style="font-size:10px;color:#f5c030;margin-top:6px">⚠ '+v.nota+'</div>';
      h+='</div>';
    });
    h+='</div></div></div>';

    // Insights
    h+='<div class="card" style="border-color:#1e0d38"><div class="card-hdr"><h3 style="color:#a78bfa">ANALISIS ESTRATEGICO</h3></div><div class="card-body">';
    var pGen=pct(GLOBAL.ty,GLOBAL.pto);
    var yoyGen=((GLOBAL.ty-GLOBAL.ly)/GLOBAL.ly)*100;
    [
      {t:"g",txt:"Canal horizontal supera presupuesto: "+GLOBAL.ty+"u vs "+GLOBAL.pto+"u ppto ("+pGen.toFixed(0)+"% cumplimiento). Liderando en CONGELADOR (112% cumpl.), MINI BAR (127%) y CAMPANA DE OLOR (203%)."},
      {t:"r",txt:"Caida YoY del "+Math.abs(yoyGen).toFixed(0)+"% — de "+GLOBAL.ly+"u a "+GLOBAL.ty+"u. Impactado principalmente por REGULADOR DE GAS (2534u vs 6298u LY, -60%) y VENTILACION (-217u). Ambas sin presupuesto asignado."},
      {t:"r",txt:"AIRE ACONDICIONADO al 75% del presupuesto (331u vs 440u). ENCIMERA al 86% (398u vs 465u). COCINETA al 63% (564u vs 890u). Tres lineas con mayor brecha en valor absoluto."},
      {t:"y",txt:"CAMPANA DE OLOR destaca: 487u vs 240u ppto (203% cumplimiento, +1006% YoY). Oportunidad de expandir presupuesto en proximos periodos."},
      {t:"y",txt:"Juan Cordero: 593u vs 571u ppto (104% cumplimiento). STAMARIA S.A. es su cliente ancla con 140u. Revisar mix de VENTILADORES (151u sin presupuesto asignado)."},
    ].forEach(function(ins){
      var cols={g:'#1fd67a',r:'#ef4444',y:'#f5c030'};
      h+='<div class="insight" style="border-color:'+cols[ins.t]+';background:'+cols[ins.t]+'10;margin-bottom:6px">'
        +'<div style="width:16px;height:16px;border-radius:4px;background:'+cols[ins.t]+'20;display:flex;align-items:center;justify-content:center;font-size:10px;color:'+cols[ins.t]+';font-weight:900;flex-shrink:0">'+(ins.t==='g'?'↑':ins.t==='r'?'✕':'!')+'</div>'
        +'<p>'+ins.txt+'</p></div>';
    });
    h+='</div></div>';
  }

  // ── LINEAS
  else if(activeTab==='lineas'){
    h+='<div class="card"><div class="card-hdr"><h3>SELL-IN POR LINEA DE PRODUCTO</h3><span style="font-size:9px;color:#252f48">Toca para ver SKUs de esa linea</span></div><div class="card-body">';
    h+=tHead();
    var sorted=LINEAS.slice().sort(function(a,b){return b.ty-a.ty});
    sorted.forEach(function(l,i){h+=tRow(l.cat,l.ty,l.ly,l.pto,l.col,i,'drillLinea("'+l.cat+'")')});
    var tTy=LINEAS.reduce(function(s,l){return s+l.ty},0);
    var tLy=LINEAS.reduce(function(s,l){return s+l.ly},0);
    var tPto=LINEAS.reduce(function(s,l){return s+(l.pto||0)},0);
    h+=tTot(tTy,tLy,tPto,'#f97316');
    h+='</div></div>';
  }

  // ── SKUs
  else if(activeTab==='skus'){
    h+='<div class="card"><div class="card-hdr"><h3>SELL-IN POR MODELO/SKU - Top 30</h3></div><div class="card-body">';
    h+=tHead();
    SKUS.forEach(function(s,i){h+=tRow(s.sku,s.ty,s.ly,s.pto,s.col,i,'')});
    var tTy2=SKUS.reduce(function(s,r){return s+r.ty},0);
    var tLy2=SKUS.reduce(function(s,r){return s+(r.ly||0)},0);
    var tPto2=SKUS.reduce(function(s,r){return s+(r.pto||0)},0);
    h+=tTot(tTy2,tLy2,tPto2,'#f97316');
    h+='</div></div>';
  }

  // ── CLIENTES
  else if(activeTab==='clientes'){
    h+='<div class="card"><div class="card-hdr"><h3>TOP CLIENTES - Sell-In TY</h3></div><div class="card-body">';
    h+=tHead();
    CLIENTES.forEach(function(c,i){h+=tRow(c.cli,c.ty,c.ly,c.pto,c.col,i,'')});
    var tTy3=CLIENTES.reduce(function(s,r){return s+r.ty},0);
    var tLy3=CLIENTES.reduce(function(s,r){return s+(r.ly||0)},0);
    var tPto3=CLIENTES.reduce(function(s,r){return s+(r.pto||0)},0);
    h+=tTot(tTy3,tLy3,tPto3,'#f97316');
    h+='</div></div>';
  }

  // ── VENDEDORES
  else if(activeTab==='vendedores'){
    h+='<div class="g2">';
    VENDEDORES.forEach(function(v){
      var p=v.pto>0?pct(v.ty,v.pto):0;
      h+='<div class="vcard" style="background:'+v.col+'12;border-color:'+v.col+'40" onclick="drillVendedor(\''+v.nombre+'\')">'
        +'<div style="display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:12px">'
        +'<div><div style="font-size:16px;font-weight:900">'+v.nombre+'</div>'
        +'<div style="font-size:10px;color:#5a6e96;margin-top:2px">Zona '+v.zona+' · '+v.skus.length+' SKUs activos</div></div>'
        +'<div style="text-align:right"><div style="font-size:24px;font-weight:900;color:'+v.col+';font-family:monospace">'+v.ty+'</div><div style="font-size:10px;color:#5a6e96">unidades TY</div></div></div>'
        +'<div class="g3" style="margin-bottom:12px">'
        +'<div class="kpi-box"><label>Ppto</label><div class="kpi-val" style="color:#5a6e96;font-size:18px">'+v.pto+'u</div></div>'
        +'<div class="kpi-box"><label>Cumpl.</label>'+(v.pto>0?pill(p)+'<div class="bar-w" style="margin-top:6px"><div class="bar" style="width:'+Math.min(p,120)/120*100+'%;background:'+barColor(p)+'"></div></div>':'<div style="color:#5a6e96;font-size:12px">s/p</div>')+'</div>'
        +'<div class="kpi-box"><label>Clientes</label><div class="kpi-val" style="color:'+v.col+';font-size:18px">'+v.clientes.length+'</div></div>'
        +'</div>';
      if(v.nota)h+='<div style="background:#241a04;border:1px solid #f5c030;border-radius:8px;padding:8px 12px;font-size:11px;color:#f5c030;margin-bottom:10px">⚠ '+v.nota+'</div>';
      h+='<div style="font-size:9px;color:#5a6e96;margin-bottom:6px;font-weight:700">TOP 5 SKUs</div>';
      v.skus.slice(0,5).forEach(function(s,i){
        h+='<div style="display:flex;justify-content:space-between;align-items:center;padding:4px 8px;background:'+(i%2===0?'#0d1224':'#0b0f1e')+';border-radius:5px;margin-bottom:2px">'
          +'<div style="font-size:10px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;max-width:60%">'+s.sku+'</div>'
          +'<div style="display:flex;gap:8px;align-items:center;flex-shrink:0">'
          +'<span style="font-size:12px;font-weight:800;color:'+v.col+';font-family:monospace">'+s.ty+'u</span>'
          +(s.pto>0?pill(pct(s.ty,s.pto)):'<span class="pill b">s/p</span>')
          +'</div></div>';
      });
      h+='<div style="margin-top:8px;text-align:right"><span style="font-size:10px;color:'+v.col+'">Ver detalle completo →</span></div>';
      h+='</div>';
    });
    h+='</div>';
  }

  document.getElementById('homeContent').innerHTML=h;
}

// ═══════════════════════════════
// DRILL FUNCTIONS
// ═══════════════════════════════
function showDrill(bc, content){
  document.getElementById('page-home').classList.remove('active');
  document.getElementById('page-drill').classList.add('active');
  document.getElementById('drillBC').innerHTML='<button class="btn-back" onclick="goHome()">← Volver</button>'+bc.map(function(b,i){return'<span>›</span>'+(i===bc.length-1?'<b>'+b+'</b>':'<span style="font-size:11px;color:#5a6e96">'+b+'</span>')}).join('');
  document.getElementById('drillContent').innerHTML=content;
  document.getElementById('drillContent').scrollTop=0;
}
function goHome(){
  document.getElementById('page-drill').classList.remove('active');
  document.getElementById('page-home').classList.add('active');
}

// DRILL: Linea
function drillLinea(cat){
  var linea=LINEAS.filter(function(l){return l.cat===cat})[0];
  if(!linea)return;
  var skus=SKUS.filter(function(s){return s.cat===cat}).sort(function(a,b){return b.ty-a.ty});
  // Clientes top (show from global data)
  var p=linea.pto>0?pct(linea.ty,linea.pto):null;
  var h='<div class="g4" style="margin-bottom:14px">';
  [{l:"Venta TY",v:linea.ty+"u",c:linea.col},{l:"Ppto",v:(linea.pto||'s/p')+(linea.pto?' u':''),c:"#5a6e96"},{l:"Cumpl.",pill:p},{l:"Venta LY",v:linea.ly+"u",c:"#5a6e96",yoy:((linea.ty-linea.ly)/linea.ly)*100}].forEach(function(k){
    h+='<div class="kpi-box" style="border-top:2px solid '+(k.c||linea.col)+'">';
    h+='<label>'+k.l+'</label>';
    if(k.pill!==undefined){h+=(k.pill!==null?pill(k.pill):'<span class="pill b">s/p</span>');if(k.pill)h+='<div class="bar-w" style="margin-top:6px"><div class="bar" style="width:'+Math.min(k.pill,120)/120*100+'%;background:'+barColor(k.pill)+'"></div></div>';}
    else{h+='<div class="kpi-val" style="color:'+(k.c||linea.col)+'">'+k.v+'</div>';}
    if(k.yoy!==undefined)h+='<div class="kpi-sub">'+(k.yoy>=0?'▲':'▼')+Math.abs(k.yoy).toFixed(1)+'% vs LY</div>';
    h+='</div>';
  });
  h+='</div>';
  if(skus.length){
    h+='<div class="card"><div class="card-hdr"><h3>SKUS - Real vs Presupuesto</h3></div><div class="card-body">';
    h+=tHead();
    skus.forEach(function(s,i){h+=tRow(s.sku,s.ty,s.ly||0,s.pto,s.col,i,'')});
    var tTy=skus.reduce(function(s,r){return s+r.ty},0);
    var tLy=skus.reduce(function(s,r){return s+(r.ly||0)},0);
    var tPto=skus.reduce(function(s,r){return s+(r.pto||0)},0);
    h+=tTot(tTy,tLy,tPto,linea.col);
    h+='</div></div>';
  } else {
    h+='<div style="padding:20px;text-align:center;color:#5a6e96;font-size:12px">No hay SKUs disponibles para esta linea en el top 30</div>';
  }
  showDrill(['Lineas de Producto',cat],h);
}

// DRILL: Vendedor
function drillVendedor(nombre){
  var v=VENDEDORES.filter(function(x){return x.nombre===nombre})[0];
  if(!v)return;
  var p=v.pto>0?pct(v.ty,v.pto):0;
  var h='';
  // KPIs
  h+='<div class="g4" style="margin-bottom:14px">';
  [{l:"Venta TY",v:v.ty+"u",c:v.col},{l:"Presupuesto",v:v.pto+"u",c:"#5a6e96"},{l:"Cumpl.",pill:p,bar:p},{l:"Clientes activos",v:v.clientes.length,c:v.col}].forEach(function(k){
    h+='<div class="kpi-box" style="border-top:2px solid '+(k.c||v.col)+'">';
    h+='<label>'+k.l+'</label>';
    if(k.pill!==undefined){h+=pill(k.pill)+'<div class="bar-w" style="margin-top:6px"><div class="bar" style="width:'+Math.min(k.pill,120)/120*100+'%;background:'+barColor(k.pill)+'"></div></div>';}
    else{h+='<div class="kpi-val" style="color:'+(k.c||v.col)+'">'+k.v+'</div>';}
    h+='</div>';
  });
  h+='</div>';
  if(v.nota)h+='<div style="background:#241a04;border:1px solid #f5c030;border-radius:8px;padding:10px 14px;font-size:12px;color:#f5c030;margin-bottom:12px">⚠ '+v.nota+'</div>';

  h+='<div class="g2">';
  // SKUs
  h+='<div class="card"><div class="card-hdr"><h3>SKUs - Real vs Presupuesto</h3></div><div class="card-body">';
  h+=tHead();
  v.skus.forEach(function(s,i){h+=tRow(s.sku,s.ty,s.ly||0,s.pto||0,v.col,i,'')});
  var tTy=v.skus.reduce(function(s,r){return s+r.ty},0);
  var tLy=v.skus.reduce(function(s,r){return s+(r.ly||0)},0);
  var tPto=v.skus.reduce(function(s,r){return s+(r.pto||0)},0);
  h+=tTot(tTy,tLy,tPto,v.col);
  h+='</div></div>';

  // Clientes
  h+='<div class="card"><div class="card-hdr"><h3>TOP CLIENTES</h3></div><div class="card-body">';
  var COLS2="1fr 55px 55px 90px 95px";
  h+='<div style="display:grid;grid-template-columns:'+COLS2+';gap:6px;padding:4px 10px 3px;margin-bottom:2px">'+['CLIENTE','TY','PTO','CUMPL.','BARRA'].map(function(l,i){return'<div style="font-size:9px;color:#5a6e96;font-weight:700;text-align:'+(i===0?'left':'center')+'">'+l+'</div>';}).join('')+'</div>';
  v.clientes.forEach(function(c,i){
    var pc2=c.pto>0?pct(c.ty,c.pto):null;
    h+='<div class="row '+(i%2===0?'ev':'od')+'" style="grid-template-columns:'+COLS2+';border-left-color:'+v.col+'">'
      +'<div style="font-size:10px;font-weight:600;overflow:hidden;text-overflow:ellipsis;white-space:nowrap">'+c.cli+'</div>'
      +'<div style="text-align:right;font-size:13px;font-weight:800;color:'+v.col+';font-family:monospace">'+c.ty+'</div>'
      +'<div style="text-align:right;font-size:11px;color:#5a6e96;font-family:monospace">'+(c.pto||'--')+'</div>'
      +'<div style="text-align:center">'+(pc2!==null?pill(pc2):'<span class="pill b">s/p</span>')+'</div>'
      +bar(pc2!==null?Math.min(pc2,120):50,pc2!==null?barColor(pc2):v.col,120)
      +'</div>';
  });
  var tTy2=v.clientes.reduce(function(s,r){return s+r.ty},0);
  var tPto2=v.clientes.reduce(function(s,r){return s+(r.pto||0)},0);
  h+='<div class="tot-row" style="display:grid;grid-template-columns:'+COLS2+';gap:6px;padding:8px 10px;align-items:center;margin-top:4px">'
    +'<div style="font-size:12px;font-weight:800;color:#4f7ef8">TOTAL</div>'
    +'<div style="text-align:right;font-size:15px;font-weight:900;color:#dce4f5;font-family:monospace">'+tTy2+'</div>'
    +'<div style="text-align:right;font-size:11px;color:#5a6e96;font-family:monospace">'+tPto2+'</div>'
    +'<div style="text-align:center">'+pill(pct(tTy2,tPto2))+'</div>'
    +bar(Math.min(pct(tTy2,tPto2),120),barColor(pct(tTy2,tPto2)),120)
    +'</div>';
  h+='</div></div></div>';
  showDrill(['Vendedores',nombre],h);
}

// ═══════════════════════════════
// INIT
// ═══════════════════════════════
initGlobal();
renderHome();
</script>
</body>
</html>
